#How to concatenate rows in sql server
The STRING_AGG() is usefull.

SELECT STRING_AGG(ProductName, ', ') AS ConcatenatedProducts
FROM Products;

