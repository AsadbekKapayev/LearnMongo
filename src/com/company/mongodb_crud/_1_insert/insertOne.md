Insert one

1) structure

```
db.collection.insertOne(
    <document>,
    { writeConcern: <document>}
)
```

2) example

```
db.books.insertOne({
    title: 'MongoDB insertOne',
    isbn: '0-7617-6154-3'
});
```


The insertOne() method accepts two arguments:

document is a document that you want to insert into the collection. The document argument is required.
writeConcern is an optional argument that describes the level of acknowledgment requested from MongoDB for insert operation to a standalone MongoDB server or to shared clusters. We’ll discuss the writeConcern another tutorial.
The insertOne() method returns a document that contains the following fields:

acknowledged is a boolean value. It is set to true if the insert executed with write concern or false if the write concern was disabled.
insertedId stores the value of _id field of the inserted document.
