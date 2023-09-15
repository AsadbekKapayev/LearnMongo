MongoDB provides you with three ways to identify a BSON type: string, number, and alias. The following table lists the BSON types identified by these three forms:

```
Type	            Number	Alias
Double	            1	    “double”
String	            2	    “string”
Object	            3	    “object”
Array	            4	    “array”
Binary data	        5	    “binData”
ObjectId	        7	    “objectId”
Boolean	            8	    “bool”
Date	            9	    “date”
Null	            10	    “null”
Regular Expression	11	    “regex”
JavaScript	        13	    “javascript”
32-bit integer	    16	    “int”
Timestamp	        17	    “timestamp”
64-bit integer	    18	    “long”
Decimal128	        19	    “decimal”
Min key	            -1	    “minKey”
Max key	            127	    “maxKey”
```

The $type operator also supports the number alias that matches against the following BSON types:

- double
- 32-bit integer
- 64-bit integer
- decimal
