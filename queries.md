# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.
select productname, categoryname from products
join categories
on products.categoryid = categories.categoryid

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.
select orderid, shippername from orders where orderdate < 1997-01-09
join shippers
on orders.shipperid = shippers.shipperid (not working yet)

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
select productname, Quantity, * from OrderDetails where orderid=10251
join products
on orderdetails.productid = products.productid (not working aswell)


### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
select orders.orderid, customers.customername, employees.lastname
from orders
inner join employees on orders.EmployeeID = employees.EmployeeID
inner join customers on orders.customerid = customers.customerid



### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 