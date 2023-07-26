projection

1) structure

{ <field>: value, ...}
{ "<embeddedDocument>.<field>": value, ... }
{ "<arrayField>.field": value, ...}

2) example

db.products.find({}, {
    name: 1,
    price: 1,
    _id: 0
});

3) The following example returns all fields of the document _id 1 except for releaseDate, spec, and storage fields:

db.products.find({_id:1}, {
    releaseDate: 0,
    spec: 0,
    storage: 0
})

4) The following example returns the name, price, and _id fields of document _id 1. It also returns the screen field on the spec embedded document:

db.products.find({_id:1}, {
    name: 1,
    price: 1,
    "spec.screen": 1
})



