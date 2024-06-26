# MySQL
## Introduction

> **Module:**
> 1. Database 
> 2. DBMS
> 3. Types of Databases
> 4. RDBMS
> 5. Installation & Setup
> 

### Database

<aside>
💡 A Database is a collection of data stored in a format that can be easily accessed, managed, and updated.
</aside>

### DBMS

<aside>
💡 A DBMS serves as an interface (Application) between the end-user and a database, allowing users to CRUD (Create, Read, Update, and Delete) data in the database.
</aside>

<aside>
  
</aside>

![image](https://github.com/praveensriram01/MySQL/assets/72486482/2a18fae4-ca00-4774-939d-8b7663d4d74d)

<aside>

</aside>

### Types of Database

<aside>
💡 The major difference b/w SQL and NoSQL is based on how the data are stored in a database.

</aside>

<aside>
  
</aside>

![image](https://github.com/praveensriram01/MySQL/assets/72486482/6be33547-b0fd-49ac-b3bd-6e25b1f6c42a)

### Relational Database

- It is a way of representing data in tables.
- Each row in the table is a record with unique id called key.
- The columns of the table hold attributes of data.
- The relational data model provides a standard way of representing and querying data that could be used by any application.
- Structured Query Language (SQL) is used to write and query data in a database.
- It is used in several applications: [ Track inventories, E-commerce transaction, Sales, Banking, Finance, Billing, etc., ]

### MySQL

- Free and Open source
- Huge community support
- Extensively tested
- High stability
- Available for all major platforms
- Replication and sharing are available
- Covers a wide range of use cases

# Querying

### Select Statement

```sql
SELECT *
FROM Shippings;
```
```
-- OP:
shipping_id	 status	    customer
1	           Pending	   2
2	           Pending	   4
3	           Delivered	 3
4	           Pending	   5
5	           Delivered 	 1
```

### Select Clause

### Where Clause

```
SELECT * 
FROM Shippings 
WHERE status = "Pending";
```
```
-- OP:
shipping_id	 status	 customer
1.           Pending	  2
2	           Pending	  4
4	           Pending	  5
```

### Logical Operator [ AND, OR, NOT ]

## AND Operator
```
SELECT * 
FROM Orders
WHERE amount >=300 AND amount <= 400;
```
```
-- OP:
zorder_id	  item	     amount	customer_id
1	          Keyboard	  400	   4
2	          Mouse	      300	   4
4	          Keyboard	  400	   1
```

## OR Operator
```
SELECT * 
FROM Orders
WHERE NOT (amount >=300 OR amount <=400);
```
```
-- OP:
order_id	item	    amount	customer_id
1	        Keyboard	400	    4
2	        Mouse	    300	    4
3	        Monitor	  12000	  3
4	        Keyboard	400	    1
5	        Mousepad	250	    2
```

## NOT Operator
```
SELECT * 
FROM Orders
WHERE NOT (amount >=300 AND amount <=400);
```
```
-- OP:
order_id	item	    amount	customer_id
3	        Monitor	  12000	   3
5	        Mousepad	250	     2
```
