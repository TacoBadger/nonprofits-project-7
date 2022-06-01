# Netflix Dataset

![](https://github.com/TacoBadger/NetflixDataset/blob/main/dataset.png?raw=true)

# Analysis of the Netflix Top 10 Dataset in Kaggle.

Worked with the dataset to find the Top titles on Netflix in US from 2020-04-01 to 2022-03-11. The dataset is a public dataset made available through Prasert Kanawattanachai on Kaggle. Please do take note that this document is for practice purposes only and it does not include any marketing of the titles involved.

## Authors
- [@TacoBadger](https://github.com/TacoBadger)

## Table of Contents

  - [What I want to find out?](#what-i-want-to-find-out-?)
  - [Data Source](#dataset)
  - [Methods](#methods)
  - [Language or Platform Used](#language-or-platform-used)
  - [Visual Results](#visual-results)
  - [Key Findings](#key-findings)
  - [Explore my Kaggle Notebook](#explore-the-notebook)
 

## What I want to find out?
- Number of titles
- Top ten titles
- Top ten least titles
- How many of them were Netflix Exclusive and Not
- Most watched type
- Top ten TV Shows
- Top ten Movies
- Top six Stand-Up Comedy

The time frame of the data is from 2020-04-01 to 2022-03-11. The dataset is a public dataset made available through Prasert Kanawattanachai on Kaggle.

## Dataset
- [Kaggle Netflix Top 10](https://www.kaggle.com/datasets/prasertk/netflix-daily-top-10-in-us)

It includes:
-  As Of: the snapshot date for each datapoint.
- Rank: A 1-10 scale representing the streaming time of each show for a given date.
- Year to Date Rank: A 1-10 scale representing the overall rank relative to all other shows that year (these rankings shift around quite a lot as this is recalculated by the day).
- Last Week Rank: A 1-10 scale showing the overall rank for the prior week.
- Title: The name of the show or special in question.
- Netflix Exclusive: Whether the show is a Netflix exclusive.
- Netflix Release Date: The date which the show debuted on Netflix
- Days in Top 10: How many total days a show has appeared in the Top 10 by the As Of date.
- Viewership Score: This statistic was reworked in late 2021 and was not used in the analysis.

## Methods
- Ask - Ask effective questions
- Prepare - Verify data's integrity, Check data credibility and reliability, Check data types and Merge datasets
- Process - Clean, Remove and Transform data and Document cleaning processes and results
- Analyze - Identify patterns and  Draw conclusions
- Share - Create effective visuals
- Act - Answer your questions and solve problems

# ASK

We took a look at the raw data set mentioned and come up with the questions I want to answer. This can be your own questions based on your interest about the data.

Questions:
- How many titles are there in the dataset?
- What is the top 10 titles in the whole dataset?
- What is the top 10 least titles in the whole dataset?
- How many of them are Netflix Exclusive and not?
- What is the most watched type?
- What is the top 10 TV Shows?
- What is the top 10 Movies?
- What is the top 6 Stand-Up Comedy?

# PREPARE

We downloaded the data in a zip file and uploaded it in directly to RStudio Cloud or you can use this code to import the dataset. Make sure to install and load the readr package in RStudio. You can always take a look in our [Netflix Dataset](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/netflix-dataset.ipynb) 

```
netflix_data <- read_csv("netflix daily top 10.csv")
View(netflix_data)
```

## Language or Platform Used
- [RStudio Cloud](https://rstudio.cloud/)

## Visual Results

![Top 10 Titles](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/Top%2010%20Titles.png?raw=true)

![Top 10 Least Titles](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/Top%2010%20Least%20Titles.png?raw=true)

![Total number of Types in Netflix](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/Type%20Count.png?raw=true)

![Total number of Production](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/Production%20Count.png?raw=true)

![Top 10 TV Shows](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/Top%2010%20TV%20Shows.png?raw=true)

![Top 10 Movies](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/Top%2010%20Movies.png?raw=true)

![Top 6 Stand-Up Comedies](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/Top%206%20Stand-up%20Comedy.png?raw=true)

## Key Findings
1. There are 595 titles.
2. Cocomelon had the highest number of days during the pandemic. All other titles on the top 10 titles had way less number of days than Cocomelon.
3. 377 of the titles are Netflix exclusive.
4. Movie is the most watched type.
5. The top 10 Tv shows were Cocomelon, Manifest, Queen's Gambit, Outer banks, Squid game, All American, Bridgerton, Cobra Kai, Lucifer and Virgin River
6. Top 10 Movies were The Mitchell vs. The machines, How the grinch stole christmas, Vivo, 365 days, Illumination presents the grinch. The Christmas Chronicles 2, We can be heroes, Red notice, The Unforgivable and Home
7. Top 6 Stand-Up Comedy were Dave Chappelle: The Closer, Kevin Hartz: Zero fucks given, George Lopez: We'll do it for half, Chris D'elia: No Pain, Bo Burnham: Inside

## Explore the Notebook
You can copy and edit the notebook to explore your own analysis of the data.
- [Notebook](https://www.kaggle.com/code/cryptocosy/netflix-dataset)
