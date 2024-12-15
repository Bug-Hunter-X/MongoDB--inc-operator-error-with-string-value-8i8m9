# MongoDB $inc Operator Error with String Value

This example demonstrates an incorrect usage of the `$inc` operator in MongoDB. The `$inc` operator is used to increment or decrement a numerical value by a specified amount, but in this example it is used with a string value, which will result in an error.

## Bug
The bug lies in the usage of the `$inc` operator with a string value ('abc') instead of a number. This will lead to an error in the MongoDB update operation.

## Solution
The solution is to use a numerical value with the `$inc` operator. For example:
```javascript
db.collection('myCollection').updateOne({ _id: 1 }, { $inc: { field: 1 } });
```