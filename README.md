# Project_4_CompTools

1. METADATA

Information was taken from [this github page](https://github.com/fivethirtyeight/data/tree/master/unisex-names) which is featured in [this article](https://fivethirtyeight.com/features/there-are-922-unisex-names-in-america-is-yours-one-of-them/). The table used in this project lists the most common unisex names in the United States and shares the total amount of occurences and the percentage of the two sexes with listed name. 

| Column Header    | Description                                                              | 
| ---------------- |:-------------------------------------------------------------------------| 
| name             | Unisex names taken from Social Security Administration                   | 
| total            |    Total number of individuals with specific unisex name                 | 
| male_share       | Ratio of men with unisex name                                            | 
| female_share     | Ratio of women with unisex name                                          |
| gap              | Size of gap in data comparing male and women with specific intersex name |


2.  I decided to use 2nd normalized form for this first table. This would make it so that the name is the prime attribute. This also allows the data to be fully transitive as the name is dependent on the total. Additionally, the original table is already in 1NF.

Table #1: Relationship between name and total

| Column Header    | Data types           |  Foreign Keys           |
| ---------------- |:--------------------:| -----------------------:|
| Name             | Character            | Would be primary key    |
| Total            | Numeric              | Is used. "Total"        |

Table #2: Relationship between female and male ratio and name 

| Name             | Character            | Would be primary key    |
| ---------------- |:--------------------:| -----------------------:|
| Male Ratio       | Numeric              | Is used. "male_share"   |
| Female Ratio     | Numeric              | Is used. "female_share" |


3. Code for creating tables

  CREATE TABLE TOTALNAMES
  (rank_id INTEGER PRIMARY KEY AUTOINCREMENT,
   name VARCHAR(255) NOT NULL,
   total VARCHAR(255)
   );
   
   CREATE TABLE NAMESEXRATIO
   (name VARCHAR(255) NOT NULL,
   male_ratio REAL,
   female_ratio REAL
   );
   
   4 
