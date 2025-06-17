## This is all about mongodb

What I am learning about mongodb. I just put these here.

## We will learn these 4 commands

1. insertOne
2. insertMany
3. find
4. findOne

### 1. insertOne - To insert a document in mongodb

If you want to insert a document to mongodb
follow this command

```
db.testing.insertOne({name: "Ashraful", email: "ashraful@gmail.com"});
```

first of all, select db and give a dot(.) then write collection name give a dot(.) after writing collection now give a dot(.) to tell to insert a document by telling above command

### 2. InsertMany - For Insert 2 or more document

```
db.testing.insertMany([
    {
        name: "Sam", email: "sam@gmail.com"
    },
    {
        name: "Altman", email: "altman@gmail.com"
    },
    {
        name: "Siam", email: "siam@gmail.com"
    }
])

```

### 3. Find - for find all documents

```
db.testing.find({})
```

It will give your all documents

### 4. findOne - for find specific document

```
db.testing.find({ email: "altman@gmail.com"});
```
