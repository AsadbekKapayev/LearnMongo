$all

1) structure
```
{ <arrayField>: { $all: [element1, element2, ...]} }
```

```
{ <arrayField>: element1 }
```

The $all is an array query operator that allows you to find the documents where the value of a field is an array that contains all the specified elements.

```
{ arrayField: {$all: [element1, element2]} }

equivalent

{ $and: [{ arrayField: element1}, {arrayField: element2} ]}
```

2) Using MongoDB $all operator to match values

```
db.products.find({
    color: {
        $all: ["black", "white"]
    }
}, {
    name: 1,
    color: 1
})
```


