exists

1) structure

```
{ field: { $exists: <boolean_value> } }
```

The $exists is an element query operator that has the following syntax:

2) Using the MongoDB $exists operator example

```
db.products.find(
   {
 price: {
 $exists: true
 } 
}, 
   {
 name: 1,
 price: 1
 }
)
```

3) Using the MongoDB $exists operator to query documents that don’t have a specified field

```
db.products.find({
    price: {
        $exists: false
    }
}, {
    name: 1,
    price: 1
});
```


