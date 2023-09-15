$gt 

$gte

$lt

$lte

$ne

1) structure 

```
{ field: { $gt: value}}
```

The $gt operator is a comparison query operator that allows you to select documents where the value of a field is greater than (>) a specified value.

The $gte is a comparison query operator that allows you to select documents where a value of a field is greater than or equal to ( i.e. >=) a specified value.

The $lt operator is a comparison query operator that allows you to select the documents where the value of a field is less than a specified value.

The $lte is a comparison query operator that allows you to select documents where the value of a field is less than or equal to ( <= ) a specified value.

The $ne is a comparison query operator that allows you to select documents where the value of a filed is not equal to a specified value. It also includes documents that don’t contain the field.


2) Using $gt to select documents where the value of a field is greater than a specified value

```
db.products.find({
    price: {
        $gt: 699
    }
}, {
    name: 1,
    price: 1
})
```

3) Using the $gt operator to check if the value of a field in an embedded document is greater than a value

```
db.products.find({
    "spec.ram": {
        $gt: 8
    }
}, {
    name: 1,
    "spec.ram": 1
});
```

4) Using the $gt operator to check if an array element is greater than a value

```
db.products.find({
    storage: {
        $gt: 128
    }
}, {
    name: 1,
    storage: 1
})
```

5) Using the $gt operator to check if the value of a field is after a date

```
db.products.find({
    "releaseDate": {
        $gt: new ISODate('2015-01-01')
    }
}, {
    name: 1,
    releaseDate: 1
});
```


