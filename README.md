# Movies-ETL
## Project Overview
Amazing Prime loves the dataset and wants to keep it updated on a daily basis. In this project create an automated pipeline that takes in new data, from Wikipedia data, Kaggle metadata and the MovieLens rating data. And performs the appropriate transformations, and loads the data into existing PostgreSQL database. For this project analysis we performed following steps:
1. Write an ETL function to read three data files
2. Extract and transform the Wikipedia data
3. Extract and transform the Kaggle and rating data
4. Load the data to a PostgreSQL Movie Database

## Resources

Python CSV Files:

ratings.csv

movies_metadata.csv

JSON Files:

wikipedia-movies.json

## Results

- By using Python, Pandas, the ETL process, and code refactoring, created three separate DataFrames.

![2022-02-27 (4)](https://user-images.githubusercontent.com/96403349/155922974-a2b5c749-dc0d-442c-8fbc-7005407a70e4.png)

![2022-02-27 (5)](https://user-images.githubusercontent.com/96403349/155923068-3be2f6d7-0733-4dd1-a8ac-0e810e242ac6.png)

![2022-02-27 (6)](https://user-images.githubusercontent.com/96403349/155923126-23530067-7c7e-46e1-8bd9-e9f8db730627.png)


- Extract and transform the Wikipedia data to merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.

![2022-02-27 (8)](https://user-images.githubusercontent.com/96403349/155923279-116fdaca-0280-4c35-b6d5-708424f1971a.png)


- Again removed the duplicates, formatted and grouped the data. The Kaggle and rating data were then merged with the Wikipedia movies DataFrame.

![2022-02-27 (9)](https://user-images.githubusercontent.com/96403349/155923418-458dc48b-79e4-4da3-be2a-494db3bf9af3.png)

- Loaded the data to PostgreSQL movies Database and confirmed that the movies table has 6,052 rows and the ratings table has 26,024,289 rows.

![2022-02-27 (10)](https://user-images.githubusercontent.com/96403349/155923635-e142627b-8765-4afb-ab42-4b21ccbd9899.png)


![movies_query](https://user-images.githubusercontent.com/96403349/155922498-dd5effd6-237c-4df6-8d03-a598bc7675ba.png)


 
 ![ratings_query](https://user-images.githubusercontent.com/96403349/155922521-1fbd1cec-3bea-403a-9e1d-c167cb8c06df.png)



