# Nonprofit Dataset (Project 7)

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/NonProfits.png?raw=true)

# Introduction

Lately I have been very interested in how Power Bi can help nonprofits. With Power Bi, you can gain insights into your operations and performance, and make data-driven decisions that can help you achieve your mission and goals. I can think of 4 main ways nonprofits can use Power Bi analysises:

Donor analysis: Power BI can be used to analyze donor data, such as donation amounts, frequency, and sources, to better understand donor behavior and identify trends. This can help charities target their fundraising efforts more effectively and improve donor retention.

Program effectiveness: Charities can use Power BI to track and monitor the effectiveness of their programs and initiatives, such as the number of people served, the impact of the program, and the resources required. This can help charities allocate resources more efficiently and optimize program design.

Financial analysis: Power BI can be used to analyze financial data, such as revenue, expenses, and fundraising performance, to identify trends and areas for improvement. This can help charities manage their finances more effectively and make informed decisions about budgeting and resource allocation.

Impact reporting: Charities can use Power BI to create interactive dashboards and reports that showcase the impact of their work and communicate it to stakeholders. This can help charities demonstrate the value of their work to donors, volunteers, and the public.

In this case study, I will limit the scope to a donor analysis. I made fictive non-profit called The Be Happy Foundation, and I also made a dataset of fictive donors.

Please do take note that this document is for practice purposes only and it does not include any marketing of the titles involved.

## Authors
- [@TacoBadger](https://github.com/TacoBadger)

## Table of Contents

  - [Dataset](#dataset)
  - [Methods](#methods)
  - [Language or Platform Used](#language-or-platform-used)
  - [Visual Results](#visual-results)
  - [Key Findings](#key-findings)
  - [Explore my Kaggle Notebook](#explore-the-notebook)
  - [What is next?](#what-is-next)
 

## Dataset
- [The Fake Be Happy Foundation Donor Data](https://github.com/TacoBadger/nonprofits-project-7/blob/main/Excel%20Nonprofits.xlsx)

This dataset consist of 100 rows of fake data, I used www.random.org to generate both names and numbers.

It includes:
- Id. This is unique identifier of each donor, from D000100 to D00199
- Donor. This is the name of the donor which comprise of both first and surname
- Anonymity. This field can be populated with Yes and No. For our example, no on of the 100 donors wanted to be anonymous.
- Regular Donation. This column is populated with regular or one-off donation. This is an important metric and KPI, as the regular donations will increase the long term sustainability of the nonprofit.
- Amount. This data is great to establish who the biggest donors are.
- Date of donations. This data goes from 2018 to 2022
- Status reason. This data shows whether the donor is an active or passive contributor.

## Methods
I used the Google Data Analytics framework. It consist of the follow 6 steps:
- [Ask](#ask) - Ask effective questions
- [Prepare](#prepare) - Verify data's integrity, Check data credibility and reliability, Check data types and Merge datasets
- [Process](#process) - Clean, Remove and Transform data and Document cleaning processes and results
- [Analyze](#analyze) - Identify patterns and  Draw conclusions
- [Share](#visual-results) - Create effective visuals
- [Act](#key-findings) - Answer your questions and solve problems

## ASK
Since I made my own mini dataset - the questions could potentially be a bit skewed towards my own interest. 

With that in mind I have 3 question.

1. I am curios whether the donation have been increaseing since 2018 and possible why?
2. I am intriqued by who the top 10 domors are and whether we can see any patterns between them?
3. I am wondering whether we fget more one-off donations or regular donations and what we can do to increase the regular donations?


## PREPARE
In this case study, we will use 2 programs Excel and Power Bi.
Firstly, I made a mini dataset of 100 rows inside excel:

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel1.png?raw=true)

Here you can see all the columns, the rows and the fields.

Later on, I used the data in the Excel to work on my power BI Dashboard.

You can download the dashboard https://github.com/TacoBadger/nonprofits-project-7/blob/main/nonprofitpowerbi.pbix or you can see how it looks like here

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power1.png?raw=true)


## PROCESS
In this step I took the time to process and clean the data in the Excel file. Purposedly, I left all the null values out. I also left out the Anonymous Data because none of them are anonomous. I also took some time to clean out all the spelling mistakes and duplicates. I did all this manually, because the dataset is relatively small, however this can also be done programmatically in everything from Excel to Python.



## ANALYZE

The first things I did in Excel was generating a table:

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel2.png?raw=true)

From there, I could generate a pivot table

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel3.png?raw=true)

In this pivot table, you can see the date of the donations and also the donor.

Now I generated a graph to get a better overview.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel4.png?raw=true)

All the Excel based table and graphs did not give a satisfying result to our enquiries.




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
