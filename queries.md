# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.
```SELECT ProductName, CategoryID FROM Products;```

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.
```SELECT orders.orderid, shippers.shippername from orders inner join shippers on orders.shipperid = shippers.shipperid where orders.orderdate < '1997-01-09';```

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
```SELECT products.productname, orderdetails.quantity, orderdetails.productid from orderdetails inner join products on products.productid = orderdetails.productid where orderdetails.orderid = '10251' order by productname;```

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
```SELECT orders.orderid, orders.employeeid, employees.employeeid, employees.lastname from orders inner join employees on orders.employeeid = employees.employeeid```

### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records.  