# Movies-ETL

# Write an ETL Function to Read Three Data Files
For this deliverable, the data from three files needed to be extracted from three differenet files. This was accomplished by creating a function.
The Function will do the following:
Extract the data one the appropiate inputs were given.
Converts the Kaggle metadata file to a Pandas DataFrame
Convert the Wikipedia JSON file to a pandas data frame. 
Converts the MovieLens ratings data file to a Pandas DataFrame
![Function](https://user-images.githubusercontent.com/104809098/185823708-b076f5b6-bd87-4484-a808-a62cea72e07b.png)

# Extract and Transform the Wikipedia Data
The first step for this deliverable is to filter out the TV shows and create a new dataframe.
![Clean movie](https://user-images.githubusercontent.com/104809098/185824425-a80a1646-d7d4-4518-9040-c1d199cf9e36.png)

The second function will use a try-except function to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.
![except](https://user-images.githubusercontent.com/104809098/185824659-c43a9b42-0434-4174-ad61-5c40dd4c2133.png)

The extraction and transformation of the Wikipedia data in the ETL function will do the following:
A list comprehension is used to keep columns with non-null values.
The non-null box office data is converted to string values using the lambda and join functions.
A regular expression is used to match the six elements of "form_one" of the box office data. 
A regular expression is used to match the three elements of "form_two" of the box office data. 
![except2](https://user-images.githubusercontent.com/104809098/185824975-0ebcf5d3-fb8b-4e48-acf4-8e5a8dbcb5cd.png)
![except3](https://user-images.githubusercontent.com/104809098/185824983-4a357e62-53a2-4cd3-b180-b2e122b0ddca.png)

# Extract and Transform the Kaggle Data

The extraction and transformation of the Kaggle metadata using the ETL function does the following:
The Kaggle metadata is cleaned. 
The Wikipedia and Kaggle DataFrames are merged. 
![kaggle](https://user-images.githubusercontent.com/104809098/185825501-9c78b104-63cd-4a1e-b0c4-98c34750acbe.png)
![kaggle2](https://user-images.githubusercontent.com/104809098/185825455-3f39d298-ae27-4b2e-a1d1-142f81e71f5d.png)


The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df: 
Unnecessary columns are dropped.
A function is used to fill in the missing Kaggle data.
The movies_df DataFrame is filtered to keep specific columns.
The movies_df DataFrame columns are renamed.
![kaggle3](https://user-images.githubusercontent.com/104809098/185825873-73d36432-1530-40d4-9c5a-c09b09c2e535.png)

The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
The ratings counts are cleaned. 
The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame. 
The empty values in the movies_with_ratings_df DataFrame are filled with “0”.  
![kaggle4](https://user-images.githubusercontent.com/104809098/185825981-e4256b44-7c0f-481b-9e02-3c0cb139bb4e.png)




