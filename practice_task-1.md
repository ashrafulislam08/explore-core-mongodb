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

#### Task 4 - Find documents where the person has skills in both "JavaScript" and "Java"

```
db.test.find({
    $and: [{
        "skills.name": "JAVASCRIPT"
    },
    {
        "skills.name": "JAVA"
    }

    ]
})

```

#### Task 5 - Add a new skill to the skills array for the document with the email "amccurry3@cnet.com". The skill is {"name": "Python", "level": "Beginner", "isLearning": true}

```
db.test.updateOne({email: "bgorgen4@gravatar.com"}, {$push: {skills: {name: "PYTHON", level: "Beginner", isLearing: true}}})
```

#### Task 6 - Add a new language "Spanish" to the list of languages spoken by the person.

```
db.test.updateOne({email: "bgorgen4@gravatar.com"},
    {$push: {languages: "Spanish"}}
)
```

#### Task 7 - Remove the skill with the name "PYTHON" from the skills array.

```
db.test.updateOne({email: "bgorgen4@gravatar.com"}, {$pull: {"skills": {name: "PYTHON"} }})

```
