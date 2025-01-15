# Incorrect use of $inc operator in MongoDB update query

This repository demonstrates an uncommon error in MongoDB update queries involving the `$inc` operator.  The error occurs when attempting to increment a field using a string value instead of a numeric value.

## Bug
The `$inc` operator is designed to increment numeric fields in MongoDB documents. Using a string value results in unexpected behavior. The update operation will likely fail silently or produce incorrect results depending on the MongoDB version and settings.

## Solution
The solution is simple: ensure the value you provide to `$inc` is always a number.