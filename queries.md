# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.
select productname, categoryname from categories
join products on categories.categoryid = products.categoryid

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.
select shippername, orderid, orderdate from orders
join shippers on orders.shipperid = shippers.shipperid
where orderid < 10409
order by orderdate

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
select productname, quantity from orderdetails
join products on orderdetails.productid = products.productid
where orderid = 10251
order by productname

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
select orderid, customername, lastname  as EmployeeLastName from orders
join employees on orders.EmployeeID = employees.EmployeeID
join customers on orders.customerid = customers.customerid

### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 