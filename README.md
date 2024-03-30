# Intro
The following is a dataset with a mix of continous and lyrical variables of songs, their lyrical features, and their lyrical content from the following paper (https://data.mendeley.com/datasets/3t9vbwxgr5/3). The data spans 1950 - 2019.

## Exploratory Data Analysis
I began exploring this dataset by generating barplots of the categorical columns "genre" and "topic". This revealed that the most popular genres were pop and country and the least popular were reggae and hip hop, respectively. The most popular topics were sadness and violence and the least popular topics were romantic and feelings, respectively. 

Then I generated histograms for the remaining numeric columns which revealed that mode of the data was strongly right skewed. The two exceptions to this were the histograms for "release_date" and "age". Both of these distributions showed that less songs were released 1950-1960 and more were released 2010-2020. Number of releases peaked between 1974-76, 1996-98, and 2017-19 with 2017-19 seeing the greatest number of releases with ~1750.

For bivariate analysis, I generated scatter plots attempting to identify relationships between columns I thought might have a relationship such as dating vs. romatic, violence vs. obscene, etc. -- the only pattern I noticed was that many hip hop songs score high in "obscene" and moderately in "violence". Hip hop songs also consistently scored low in "romance" and "dating". When I generated boxplots I noticed that reggae adn hip hop songs were among the longest in terms of length. Hip hop songs were also amongst the most recently released compared to country songs which were among the oldest. Hip hop songs ranked highest in obscenity.

For multivariate analysis, I generated a correlation heat map which showed that the strongest linear relationship existed between oscenity and length. There was a perfect negative relationship between "release_date" and "age" which made sense as both columns represented similar data in differnt ways.

## Data Cleaning, Pre-processing, & Dimensionality Reduction

As revealed in the process of EDA, this dataset had no null values.

I chose to drop the 'Unnamed: 0' column because it was an identifier and provided no predicitve insights. I also dropped 'artist_name' and 'track_name' because they contained qualitative data and I decided to prioritize numeric data for the purpose of the model. Finally, I dropped the 'age' column because it's values expressed how “old” a song was on a scale from 0 to 1 and I felt that data was more accurately captured by the "release_date" column -- these columns also had a perfectly negative linear relationship.

I renamed the "shake the audience" column to "shake_the_audience" to avoid potential syntax errors.