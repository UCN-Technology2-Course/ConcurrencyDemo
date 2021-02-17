# ConcurrencyDemo

This project demonstrates how to implement concurrency control strategies in a Java application. 

## Creating database and tables 

For this demo to work, you need to create a relational database (MS SQL Server) named TheCoffeeBreak with the following tables:

* Customers
* Orders

You can use the following scripts to create the tables:

```SQL
CREATE TABLE Customers(
  Id int primary key not null identity (1,1), 
  Name nvarchar(50) not null,
  LatestOrderStatus nvarchar(10), 
  Version rowversion
);

CREATE TABLE Orders(
  Id int primary key not null identity(1,1), 
  CustomerId int not null foreign key references Customers(Id), 
  Placed datetime not null
);  
```
