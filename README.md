# IS211_FinalProject

Book Tracker is a Python Flask web application (also hosted on PythonAnywhere at (http://kathybootsrisps.pythonanywhere.com/).

The web application has several features:
Individual User Logins: Visitors can visit the site and create their own log-in. A dummy account is as follows:
  Username: kat@kat.com
  Password: katkat
  
Already Read booklist: Books you added to the booklist and already read

Net Yet Read booklist: Books you added to the booklist but did not read

Favorites booklist: Books that are marked favorite (regardless if read or not read, they just have to be on your booklist)

Search: Search first returned value by searching for keywords or ISBNs

Clear Your List: Clear your entire booklist

Books can be added and deleted individually from the Already Read or Net Yet Read booklist.

The SQL database is a PostgreSQL database. Any changes to the database (usernames, booklists, etc.) use GET and POST. There are three different databases:
-Login table to track users and validate credentials
-Booklist to store books with tags if they have been read, marked as favorite and tagged to the user to only appear in the specific user's login
-Search-log to store all historical searches and to retrieve the last search credentials to be added to the booklist (if it matches the user)

The Search portion uses the Google Book API and uses only the keyword or the ISBN URL to search for the book. The HTML then uses parsed JSON returned metadata to create the description and populate a thumbnail of the first search. 

Extra-Credit Items:
1. Extend the application to support multiple users
2. Save and populate links to thumbnails
4. Allow searching by title: Figure out how to use the Google API to search by title.

Requirement 2A:
a. For extra credit, you can host your project on PythonAnywhere
