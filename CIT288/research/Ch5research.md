[//]: # (Created by Chaz Davis on 2020-02-06)
Same instructions as always:
1.   What is a relational database and what are its principal ingredients?
2.   How many primary keys and how many foreign keys may a table have in a relational database?
3.   Explain the nature of the inference threat to an RDBMS.
4.   What are the disadvantages of database encryption?

https://www.quora.com/What-are-the-pros-and-cons-of-using-database-encryption/answer/Guy-Birkbeck?ch=99&share=cdddb33c&srid=H9wz

5.  What is an SQLi?  How does one attack using this method?  

SQL injection is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database. It generally allows an attacker to view data that they are not normally able to retrieve. This might include data belonging to other users, or any other data that the application itself is able to access. In many cases, an attacker can modify or delete this data, causing persistent changes to the application's content or behavior.
In some situations, an attacker can escalate an SQL injection attack to compromise the underlying server or other back-end infrastructure, or perform a denial-of-service attack.

There are a wide variety of SQL injection vulnerabilities, attacks, and techniques, which arise in different situations. Some common SQL injection examples include:
Retrieving hidden data, where you can modify an SQL query to return additional results.
Subverting application logic, where you can change a query to interfere with the application's logic.
UNION attacks, where you can retrieve data from different database tables.
Examining the database, where you can extract information about the version and structure of the database.
Blind SQL injection, where the results of a query you control are not returned in the application's responses.

6. Define Defensive coding.

A form of defensive design intended to ensure the continuing function of a piece of software in spite of unforeseeable usage of said software. The idea can be viewed as reducing or eliminating the prospect of Murphy's Law having effect. Defensive programming techniques are used especially when a piece of software could be misused mischievously or inadvertently to catastrophic effect.
What I'm really talking about is a combination of the following guidelines:
Every line of code is a liability

Codify your assumptions

Executable documentation is preferable [1]


7.  What is an attribute in a database.  Give an example.
8.  Explain cascading authorizations.  Is there a "downside " to this method of security?  
9.  What is an in-band attack?  Is there such a thing as an out-of-band attack?  

In-band SQLi (Classic SQLi)
In-band SQL Injection is the most common and easy-to-exploit of SQL Injection attacks. In-band SQL Injection occurs when an attacker is able to use the same communication channel to both launch the attack and gather results.
The two most common types of in-band SQL Injection are Error-based SQLi and Union-based SQLi

Out-of-band SQLi
Out-of-band SQL Injection is not very common, mostly because it depends on features being enabled on the database server being used by the web application. Out-of-band SQL Injection occurs when an attacker is unable to use the same channel to launch the attack and gather results.
Out-of-band techniques, offer an attacker an alternative to inferential time-based techniques, especially if the server responses are not very stable (making an inferential time-based attack unreliable).
Out-of-band SQLi techniques would rely on the database server’s ability to make DNS or HTTP requests to deliver data to an attacker. Such is the case with Microsoft SQL Server’s xp_dirtree command, which can be used to make DNS requests to a server an attacker controls; as well as Oracle Database’s UTL_HTTP package, which can be used to send HTTP requests from SQL and PL/SQL to a server an attacker controls.

10.  What is "blind" SQL injection?  


Blind SQL (Structured Query Language) injection is a type of SQL Injection attack that asks the database true or false questions and determines the answer based on the applications response. This attack is often used when the web application is configured to show generic error messages, but has not mitigated the code that is vulnerable to SQL injection.
When an attacker exploits SQL injection, sometimes the web application displays error messages from the database complaining that the SQL Query’s syntax is incorrect. Blind SQL injection is nearly identical to normal SQL Injection, the only difference being the way the data is retrieved from the database. When the database does not output data to the web page, an attacker is forced to steal data by asking the database a series of true or false questions. This makes exploiting the SQL Injection vulnerability more difficult, but not impossible. .


Charles Davis II
