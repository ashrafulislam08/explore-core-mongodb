### MongoDB Field Filtering

```
    db.test.find({ gender: "Male"}, {gender: 1, name: 1, email: 1})

```

1 Mean stay
0 Mean Do not stay

## MongoDB Operators

# 📘 MongoDB Query Operators Cheat Sheet

MongoDB provides a rich query language with various operators. Here’s a categorized overview:

---

## 🔁 Comparison Operators

| Operator | Description                                                       |
| -------- | ----------------------------------------------------------------- |
| `$eq`    | Matches values that are equal to the given value.                 |
| `$gt`    | Matches values that are greater than the given value.             |
| `$lt`    | Matches values that are less than the given value.                |
| `$gte`   | Matches values that are greater than or equal to the given value. |
| `$lte`   | Matches values that are less than or equal to the given value.    |
| `$ne`    | Matches values that are not equal to the given value.             |
| `$in`    | Matches any of the values specified in an array.                  |
| `$nin`   | Matches none of the values specified in an array.                 |

---

## 🧠 Logical Operators

| Operator | Description                               |
| -------- | ----------------------------------------- |
| `$and`   | Joins query clauses with a logical AND.   |
| `$or`    | Joins query clauses with a logical OR.    |
| `$not`   | Inverts the effect of a query expression. |
| `$nor`   | Joins query clauses with a logical NOR.   |

---

## 📌 Element Operators

| Operator  | Description                                                 |
| --------- | ----------------------------------------------------------- |
| `$exists` | Matches documents that have the specified field.            |
| `$type`   | Selects documents if a field is of the specified BSON type. |

---

## 📏 Evaluation Operators

| Operator      | Description                                                          |
| ------------- | -------------------------------------------------------------------- |
| `$expr`       | Allows the use of aggregation expressions within the query language. |
| `$jsonSchema` | Validates documents against the given JSON Schema.                   |
| `$mod`        | Performs a modulo operation on the value of a field.                 |
| `$regex`      | Selects documents where values match a specified regular expression. |
| `$text`       | Performs text search on content indexed with a text index.           |
| `$where`      | Matches documents that satisfy a JavaScript expression.              |

---

## 🌍 Geospatial Operators

| Operator         | Description                                               |
| ---------------- | --------------------------------------------------------- |
| `$geoWithin`     | Matches geometries within a bounding shape.               |
| `$geoIntersects` | Matches geometries that intersect with a given shape.     |
| `$near`          | Returns documents sorted by proximity to a point.         |
| `$nearSphere`    | Similar to `$near`, but calculates distances on a sphere. |

---

## 🧩 Array Operators

| Operator     | Description                                                                                      |
| ------------ | ------------------------------------------------------------------------------------------------ |
| `$all`       | Matches arrays that contain all elements specified.                                              |
| `$elemMatch` | Matches documents that contain an array field with at least one element matching all conditions. |
| `$size`      | Matches any array with the specified number of elements.                                         |

---

## 💡 Bitwise Operators

| Operator        | Description                                                    |
| --------------- | -------------------------------------------------------------- |
| `$bitsAllClear` | Matches documents where all given bit positions are clear (0). |
| `$bitsAllSet`   | Matches documents where all given bit positions are set (1).   |
| `$bitsAnyClear` | Matches documents where any given bit position is clear.       |
| `$bitsAnySet`   | Matches documents where any given bit position is set.         |

---

## 📝 Comments Operator

| Operator   | Description                                          |
| ---------- | ---------------------------------------------------- |
| `$comment` | Adds a comment to a query to help trace or debug it. |
