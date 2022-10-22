# Mongo and Mongoose

SELECT reading_notes FROM dbo.code301 WHERE class LIKE '11';

## Reading

### [nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

Fill in the chart below with five differences between SQL and NoSQL databases:

| SQL | NoSQL |
|---|---|
| primarily called as Relational Databases (RDBMS) | primarily called as non-relational or distributed database |
| table based | document based, key-value pairs, graph databases or wide-column stores |
| predefined schema | dynamic schema for unstructured data |
| vertically scalable | horizontally scalable |
| uses Structured Query Language (SQL)) for defining and manipulating the data | Queries are focused on collection of documents. Sometimes it is also called as Unstructured Query Language (UnQL). The syntax of using UnQL varies from database to database. |

1. What kind of data is a good fit for an SQL database?
    1. SQL databases are good fit for the complex query intensive environment.
2. Give a real world example.
    1. MySQL is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js.
3. What kind of data is a good fit a NoSQL database?
    1. NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data)
4. Give a real world example.
    1.MongoDB is being used by some big companies like The New York Times, Craigslist, MTV Networks.
5. Which type of database is best for hierarchical data storage?
    1. NoSQL
6. Which type of database is best for scalability?
    1. In most typical situations, SQL databases are vertically scalable.

## Video

## [sql vs nosql](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

1. What does SQL stand for?
    1. structured query language
2. What is a relational database?
    1. "A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables. In a relational database, each row in the table is a record with a unique ID called the key. The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish the relationships among data points." [Oracle](https://www.oracle.com/database/what-is-a-relational-database/)
3. What type of structure does a relational database work with?
    1.
4. What is a ‘schema’?
    1. The database schema defines the requirements for what/how data is stored in tables
5. What is a NoSQL database?
    1. "NoSQL databases (aka "not only SQL") are non-tabular databases and store data differently than relational tables. NoSQL databases come in a variety of types based on their data model. The main types are document, key-value, wide-column, and graph. They provide flexible schemas and scale easily with large amounts of data and high user loads." [MongoDB](https://www.mongodb.com/nosql-explained)
6. How does it work?
    1. Magic. Probably. But no one knows for sure.
7. What is inside of a Mongo database?
    1. "In MongoDB, a database contains the collections of documents." [GeeksForGeeks](https://www.geeksforgeeks.org/mongodb-database-collection-and-document/#:~:text=In%20MongoDB%2C%20a%20database%20contains,databases%20on%20the%20MongoDB%20server.)
8. Which is more flexible - SQL or MongoDB? and why.
    1. "While MongoDB is more flexible and ensures high and diverse data availability, a SQL Database operates with the ACID (Atomicity, Consistency, Isolation, and Durability) properties and ensures greater reliability of transactions." [Hevo Data](https://hevodata.com/learn/mongodb-vs-sql/#:~:text=While%20MongoDB%20is%20more%20flexible,ensures%20greater%20reliability%20of%20transactions.)
9. What is the disadvantage of a NoSQL database?
    1. "One of the most frequently cited drawbacks of NoSQL databases is that they don’t support ACID (atomicity, consistency, isolation, durability) transactions across multiple documents. With appropriate schema design, single-record atomicity is acceptable for lots of applications. However, there are still many applications that require ACID across multiple records." [MongoDB](https://www.mongodb.com/nosql-explained/nosql-vs-sql#:~:text=and%20fewer%20bugs.-,What%20are%20the%20drawbacks%20of%20NoSQL%20databases%3F,acceptable%20for%20lots%20of%20applications.)

---

## Further Reading

-[mongoose api](https://mongoosejs.com/docs/api.html#Model)  
-[React Router](https://reactrouter.com/web/api/BrowserRouter)  
