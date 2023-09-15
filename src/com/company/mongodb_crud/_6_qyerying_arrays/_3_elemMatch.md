$elemMatch

1) structure

{ <arrayField>: {$elemMatch: { <query1>, <query2>, ...} } }

The $elemMatch is an array query operator that matches documents that contain an array field and the array field has at least one element that satisfies all the specified queries.

2) Using the MongDB $elemMatch opeator example

```
db.products.find({
    storage: {
        $elemMatch: {
            $lt: 128
        }
    }
}, {
    name: 1,
    storage: 1
});
```
