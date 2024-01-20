
# Callprep Backend Assigment

## Note
- ### Use any of the backend libraries you are comfortable with (django, flask, node etc.)
- ### Deadline is 11 PM, January 21, 2024
- ### Use any Database you are comfortable with (default database files that comes with some technologies are also sufficient)

## Part 1
### Create two POST endpoints to accept data in the specified formats.
```
#FIRST ENDPOINT
{
    "name": "",
    "age": "",
    "gender": "",
    "marks": {
        "physics": [obtained_marks, total_marks],
        "chemistry": [obtained_marks, total_marks],
        "maths": [obtained_marks, total_marks]
    }
}
==========================================================
#SECOND ENDPOINT
{
{
    "first_name": "",
    "last_name": "",
    "years_old": "",
    "scores": {
        "subjects": ["physics", "chemistry", "maths"],
        "marks_obtained": [In order of subjects array],
        "total_marks": [In order of subjects array]
    }
}
```
### -   Implement a GET endpoint to retrieve all student records with their calculated percentages, formatted as:
```
#A singular format of get endpint
{
    "name": "",  
    "age": "", 
    "gender": "",
    "physics_percentage": float,
    "chemistry_percentage": float,
    "maths_percentage": float,
    "overall_percentage": float
}
```

### Data Validation Rules:
**1. Mandatory Fields:**
-   **For both endpoints:**
    -   `name` (or `first_name` and `last_name`)
    -   `age` (or `years_old`)
    -   `gender`
    
-   **For subjects:**
    -   `physics` and `maths` are mandatory.
    -   `chemistry` is optional
 
**2. Marks Validation:**

-   Obtained marks must be non-negative integers.
-   Total marks must be positive integers.
-   Obtained marks cannot exceed total marks.


## Part 2: Database Schema Design

**Task:**

-   Design a database schema that effectively stores student records, marks, and calculated percentages, ensuring extensibility for future requirements.
-   Create a draw.io diagram visually representing the schema, including tables, columns, data types, and relationships.

**Considerations:**

-   **Normalization:** Normalize the schema to reduce redundancy and improve data integrity.
-   **Extensibility:** Design with future growth in mind, allowing for potential additions like:
    
    -   More subjects
    -   Additional student details 
    
-   **Average Marks and Total Score:** Decide how and where to exaclty store them 

## Part 3 (Bonus Task)
**Part 3: Data Aggregation and Storage**

**Bonus Task:**

-   Implement a GET endpoint to retrieve aggregated statistics:
    
    -   Average score of the entire class
    -   Average score for each subject
    
-   Store these calculated averages in the database for future retrieval.

**Requirements:**

2.  **Endpoint Design:**
    
    -   Create a GET endpoint to retrieve the aggregated data, formatted appropriately (e.g., JSON).
    
4.  **Database Queries:**
    
    -   Write efficient SQL queries to calculate the required averages.
    -   Consider using aggregate functions like AVG and JOINs to combine data from multiple tables.
    
6.  **Data Storage:**
    
    -   Decide how to store the calculated averages in the database.



If you have any doubts or clarifications regarding the assignment reach out to   [nikhil@callprep.io](user@example.com)
