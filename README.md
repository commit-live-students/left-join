![GitHub Logo](https://s3.ap-south-1.amazonaws.com/greyatom-social/GreyAtom-logo.png)

# LEFT JOINS

The SQL LEFT JOIN returns all rows from the left table, even if there are no matches in the right table. This means that if the ON clause matches 0 (zero) records in the right table; the join will still return a row in the result, but with NULL in each column from the right table.

This means that a left join returns all the values from the left table, plus matched values from the right table or NULL in case of no matching join predicate.

### Syntax

The basic syntax of a LEFT JOIN is as follows.

        SELECT table1.column1, table2.column2...
        FROM table1
        LEFT JOIN table2
        ON table1.common_field = table2.common_field;

Here, the given condition could be any given expression based on your requirement.

Now, let us join these two tables using the LEFT JOIN as follows.

        SELECT  Customers.CustomerID, Customers.CustomerName, ORDERS.OrderDate
            FROM Customers
            LEFT JOIN ORDERS
            ON Customers.CustomerID = ORDERS.CustomerID;

This would produce the following result −

| CustomerID | CustomerName | OrderDate |
| ---------- | --------- | --------- |
| 51 | Bottom-Dollar Marketse	| 2017-03-20 |
| 71 | Split Rail Beer & Ale | 2016-11-21 |
| 72 | Princesa Isabel Vinhoss	| 2016-12-29 |
| 73 | Folk och fä HB	| 2017-01-04 |
| 74 | Consolidated Holdings	| 2017-03-28 |
