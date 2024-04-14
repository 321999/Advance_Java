![image](https://github.com/321999/Advance_Java/assets/73833132/c090be5d-cd1f-464d-9204-6e0c46690bd7)
types of java addition 
	normal(jse ,core java)
	java enterprise(addition of java,jee,j2ee) 
	java micron 
purpose of diifereren addtion:
	JSE 
		swing
		     swing is a library of java which is set of gui components,and tools for building destoop application 
		Applet
		     Applet is an computer program that perform speccific task 
			usign JSE we can build standalone application (if an application needs to be install on a platform to be used such kind application is called are standalone applcation ex:vlc media)
	JEE
		We can build web application with the help of (applicationn which is going to be deployed on the server os known as web application)
		To build web applicatio we can take the help of servlet or spring (intagram,amazon)
	JME 
		java micro addtion is a subset of java platform which is designed for resource constraint devices such as mobile phones
		opera mini ,nokia naps ,google maps(earliesr version) 
	Mvc ARCHITECTURE 

 data logic,where getters an setters 
 	#View (user interface)
  	* it represents current models state 
   	* it takes input from user and display output to user

 	#Controller(buisiness logic)
  	* controlles and decides how data is dipllayed
   	* 
    # what is MVC ARchitecture ?
    	* it is software architecture pattern commonly used in development of appllication 
     	* particularly in context with web applicatio and desktop applcation 
      	* it is away to orgainise and structure a code to enhance the maintainability modularity and scalability 
       ** package declaration 
	##Naming convention
 ```
	domain_extension.organisation_name.project_name.controller
  	domain_extension.organisation_name.project_name.view
   	gov.uidai.library.model
	com.indian_website. gov
 ```
## JDBC 
java to database connectivity 
* whenever we write java program and whenever that program need to communicate with the database we need jdbc api
* jdbc api stands as an interface between java program and the database
* jdbc api is an only api which helps to eastablish connection between java program and database
# API 
* Application programing interface
* an api set of rules and protocols that defines how diffferent software component should interact with each other
* it provides structuure and standardise way for different application or modules to communicate an exchange data

  data:
  data is an information about entity

  ### data storage solution
  	data storage is a concern which deals with where and how we store inforamtion
  	* File storage
  	* database

Advance java

| File storage         | database |
|--------------|:-----:|-----------:|
| Provide less security  |  Provide more security  |        739 |
| No efficient query processing|  Efficient query processing  |          6 |
|Less complexity to hanldle|Complex to handle |


Add headings (Format > Paragraph styles) and they will appear in your table of contents.
||	File storage || database||
Provide less security 
No efficient query processing 
Less complexity to hanldle
Database:
Provide more security 
Efficient query processing 
Complex to handle 
Database is the place where we store the data in structure or in organised manner 
  
## how does jdbc helps

suppose java application need to comuunicate with the database then we will take the help fo jdbc api
jdbc api will now convert any java instruction into database understandable language
so we need something which can do conversion work 

### Driver software will help to convert java istruction to database java understandable language and vice versa 
![image](https://github.com/321999/Advance_Java/assets/73833132/4b42885d-3781-43de-bcab-c63c2190f98e)


# who will provide the driver software 
driver software is provided by the database vendors 
jdbc api is independent of database 
where driver software iw dependent of software 
  

  ```
Advance java
Add headings (Format > Paragraph styles) and they will appear in your table of contents.

File storage 
Provide less security 
No efficient query processing 
Less complexity to hanldle

Database:
Provide more security 
Efficient query processing 
Complex to handle 

Database is the place where we store the data in structure or in organised manner 


	Why do we require maven project vehicle working the jdbc 
It provides several adavanteages like 
Dependency management (prom.xml)
	Maven will automatically download an include required dependencies ensuring that project has necessary libraries and build time

CONSISTENT PROJECT 
	MAVEN follows standard project structure making it easier to organise the code.it prompts the separation of source code,resources and configuration filles
Allowing it for better code separation,mentanabliity and collaboration within the team 

EASY PROJECT SETUP:
Maven provides arche types(architecture types ) templates which are predefine project templates for difference dtype of application  

Dependency version management:
Continue integreatio 
Standardise project life cycle 

Maving naming convention 
Group id
	(reverse domain name)gid identifies the group of orgainisation who own the project it is typically writtain in reverse domain name 
Example :if org domain is example.com then gid will be com.example 

Artifact id (projecct name):
	Artifact id represents the specific project within group it is name a project which will be used to identify the project within the organisation uniquely

What is dependency
	The dependency will maintained inside “pom.xml”
In context with the maven project dependency in pom.xml file referseed to external library or modules that project relies on 

Inside pom.xml file dependencies will be define inside 
<dependencies>

</dependencies>

In OUR CASE we need to get postresql dependencies 
To get the dependencies 
	We need to serarfch for mvn 
https://get.enterprisedb.com/postgresql/postgresql-14.8-2-windows-x64.exe

```
![image](https://github.com/321999/Advance_Java/assets/73833132/8d363066-704a-443a-a906-0d3dadb7faba)


## Retrieve data from database 
* To retriever data from database we need select query
* To execute SELECT query we have dedicated method called executeQuery  and this return ResultSet object
  	* what is ResultSet /
  	  	* ResultSet is an interface which presetn in java.sql package
  	  	* It holds data and acct as a curoso or poitner for the records
  	  	* ResultSet is responsible to store the data which is coming from database
  	  	  we can getr RESEULT SET AOBJECT BY CALY EXECUTE ewuery ()
  	  	  RESULTset OBJECCT AMINAITAIN CURSER/JOINTER WHICH POINTTING TO PARTICULAR RECORD
  	  	  tHE next() is used to move cursor/poinyer to nexta position
  	  	  There are frew more mrethdos in REesultaset TPO FECH DATA FROM A PRATICULAR record
  	  	  	* ResultSet.getInt(int ColumnsetIndex)
  	  	  	* ResultSet.getInt(String columnName)
  	  	  	* 	columnIndex which is nothing but the column no. starts from 1 and goes incredasidng fromm left to righth

## JDBC 5 steps in detail 
	### step1: laod or register
 	public static Class<?> forName(String className)
                        throws ClassNotFoundException
Returns the Class object associated with the class or interface with the given string name. Invoking this method is equivalent to:
Class.forName(className, true, currentLoader)
where currentLoader denotes the defining class loader of the current class.
For example, the following code fragment returns the runtime Class descriptor for the class named java.lang.Thread:

Class t = Class.forName("java.lang.Thread")
A call to forName("X") causes the class named X to be initialized.

Parameters:
className - the fully qualified name of the desired class.
Returns:
the Class object for the class with the specified name.
Throws:
LinkageError - if the linkage fails
ExceptionInInitializerError - if the initialization provoked by this method fails
ClassNotFoundException - if the class cannot be located

#### way 2:
Register dRIVIER 
Driver driver=new Driver();
DriverManger dm=registerDrvier(driver);
public static void registerDriver(Driver driver,
                                  DriverAction da)
                           throws SQLException
Registers the given driver with the DriverManager. A newly-loaded driver class should call the method registerDriver to make itself known to the DriverManager. If the driver is currently registered, no action is taken.
Parameters:
driver - the new JDBC Driver that is to be registered with the DriverManager
da - the DriverAction implementation to be used when DriverManager#deregisterDriver is called
Throws:
SQLException - if a database access error occurs
NullPointerException - if driver is null
Since:
1.8

step2 getconnection 
connectio is an interface (it is presetn inside the java.sql package)
public static Connection getConnection(String url,
                                       String user,
                                       String password)
                                throws SQLException
Attempts to establish a connection to the given database URL. The DriverManager attempts to select an appropriate driver from the set of registered JDBC drivers.
Note: If the user or password property are also specified as part of the url, it is implementation-defined as to which value will take precedence. For maximum portability, an application should only specify a property once.

Parameters:
url - a database url of the form jdbc:subprotocol:subname
user - the database user on whose behalf the connection is being made
password - the user's password
Returns:
a connection to the URL
Throws:
SQLException - if a database access error occurs or the url is null
SQLTimeoutException - when the driver has determined that the timeout value specified by the setLoginTimeout method has been exceeded and has at least tried to cancel the current database connection attempt

## Creating connectio by single argument 
public static Connection getConnection(String url)
                                throws SQLException
Attempts to establish a connection to the given database URL. The DriverManager attempts to select an appropriate driver from the set of registered JDBC drivers.
Parameters:
url - a database url of the form jdbc:subprotocol:subname
(url?user=value&password)
* in this ? is called separator and & is called to add the value 
Returns:
a connection to the URL
Throws:
SQLException - if a database access error occurs or the url is null
SQLTimeoutException - when the driver has determined that the timeout value specified by the setLoginTimeout method has been exceeded and has at least tried to cancel the current database connection attempt

## create a connectio by using two parameter

public static Connection getConnection(String url,
                                       Properties info)
                                throws SQLException
Attempts to establish a connection to the given database URL. The DriverManager attempts to select an appropriate driver from the set of registered JDBC drivers.
Note: If a property is specified as part of the url and is also specified in the Properties object, it is implementation-defined as to which value will take precedence. For maximum portability, an application should only specify a property once.

Parameters:
url - a database url of the form jdbc:subprotocol:subname
info - a list of arbitrary string tag/value pairs as connection arguments; normally at least a "user" and "password" property should be included
Returns:
a Connection to the URL
Throws:
SQLException - if a database access error occurs or the url is null
SQLTimeoutException - when the driver has determined that the timeout value specified by the setLoginTimeout method has been exceeded and has at least tried to cancel the current database connection attempt

## step 3:
creation of statement 
mainly we will be using statement for static queries 
note : we can create dynamic queries with the help of statement but it comes with its own complexation thats why it is not recommmeded to create dynacmic queries usinng createstatement 
tatement createStatement()
                   throws SQLException
Creates a Statement object for sending SQL statements to the database. SQL statements without parameters are normally executed using Statement objects. If the same SQL statement is executed many times, it may be more efficient to use a PreparedStatement object.


Returns:
a new default Statement object
Throws:
SQLException - if a database access error occurs or this method is called on a closed connection


Transition from statement to prepared statement 
** PERFORMANCE 
	prepare statement are precompile on database server which means sql statement is passed and optimised and passed once this result through performance specially for sql queries that rer executed multiple times with differernt parameters
 Database server can reuse the execcutio plan for precompiled statement reducing the overhead(load).

 ** Readability and maintainability 
 Prepared statement queries are more readable and mantainable compared to concatenated queries 
 This makes separation between java code and sql queries withing java application
 this application also reduces the risk of syntax sql 	



 ```
package createstatment;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.SQLException;

public class usingSingleStatement {
public static void main(String[] args) {
	
	try {
		Class.forName("org.postgresql.Driver");
		
//		get connectio 
		
			Connection connection = DriverManager.getConnection("jdbc:postgresql://localhost:5432/student?user=postgres&password=root");
		
//			connection.createStatement()//static
			String query="INSERT INTO SR VALUES(?,?,?);";//? IS CALLED DELIMETER
			
			PreparedStatement preparestatement = connection.prepareStatement(query);
			
			preparestatement.setInt(1, 5);
			preparestatement.setString(2,"krishna");
			preparestatement.setInt(3,124123);
			preparestatement.execute();
	} catch (SQLException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		 catch (ClassNotFoundException e) {
		// TODO Auto-generated catch block
		e.printStackTrace();
	}
	
	
	
	
}
}


```
