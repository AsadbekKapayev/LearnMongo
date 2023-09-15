$type

1) structure

```
{ field: { $type: <BSON type> } }
```

```
{ field: { $type: [ <BSON type1> , <BSON type2>, ... ] } }
```

The $type is an element query operator that allows you to select documents where the value of a field is an instance of a specified BSON type.

2) Using the $type operator example

```
db.products.find({
    price: {
        $type: "string"
    }
}, {
    name: 1,
    price: 1
})
```

3) Using the $type operator with the number alias example

```
db.products.find({
    price: {
        $type: "number"
    }
}, {
    name: 1,
    price: 1
})
```

4) Using the $type operator to query documents with multiple types

```
db.products.find({
    price: {
        $type: ["number", "string"]
    }
}, {
    name: 1,
    price: 1
})
```
