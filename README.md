# Customer Churn Database Project

This project demonstrates the process of creating, managing, and querying a database for customer churn analysis. The project is divided into two primary stages: *Database Creation and Management* and *Website Development*.

---

## 1. *Database Creation and Management*

### Step 1.1: Database Design
- The data for customer churn was organized into multiple logical tables based on its structure and relationships.
- Tables were created to handle various aspects of the data (e.g., customer details, subscription plans, churn status, etc.).
  
### Step 1.2: Writing SQL Scripts
Two SQL files were created to streamline the database setup:
- **create.sql**: 
  - Contains SQL commands for defining the schema and creating the necessary tables in the SQLite database.
  - Ensures all the tables are created with proper constraints and data types.

- **load.sql**: 
  - Contains SQL commands for populating the tables with data.
  - Includes INSERT statements for adding records to the tables.

### Step 1.3: Loading Data into the Database
- The SQLite database file (customer_churn_db.db) was initialized and populated by executing the create.sql and load.sql scripts using a database management tool or directly via SQLite.

---

## 2. *Website Development*

### Step 2.1: Setting Up the Project
- A *Streamlit* application was developed to provide a user-friendly interface for interacting with the database.
- The database file customer_churn_db.db was included in the project directory to allow direct access by the app.

### Step 2.2: Developing the Streamlit App
Key features of the app:
- *Display Available Tables:*
  - The app queries the database to list all the available tables using the query: 
    sql
    SELECT name FROM sqlite_master WHERE type='table';
    
  - Users can click on a table name to view its contents.

- *Custom SQL Query Execution:*
  - Users can input any valid SQL query in a text area, and the app executes the query, displaying the results.

### Step 2.3: Testing and Debugging
- Verified database connectivity and query execution.
- Ensured that the app handles errors gracefully, including missing files, invalid queries, or database-related issues.

---

## 3. *How to Run the Project*

### Prerequisites
- Python 3.x installed on your machine.
- Streamlit installed via:
  ```bash
  pip install streamlit
