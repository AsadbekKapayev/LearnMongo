findOne

1) structure

```
db.collection.findOne(query, projection)
```

The findOne() accepts two optional arguments: query and projection.

The query is a document that specifies the selection criteria.
The projection is a document that specifies the fields in the matching document that you want to return.

2) example 

```
db.products.findOne({_id:2})
```

3) example 

```
db.products.findOne({_id: 5}, {name: 1})
```
