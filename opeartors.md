### MongoDB Field Filtering

```
    db.test.find({ gender: "Male"}, {gender: 1, name: 1, email: 1})
    db.test.find({ gender: "Female"}).project({name: 1, email: 1, gender: 1})

```

1 Mean stay
0 Mean Do not stay

## MongoDB Operators

# 📘 MongoDB Query Operators Cheat Sheet (with Examples)

---

## 🔁 Comparison Operators

| Operator | Description                                | Example                                       |
| -------- | ------------------------------------------ | --------------------------------------------- |
| `$eq`    | Matches values equal to a specified value. | `{ age: { $eq: 30 } }`                        |
| `$gt`    | Greater than a specified value.            | `{ score: { $gt: 80 } }`                      |
| `$lt`    | Less than a specified value.               | `{ price: { $lt: 100 } }`                     |
| `$gte`   | Greater than or equal to.                  | `{ marks: { $gte: 40 } }`                     |
| `$lte`   | Less than or equal to.                     | `{ quantity: { $lte: 10 } }`                  |
| `$ne`    | Not equal to a specified value.            | `{ status: { $ne: "active" } }`               |
| `$in`    | Matches any value in an array.             | `{ category: { $in: ["food", "clothing"] } }` |
| `$nin`   | Matches none of the values in an array.    | `{ type: { $nin: ["used", "refurbished"] } }` |

---

## 🧠 Logical Operators

| Operator | Description                         | Example                                                     |
| -------- | ----------------------------------- | ----------------------------------------------------------- |
| `$and`   | Combines conditions with AND logic. | `{ $and: [ { age: { $gt: 18 } }, { age: { $lt: 30 } } ] }`  |
| `$or`    | Combines conditions with OR logic.  | `{ $or: [ { city: "NY" }, { city: "LA" } ] }`               |
| `$not`   | Inverts the query condition.        | `{ score: { $not: { $gt: 80 } } }`                          |
| `$nor`   | None of the conditions are true.    | `{ $nor: [ { status: "pending" }, { status: "failed" } ] }` |

---

## 📌 Element Operators

| Operator  | Description          | Example                        |
| --------- | -------------------- | ------------------------------ |
| `$exists` | Field exists or not. | `{ phone: { $exists: true } }` |
| `$type`   | Matches BSON type.   | `{ age: { $type: "int" } }`    |

---

## 📏 Evaluation Operators

| Operator      | Description                               | Example                                                                |
| ------------- | ----------------------------------------- | ---------------------------------------------------------------------- |
| `$expr`       | Use aggregation expressions in queries.   | `{ $expr: { $gt: ["$spent", "$budget"] } }`                            |
| `$jsonSchema` | Validate documents against a JSON schema. | `{ $jsonSchema: { bsonType: "object", required: ["name", "email"] } }` |
| `$mod`        | Modulus operation.                        | `{ score: { $mod: [5, 0] } }` (Multiples of 5)                         |
| `$regex`      | Regular expression match.                 | `{ name: { $regex: "^A", $options: "i" } }`                            |
| `$text`       | Text search using text index.             | `{ $text: { $search: "mongodb" } }`                                    |
| `$where`      | JavaScript condition.                     | `{ $where: "this.age > 18" }`                                          |

---

## 🌍 Geospatial Operators

| Operator         | Description                      | Example                                                                                                     |
| ---------------- | -------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `$geoWithin`     | Matches geometry inside shape.   | `{ location: { $geoWithin: { $center: [[50, 50], 10] } } }`                                                 |
| `$geoIntersects` | Intersects with a given shape.   | `{ location: { $geoIntersects: { $geometry: { type: "Polygon", coordinates: [...] } } } }`                  |
| `$near`          | Returns documents near a point.  | `{ location: { $near: { $geometry: { type: "Point", coordinates: [40, 5] }, $maxDistance: 1000 } } }`       |
| `$nearSphere`    | Same as `$near` but on a sphere. | `{ location: { $nearSphere: { $geometry: { type: "Point", coordinates: [40, 5] }, $maxDistance: 1000 } } }` |

---

## 🧩 Array Operators

| Operator     | Description                                               | Example                                             |
| ------------ | --------------------------------------------------------- | --------------------------------------------------- |
| `$all`       | Matches arrays that contain all specified elements.       | `{ tags: { $all: ["red", "blue"] } }`               |
| `$elemMatch` | Matches array element that satisfies multiple conditions. | `{ scores: { $elemMatch: { $gt: 80, $lt: 100 } } }` |
| `$size`      | Matches array of specified length.                        | `{ items: { $size: 3 } }`                           |

---

## 💡 Bitwise Operators

| Operator        | Description                        | Example                                |
| --------------- | ---------------------------------- | -------------------------------------- |
| `$bitsAllClear` | All bits at given positions are 0. | `{ flags: { $bitsAllClear: [1, 4] } }` |
| `$bitsAllSet`   | All bits at given positions are 1. | `{ flags: { $bitsAllSet: [1, 4] } }`   |
| `$bitsAnyClear` | Any bit at position is 0.          | `{ flags: { $bitsAnyClear: [1, 4] } }` |
| `$bitsAnySet`   | Any bit at position is 1.          | `{ flags: { $bitsAnySet: [1, 4] } }`   |

---

## 📝 Comments Operator

| Operator   | Description           | Example                                                      |
| ---------- | --------------------- | ------------------------------------------------------------ |
| `$comment` | Add comment to query. | `{ age: { $gt: 25 }, $comment: "Filtering adults over 25" }` |
