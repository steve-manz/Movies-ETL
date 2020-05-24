# Movies-ETL
---

# •	Module 8 Challenge:
## o	Create an automated ETL pipeline.
## o	Extract data from multiple sources.
## o	Clean and transform the data automatically using Pandas and regular expressions.
## o	Load new data into PostgreSQL.
---
# •	The challenge is to extract and clean data from three files:
## o	“wikipedia_movies.json”
## o	two csv files downloaded from the Kaggle website, “kaggle_metadata.csv” and “ratings.csv “  
---
# •	In anticipation of merging the three files, we developed several functions to clean the “wikipedia_movies” data:
## o	Eliminate unnecessary columns (e,g., languages) to 21
## o	Change the columns names 
## o	Remove duplicate rows  
## o	Cleaned the data in several columns with inconsistent formats:
### 	Box Office Data converted to a $xxx million/billion format
### 	Budget Data converted to a  $xxx million/billion format
### 	Release Dates to Month Day Year format
### 	Running Time to a xxx mins format
---
# •	Cleaned the data in “kaggle_metadata_df”
## o	The file has 26 million rows
## o	In order to efficiently merge with the “wiki_movies_df” we reduced the number of columns to four 
---
# •	Cleaned the data in the “ratings_df”
## o	Updated the timestamp to year-month-date hour:minutes:seconds format
## o	Analyzed the average rating and determined that the average rating is 3.52
---
# •	 Began merging the files:
## o	“wiki_movies_df” and the “kaggle_metadata_df” into a new data_frame using the movie id column (i.e., imdb_id) called “movies_df”
### 	There were 7 duplicate columns in “movies_df”, and developed a series of functions 
### 	Dropped four “wiki_movies_df” columns and 
### 	Change the data in three other “wiki_movies” with zeros
### 	As a result, we kept 15 columns and renamed them 
## o	Merged the “movies_df” with “ ratings_df” into a new data_frame called “movies_rating_counts_df” using the kaggle_id column (formerly called  movie_id
---
## •	 Uploaded the “clean” data in a new table in SQL called “movie_data”

