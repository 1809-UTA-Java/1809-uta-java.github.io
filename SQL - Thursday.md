# JDBC
JDBC API from `java.sql` package. It's a SQL API, not embedded SQL for Java.

## Interfaces
**DriverManager** Pass a url, username, and password to a builder pulled from the jdbc driver jar of your respective database. Will then allow you to create a Connection and then send through it a Statement.
**Connection** Using DriverManager, you obtain a Connection object that represents a database connection to send SQL statements
**Statement** A representation of a SQL command that you will execute.
**ResultSet** Results of a query will be stored and delivered through this object, and accessed by numerous getters.

## Process
Usually the JDBC driver classes from your jar will register themselves with the DriverManager using registerDriver() or the Class.forName() method.

After the required driver is loaded and registered, you can connect to the database by calling DriverManager.getConnection(). This will deliver a connection object that wraps around your RDBMS connection, which is pulled from the connection pool.

You specify the database to connect with a jdbc url:
>jdbc:*subprotocol*:host:/databasename

In our case it's
>jdbc:oracle:thin:@192.168.56.105:1521:xe

The subprotocol identifies the particular database system and the client that we will use to connect to it.

Once you have your connection, you will use createStatement() on the connection to give you an object that implements a Statement.

## Statement
A Statement object sends queries and updates, as well as receive errors or ResultSets.
**Statement** is prone to SQL Injection attacks, especially if you use a raw string to write the query.
**PreparedStatement** is a precompiled SQL statement. It is best used for writing several similar queries in a loop, but will also as a side effect protect against SQL Injections
```
PreparedStatement ps = myConnection.prepareStatement("UPDATE ANIMALS SET name=? WHERE id=?");
ps.setString(1, "Hippo");
ps.setInt(2, 7);
ps.executeQuery();
```
**CallableStatement** execute stored procedures and can return 1 or many ResultSets.


