# ConcurrencyDemo

This project demonstrates how to implement concurrency control strategies in a Java application. 

## Creating database and tables 

For this demo to work, you need to create a database named TheCoffeeBreak with the following tables:

* Customers
* Orders
* Coffees
* Suppliers

You can use the following scripts to create the tables:

```SQL
CREATE TABLE Customers(
  Id int primary key not null identity (1,1), 
  Name nvarchar(50) not null,
  LatestOrderStatus nvarchar(10), 
  Version rowversion
);
```
