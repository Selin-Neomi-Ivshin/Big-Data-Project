
# Web Application Backend Project
---

This project involves building the backend of a web application using Java with MongoDB as the database. 
The development environment is Eclipse IDE with Apache Tomcat as the application server.

---

## Project Structure:  
- **Controllers and Core Files:**
  - `RegistrationController.java`: Manages user registration and authentication.
  - `ItemsController.java`: Handles media item storage and retrieval.
  - `HistoryController.java`: Manages user interaction history.
  - `MediaItems.java`: Represents media item objects.
  - `HistoryPair.java`: Represents a user’s interaction with a media item.

---

## Functions Overview:

### _RegistrationController_
1. **`isExistUser()`**  
   - Checks if a specific username exists in the database.

2. **`validateUser()`**  
   - Verifies that the provided username and password combination matches a stored entry.

3. **`registerNewUser()`** 
   - Registers a new user if the username is not already taken.

4. **`getNumberOfRegisteredUsers()`**   
   - Retrieves the number of users registered in the past `n` days.

5. **`getAllUsers()`** 
   - Fetches all users from the database.

### _HistoryController_
1. **`insertToHistory()`** 
   - Adds a new interaction entry (username, title, timestamp) to the system.

2. **`getHistoryByUser()`** 
   - Retrieves the viewing history of a user, sorted by time in descending order.

3. **`getHistoryByItems()`** 
   - Retrieves the history of interactions with a specific item, including usernames and timestamps.

4. **`getItemsSimilarity()`**  
   - Calculates the similarity between two items using the **Jaccard similarity** formula.


### _ItemsController_
1. **`fillMediaItems()`** 
    - Copies media item data from an SQL database into MongoDB storage.

2. **`fillMediaItemsFromUrl()`**  
    - Populates media items from a remote file via URL.

3. **`getTopNItems()`** 
    - Retrieves the top `N` media items from the database.

---

## Setup Instructions:

### Prerequisites
1. **Eclipse IDE for Enterprise Java and Web Developers**  
   [Download Eclipse](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2023-03/R/eclipse-inst-jre-win64.exe).

2. **Apache Tomcat**  
   [Download Tomcat](http://tomcat.apache.org/). Ensure compatibility with your OS, Java version, and Eclipse.

3. **MongoDB Server**  
   Set up MongoDB locally or ensure access to a running MongoDB server.

---

## Usage:
- **Registration**: Add new users and authenticate them using the `RegistrationController`.
- **Media Items**: Populate and retrieve media items using `ItemsController`.
- **History Management**: Track and query user interaction history with the `HistoryController`.

---

