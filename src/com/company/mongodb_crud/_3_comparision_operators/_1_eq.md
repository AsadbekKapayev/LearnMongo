$eq

1) structure

```
{ <field>: { $eq: <value> } }
```

The $eq operator is a comparison query operator that allows you to match documents where the value of a field equals a specified value.

2) example

```
db.bookdb.find({ title: { $eq: 'example1' }})
```

3) Using $eq operator to check if an array element equals a value

```
db.products.find({
    color: "black"
}, {
    name: 1,
    color: 1
})
```

4) Using $eq operator to check if a field equals a date

```
db.products.find({
    releaseDate: {
        $eq: new ISODate("2020-05-14")
    }
}, {
    name: 1,
    releaseDate: 1
})
```

