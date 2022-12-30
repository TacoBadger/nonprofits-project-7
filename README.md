# Nonprofit Dataset (Project 7)

![](https://github.com/TacoBadger/NetflixDataset/blob/main/dataset.png?raw=true)

# Introduction

Lately I have been very interested in how Power Bi pecifically can help nonprofits. With Power Bi, you can gain insights into your operations and performance, and make data-driven decisions that can help you achieve your mission and goals. I can think of 4 main ways nonprofits can use Power Bi analysises:

Donor analysis: Power BI can be used to analyze donor data, such as donation amounts, frequency, and sources, to better understand donor behavior and identify trends. This can help charities target their fundraising efforts more effectively and improve donor retention.

Program effectiveness: Charities can use Power BI to track and monitor the effectiveness of their programs and initiatives, such as the number of people served, the impact of the program, and the resources required. This can help charities allocate resources more efficiently and optimize program design.

Financial analysis: Power BI can be used to analyze financial data, such as revenue, expenses, and fundraising performance, to identify trends and areas for improvement. This can help charities manage their finances more effectively and make informed decisions about budgeting and resource allocation.

Impact reporting: Charities can use Power BI to create interactive dashboards and reports that showcase the impact of their work and communicate it to stakeholders. This can help charities demonstrate the value of their work to donors, volunteers, and the public.

In this case study, I will limit the scope to a donor analysis. I made fictive non-profit called The Be Happy Foundation, and I also made a dataset of fictive donors.

Please do take note that this document is for practice purposes only and it does not include any marketing of the titles involved.

## Authors
- [@TacoBadger](https://github.com/TacoBadger)

## Table of Contents

  - [What I want to find out?](#what-i-want-to-find-out)
  - [Data Source](#dataset)
  - [Methods](#methods)
  - [Language or Platform Used](#language-or-platform-used)
  - [Visual Results](#visual-results)
  - [Key Findings](#key-findings)
  - [Explore my Kaggle Notebook](#explore-the-notebook)
  - [What is next?](#what-is-next)
 

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
- [Ask](#ask) - Ask effective questions
- [Prepare](#prepare) - Verify data's integrity, Check data credibility and reliability, Check data types and Merge datasets
- [Process](#process) - Clean, Remove and Transform data and Document cleaning processes and results
- [Analyze](#analyze) - Identify patterns and  Draw conclusions
- [Share](#visual-results) - Create effective visuals
- [Act](#key-findings) - Answer your questions and solve problems

## ASK
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

## PREPARE
We downloaded the data in a zip file and uploaded it in directly to RStudio Cloud or you can use this code to import the dataset. Make sure to install and load the readr package in RStudio. You can always take a look in our [Netflix Dataset](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/netflix-dataset.ipynb) whenever you need help with a line.

```
netflix_data <- read_csv("netflix daily top 10.csv")
View(netflix_data)
```

## PROCESS
In this step we took our time to process and clean our data. Here a sample of our cleaning process which involves changing the column names to lower case and changing all the NA values to Others.

```
netflix_data <- netflix_data %>% rename_with(tolower) %>% 
  rename(date = "as of", 
         year_to_date_rank = "year to date rank",
         last_week_rank = "last week rank",
         production = "netflix exclusive",
         netflix_release_date = "netflix release date",
         days_in_top_10 = "days in top 10",
         viewership_score = "viewership score")


View(netflix_data)

#replace NA values in production column to "others"
netflix_data <- netflix_data %<>% mutate(production = fct_explicit_na(production, na_level = "Others")) 
View(netflix_data)
```

We also took time to clean out all the spelling mistakes and duplicates. You can take a look at the whole process on correcting all the spelling mistakes in [Netflix Dataset](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/netflix-dataset.ipynb) 

```
netflix_data <- mutate(netflix_data, title = recode(.x=title, "Tiger King"="Tiger King: Murder, Mayhem, and Madness"))
netflix_data <- mutate(netflix_data, title = recode(.x=title, "Tiger King: Murder, Mayhem …"="Tiger King: Murder, Mayhem, and Madness"))
netflix_data <- mutate(netflix_data, title = recode(.x=title, "Jerry Seinfeld: 23 Hours to…"="Jerry Seinfeld: 23 Hours to Kill"))
netflix_data <- mutate(netflix_data, title = recode(.x=title, "George Lopez: Weâll Do It f…"="George Lopez: We'll Do It for Half"))
netflix_data <- mutate(netflix_data, title = recode(.x=title, "The Queenâs Gambit"="The Queen's Gambit"))
```

## ANALYZE
We took a look at out cleaned data and filtered them to the data we need to answer our questions. We also made new tables that is already sorted and filtered to answer our questions. The whole process can be found in [Netflix Dataset](https://github.com/TacoBadger/NetflixDataset/blob/main/Assets/netflix-dataset.ipynb) 

```
#Number of titles
unique(netflix_data$title)

#Top 10 titles
title_count_top <- netflix_data %>% count(title) %>% rename(days_in_top_10 = n) %>%
  arrange(-days_in_top_10) %>% head(10)
View(title_count_top)
```
Top 10 Titles will show
| Title     	                | Days in top 10  	|
|-------------------	        |------------------	|
| Cocomelon                  	| 415               |
| Manifest             	      | 80	              |
| The Queen's Gambit          | 73 	              |
| Outer Banks                 | 72	              |
| Squid Game                  | 66	              |
| All American                | 58 	              |
| Bridgerton                  | 58	              |
| Cobra Kai                   | 57	              |
| Lucifer                     | 56	              |
| Virgin River                | 56	              |

```
title_count_least <- netflix_data %>% count(title) %>% rename(days_in_top_10 = n) %>%
  arrange(days_in_top_10) %>% head(10)
View(title_count_least))
```
Top 10 Least titles will show
| Title     	                | Days in top 10  	|
|-------------------	        |------------------	|
| Animals on the loose: A you vs. Wild movie                 	| 1                 |
| Are we there yet?      	    | 1	                |
| Badland                     | 1 	              |
| Christmas on the square     | 1	                |
| Dare me                     | 1                 |
| Dare me: Seaon 1            | 1	                |
| Dark                        | 1	                |
| Elves                       | 1	                |
| Grumpy Christmas            | 1                 |
| Hannibal                    | 1	                |

```
type_count <- netflix_unique %>% count(type) %>% rename(count = n)
View(type_count)
```
Type Count will show
| Type      	                | Count            	|
|-------------------	        |------------------	|
| Concert/Performance        	| 2                 |
| Movie                  	    | 2401	            |
| Stand-Up Comedy             | 41 	              |
| TV Show                     | 3995              |


```
production_count <- netflix_unique %>% count(production) %>% rename(count = n)
View(production_count)
```
Production Count will show
| Production   	              | Count            	|
|-------------------	        |------------------	|
| Netflix Exclusive         	| 4104              |
| Not Netflix Exclusive       | 2335	            |

```
tv_show <- filter(netflix_data,type=="tv show") %>% count(title) %>% rename(days_in_top_10 = n) %>%
  arrange(-days_in_top_10) %>% head(10)
View(tv_show)
```
Top 10 TV Shows will show
| Title     	                | Days in top 10  	|
|-------------------	        |------------------	|
| Cocomelon                  	| 415               |
| Manifest             	      | 80	              |
| The Queen's Gambit          | 73 	              |
| Outer Banks                 | 72	              |
| Squid Game                  | 66	              |
| All American                | 58 	              |
| Bridgerton                  | 58	              |
| Cobra Kai                   | 57	              |
| Lucifer                     | 56	              |
| Virgin River                | 56	              |

```
movies <- filter(netflix_data,type=="movie") %>% count(title) %>% rename(days_in_top_10 = n) %>%
  arrange(-days_in_top_10) %>% head(10)
View(movies)
```
Top 10 Movies will show
| Title      	                | Days in top 10    |
|-------------------	        |------------------	|
| The Mitchells vs. The Machines   	| 31                 |
| How the Grinch Stole Christmas    | 29	               |
| Vivo                        | 29  	              |
| 365 days                    | 28	                |
| Illumination presents the Grinch  | 24            |
| The Christmas Chronicles 2  | 24	                |
| We can be heroes            | 24	                |
| Red Notice                  | 23	                |
| The Unforgivable            | 22                  |
| Home                        | 21 	                |

```
comedy <- filter(netflix_data,type=="stand-up comedy") %>% count(title) %>% rename(days_in_top_10 = n) %>%
  arrange(-days_in_top_10) %>% head(10)
View(comedy)
```
Top 6 Stand-Up Comedy will show
| Title      	                | Days in top 10    |
|-------------------	        |------------------	|
| Dave Chappelle: The Closer        	| 31                  |
| Kevin Hartz: Zero fucks given       | 29	                |
| George Lopez: We'll do it for half  | 29  	              |
| Jerry Seinfeld: 23 hours to kill    | 28	                |
|  Chris D'elia: No Pain              | 24                  |
| Bo Burnham: Inside                  | 24	                |

```
concert_and_performance <- filter(netflix_data,type=="concert/performance") %>% count(title) %>% rename(days_in_top_10 = n) %>%
  arrange(-days_in_top_10) %>% head(10)
View(concert_and_performance)
```
Concert and Performance will show
| Title       	              | Days in top 10   	|
|-------------------	        |------------------	|
| Ariana Grande's Excuse me, i love you	| 2       |

## SHARE AND ACT  
Our share and act process are documented below

  - [Visual Results](#visual-results)
  - [Key Findings](#key-findings)


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
7. Top 6 Stand-Up Comedy were Dave Chappelle: The Closer, Kevin Hartz: Zero fucks given, George Lopez: We'll do it for half, Jerry Seinfeld: 23 hours to kill, Chris D'elia: No Pain, Bo Burnham: Inside

## Explore the Notebook
You can copy and edit the notebook to explore your own analysis of the data.
- [Notebook](https://www.kaggle.com/code/cryptocosy/netflix-dataset)

## What is next?
Thank you for reading my doccumentation about my Netflix Dataset. To help me improve more of my basic data analytical skills I will list down a few pointers on what's next for my other projects.

- I could have improved my data story telling or I could have made a more compelling narrative by including all detailed and relevant explanation in my documentation, I should know what my target audience is and start telling my data from there. I should also be including basic terms especially for beginners reading my documentation.
- I could have improved my keypointers that can lead the audience to understand more about my data analysis. I could have make use of highlighting all important keywords and relevant data for our target audience.
- A more detailed explanation of the codes used and functions. We can use a small summary for our target audience.
- A more effective way of using visuals where our target audience can easily understand it. Always make sure you choose the proper visual to express your dataset. 
-  We will also start using SQL for our next dataset practice which involves more functions and commands that is more complex than in RStudio. We will specifically used DB Browser SQLite for our next ptractice, DB Browser works similar to SQL in some functions and commands so let us learn about it together in the next dataset. 

See you on our next project!
