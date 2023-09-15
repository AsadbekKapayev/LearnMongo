$in

$nin

1) structure

```
{ field: { $in: [<value1>, <value2>,...] }}
```

The $in is a comparison query operator that allows you to select documents where the value of a field is equal to any value in an array.

The $nin is a query comparison operator that allows you to find documents


2) Using the $in opeator to match values

```
db.products.find({
    price: {
        $in: [699, 799]
    }
}, {
    name: 1,
    price: 1
})
```

3) Using the $in operator to match values in an array 

```
db.products.find({
    color: {
        $in: ["black", "white"]
    }
}, {
    name: 1,
    color: 1
})
```

4) Using the $in operator with regular expressions

```
db.products.find({
    color: {
        $in: [/^g+/, /^w+/]
    }
}, {
    name: 1,
    color: 1
})
```

