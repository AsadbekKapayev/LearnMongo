Insert many

1) structure

db.collection.insertMany(
    [document1, document2, ...],
    {
        writeConcern: <document>,
        ordered: <boolean>
    }
)

If an error occurs, the ordered insert will **stop** while the unordered insert will continue to process for the remaining documents in the queue.

2) example 

db.books.insertMany([
    { title:  "NoSQL Distilled", isbn: "0-4696-7030-4"},
    { title:  "NoSQL in 7 Days", isbn: "0-4086-6859-8"},
    { title:  "NoSQL Database", isbn: "0-2504-6932-4"},
]);

3) unordered 

db.books.insertMany(
[{ _id: 3, title:  "SQL Performance Tuning", isbn: "0-6799-2974-6"},
    { _id: 3, title:  "SQL Trees", isbn: "0-6998-1556-8"},
    { _id: 4, title:  "SQL Graph", isbn: "0-6426-4996-0"},
    { _id: 5, title:  "NoSQL Pros", isbn: "0-9602-9886-X"}],
    { ordered: false }
);
