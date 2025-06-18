#### Task 1 - Find all documents in the collection where the age is greater than 30, and only return the name and email fields.

```
db.test.find({ age: {$gt: 30}}, {name: 1, age: 1})
```

#### Task 2 - Find documents where the favorite color is either "Maroon" or "Blue."

```
db.test.find({ favoriteColor: { $in: ["Maroon", "Blue"]} })
```

#### Task 3 - Find all documents where the skill is an empty array.

```
db.test.find({skills: { $size: 0}})
```
