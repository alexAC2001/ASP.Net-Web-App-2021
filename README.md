# ASP.Net-Web-App-2021
This is a Bible web application created in ASP.Net using Visual Studio. The application was written in C# and HTML. The user is able to view the all the verses from the Bible.

# Home Page
Here is the root page of the Bible application. The user can perform certain actions in the navigation bar at the top of the page.

![image](https://user-images.githubusercontent.com/62003762/174076548-c2ba18c3-c475-456e-9d3a-ca922814b0d6.png)

# Bible Verses
All verses from the Bible are stored in SQL Server and can be accessed by the user. Each verse is presented with its verse number, chapter number, and book number.

![image](https://user-images.githubusercontent.com/62003762/174077858-97f66ae1-665b-4f60-96d9-222f23a1a248.png)

# Create New Verse
The user can also add new verses. This was implemented to show that data can be inserted into the SQL Server database.

![image](https://user-images.githubusercontent.com/62003762/174079410-0dde861e-cdf2-4c6b-9607-397a7c1a0976.png)

# Search
This allows the user to search for specific verses with key words.

![image](https://user-images.githubusercontent.com/62003762/174078551-c38b35e0-1677-4a61-a6a0-12342fed60c1.png)

After inputting 'in the beginning', Bible verses that contained this search term were displayed in a table.

![image](https://user-images.githubusercontent.com/62003762/174079250-f1e141d5-f676-4303-a03d-2f509846fee7.png)

# Dependency Injection
Here is an example of Dependency Injection in one of the controller classes. IBibleDataService is set as a parameter as dataService. It was then set equal to repository.

![image](https://user-images.githubusercontent.com/62003762/174082921-b94e8faa-1ad1-4972-a8f4-4df01e966571.png)

# Data Access Object
BibleVerseDAO was the data access object class used to implement methods that persisted data to and from the SQL Server database. Here is code snippet within the GetAllVerses() method. This contains a select SQL statement to access the database table, dbo.t_asv. The SQL connection is opened so the SqlDataReader class can read the select statement.

![image](https://user-images.githubusercontent.com/62003762/174087576-b83a3266-9145-45e8-ae71-3f9c860ea25a.png)

# Logging
A class, MyLogger, was created to implement methods from an interface, ILogger. This allows the application to effectively log data.

![image](https://user-images.githubusercontent.com/62003762/174082174-54694e68-a9af-4f19-836c-f224f0989aec.png)

Whenever the user performs an action, such as viewing all verses or creating a new verse, it is logged to an external text document.

![image](https://user-images.githubusercontent.com/62003762/174081952-892fa030-8bfb-4ad5-a137-de97aab7571c.png)
