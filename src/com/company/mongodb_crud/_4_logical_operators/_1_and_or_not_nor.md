$and 

$or 

$not 

$nor 

1) structure

```
$and :[{expression1}, {expression2},...]
```

The $and is a logical query operator that allows you to carry a logical AND operation on an array of one or more expressions.

The $or is a logical query operator that carries a logical OR operation on an array of one or more expressions and selects the documents that satisfy at least one expression.

```
{ field: { $not: { <expression> } } }
```

The $not operator is a logical query operator that performs a logical NOT operation on a specified <expression> and selects documents that do not match the <expression>. This includes the documents that do not contain the field.

```
{ $nor: [ { <expression1> }, { <expression2> },...] }
```

The $nor is a logical query operator that allows you to perform a logical NOR operation on a list of one or more query expressions and selects documents that fail all the query expressions.


Implicit AND operator

```
{ field: { expression1, expression2, ... }
```


2) Using MongoDB $and operator example

```
db.products.find({
    $and: [{
        price: 899
    }, {
        color: {
            $in: ["white", "black"]
        }
    }]
}, {
    name: 1,
    price: 1,
    color: 1
})
```

3) Using MongoDB $and operator with the same field

```
db.products.find({
    price: {
        $eq: 699,
        $exists: true
    }
}, {
    name: 1,
    price: 1,
    color: 1
})
```

