find

1) structure

db.collection.find(query, projection)

Similar to the findOne() method, the find() method accepts two optional arguments.

The query is a document that specifies the selection criteria.
The projection is a document that specifies the fields in the matching document that you want to return.

2) example 

db.books.find()

3) example 

db.books.find({_id: 10})

4) example 

db.books.find({ categories: 'Java'}, { title: 1,isbn: 1,_id: 0})
