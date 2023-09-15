$sort

1) structure

```
cursor.sort({field1: order, field2: order, ...})
```

The sort() method allows you to sort the matching documents by one or more fields (field1, field2, …) in ascending or descending order.

2) Sorting document by one field examples 

```
db.products.find({
    'price': {
        $exists: 1
    }
}, {
    name: 1,
    price: 1
}).sort({
    price: 1
})
```

3) Sorting document by two or more fields example

```
db.products.find({
    'price': {
        $exists: 1
    }
}, {
    name: 1,
    price: 1
}).sort({
    price: 1,
    name: 1
});
```

4) Sorting documetns by dates

```
db.products.find({
    releaseDate: {
        $exists: 1
    }

}, {
    name: 1,
    releaseDate: 1
}).sort({
    releaseDate: 1
});
```

5) Sorting documents by fields in embedded documents

```
db.products.find({}, {
    name: 1,
    spec: 1
}).sort({
    "spec.ram": 1
});
```

