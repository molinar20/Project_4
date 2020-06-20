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


2.  I decided to use 2NF for this first table. This would make it so that the name is the prime attribute. This also allows the data to be fully transitive as the name is dependent on the total. Additionally, the original table is already in 1NF. The second table is 1NF since the data does not directly rate to a primary key but they all are still supportive of each other.

Table #1: Relationship between name and total

| Column Header    | Data types           |  Foreign Keys           |
| ---------------- |:--------------------:| -----------------------:|
| rank_id          | Character / VARCHAR| Would be primary key    |
| Name             | Character / VARCHAR  | Would be primary key    |
| Total            | Numeric / INTEGER    | Is used. "Total"        |

Table #2: Relationship between female and male ratio and name 

| Column Header    | Data types           | Keys?                   |
| ---------------- |:--------------------:| -----------------------:|
| name             | Character /VARCHAR   | No.                     |
| male_ratio       | Numeric / REAL       | No.                     |
| female_ratio     | Numeric / REAL       | No.                     |


Problems 3 and 4 are located in their appropriate files and were used with sqlite and MS word for some text editing from a column extraction

EXTRA CREDIT

This is another dataset available [here](https://github.com/fivethirtyeight/data/blob/master/bad-drivers/bad-drivers.csv) and it lists the statistics of drivers involved in a collion per one billion miles by state. The Information presented in the table came from the National Highway Traffic Safety Administration 2010-2012. All of the headings are descriptive in their  provided heading and use consist of the following: 

State	N/A
Number of drivers involved in fatal collisions per billion miles	
Percentage Of Drivers Involved In Fatal Collisions Who Were Speeding	
Percentage Of Drivers Involved In Fatal Collisions Who Were Alcohol-Impaired	
Percentage Of Drivers Involved In Fatal Collisions Who Were Not Distracted	
Percentage Of Drivers Involved In Fatal Collisions Who Had Not Been Involved In Any Previous Accidents	
Car Insurance Premiums ($)	(Provided by National Association of Insurance Commissioners 2011)
Losses incurred by insurance companies for collisions per insured driver ($)	Provided by National Association of Insuarance Commissioners 2010)

In this dataset I would use more tables to normalize the data featured here. One table would focus on purely fatal collions from the first five columns while another table would focus on fatal collisions per billion miles and compare the car insurance premioms and losses incurred. Other tables could focus on total number of drivers in a fatal collion and compare that with only the alcohol-impaired percentage value. Many relations could be drawn with merely just fatal collions per billion miles and the losses incurred. These tables would most likely be in a basic normal form of 1NF, perhaps using a rank system as seen in the other table used to sort the states with the highest number of fatal collions. 
