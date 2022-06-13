# Objective of code:
    This code converts textual data into numerical vectors, stores the numerical data into database and converts the 
    numerical data back to normal text upon fetching from database.

## Libraries Used

#### 1. sqlite3: 
                    A library used to create and manage database and tables. 

#### 1. time: 
                    A library used to manage and handel time and date related problems. 

## Database Structure

### Database name:  vectorized.db
Contains 1 table with 1 column:
                                         
                                        vectors   

                               |        vector   | 
                               |-----------------|
                               |        TEXT     |        
                               | (contains list) |   

## User defined functions:
1. create_table: Create a table named **vectors**.
2. delete_table: Delete the table.
3. convert_to_numbers: Take the raw list of strings and converts the string to a list of numbers for each string by 
   using in-built function ord() 
4. convert_to_string: Take the numbers list and convert them back to words using inbuilt function chr() and returns the 
   original string after joining using .join function 
5. insert: To insert multiple items into database using executemany.
6. fetch: To fetch all the data from database.
7. search: Takes a string to be searched in the database, converts it to numbers and run a search throughout the table 
   in database for matching items and return the data in string form after converting the numbers back to original 
   string along with its row id

## Working of Code
This code takes the batch of strings as inputs and convert them into numeric form, then store the list of numbers 
into **_vectors_** table in database named **_vectorized.db_** 
The fetch function fetches and print all the items from the **_vectors_** table and decode them back to their original string.
The search function takes argument that user needs to search in the database, converts it to numbers and run a search 
throughout the table in database for matching items and return the data in string form after converting the numbers 
back to original string along with its row id