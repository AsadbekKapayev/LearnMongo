$size

1) structure

```
{ array_field: {$size: element_count} }
```

The $size is an array query operator that allows you to select documents that have an array containing a specified number of elements.

2) Using MongoDB $size operator to select documents that have an array containing a number of elements

```
db.products.find({
    color: {
        $size: 2
    }
}, {
    name: 1,
    color: 1
})
```

2) Using MongoDB $size operator with the $or operator example

```
db.products.find({
    $or: [{
            color: {
                $size: 1
            }
        },
        {
            color: {
                $size: 2
            }
        }
    ]
}, {
    name: 1,
    color: 1
})
```


