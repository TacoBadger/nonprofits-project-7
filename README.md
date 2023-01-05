# Nonprofit Dataset (Project 7)

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/NonProfits.png?raw=true)

# Introduction

Lately I have been very interested in how Power Bi can help nonprofits. With Power BI, you can gain insights into your operations and performance, and make data-driven decisions that can help you achieve your mission and goals. I can think of 4 main ways nonprofits can use Power BI analysises:

- Donor analysis: Power BI can be used to analyze donor data, such as donation amounts, frequency, and sources, to better understand donor behavior and identify trends. This can help charities target their fundraising efforts more effectively and improve donor retention.

- Program effectiveness: Charities can use Power BI to track and monitor the effectiveness of their programs and initiatives, such as the number of people served, the impact of the program, and the resources required. This can help charities allocate resources more efficiently and optimize program design.

- Financial analysis: Power BI can be used to analyze financial data, such as revenue, expenses, and fundraising performance, to identify trends and areas for improvement. This can help charities manage their finances more effectively and make informed decisions about budgeting and resource allocation.

- Impact reporting: Charities can use Power BI to create interactive dashboards and reports that showcase the impact of their work and communicate it to stakeholders. This can help charities demonstrate the value of their work to donors, volunteers, and the public.

In this case study, I will limit the scope to a donor analysis. I made fictive non-profit called The Be Happy Foundation, and I also made a dataset of fictive donors.

Please do take note that this document is for practice purposes only.

## Authors
- [@TacoBadger](https://github.com/TacoBadger)

## Table of Contents

  - [Dataset](#dataset)
  - [Methods](#methods)
  - [Ask](#ask)
  - [Prepare](#prepare)
  - [Process](#process)
  - [Analyze](#analyze)
  - [Share and Act](#share-and-act)
  - [Key Findings](#key-findings)
  - [What is next?](#what-is-next)
 

## Dataset
[The Be Happy Foundation Donor Data](https://github.com/TacoBadger/nonprofits-project-7/blob/main/Excel%20Nonprofits.xlsx)

This dataset consist of 100 rows of fake data, I used www.random.org to generate both names and numbers.

It includes:
- Id. This is unique identifier of each donor, from D000100 to D000199.
- Donor. This is the name of the donor which comprise of both first name and surname.
- Anonymity. This field can be populated with Yes and No. In this example, no one of the 100 donors wanted to be anonymous.
- Regular Donation. This column is populated with regular or one-off donation. 
- Amount. This data is great to establish who the biggest donors are.
- Date of donations. This data goes from 2018 to 2022.
- Status reason. This data shows whether the donor is an active or passive contributor.


## Methods
I used the Google Data Analytics framework with the following 6 steps:
1. Ask - Ask effective questions
2. Prepare - Verify data's integrity, check data credibility and reliability, check data types and merge datasets
3. Process - Clean, remove and transform data and document cleaning processes and results
4. Analyze - Identify patterns and draw conclusions
5. Share - Create effective visuals
6. Act - Answer the questions and solve the problems


## Ask
Since I made my own mini dataset - the questions could potentially be a bit skewed towards my own interest. 

With that in mind I have 3 questions.

1. I am curios whether the donation have been increaseing since 2018 and possibly why?
2. I am intriqued by who the top 9 donors are and whether we can see any patterns between them?
3. I am wondering whether we get more one-off donations or regular donations and what we can do to increase the regular donations?


## 2. Prepare
In this case study, I will use 2 programs, Excel and Power BI.

Firstly, I made a mini dataset of 100 rows inside excel:

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel1.png?raw=true)

Here you can see all the columns and rows.

Later on, I used the data in the Excel to work on my Power BI Dashboard.

You can download the dashboard https://github.com/TacoBadger/nonprofits-project-7/blob/main/nonprofitpowerbi.pbix or you can see how it looks like here

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power1.png?raw=true)


## 3. Process
In this step I took the time to process and clean the data in the Excel file. Purposely, I did not create any null values in this dataset, and all entries are not anonymous. I also took some time to clean out all the spelling mistakes and duplicates. I did all this manually, because the dataset is relatively small, however this can also be done programmatically in Excel or Power BI.


## 4. Analyze
The first things I did in Excel was generating a table.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel2.png?raw=true)

From there, I could generate a pivot table.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel3.png?raw=true)

In this pivot table, you can see the date of the donations and also the donor.

Now I generated a graph to get a better overview of donation types and the total amount donated per time periods.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel4.png?raw=true)

All the Excel based table and graphs did not give a insightful result to our enquiries.


## 5. Share
So now we will use Power BI and see if the insights to our enquires becomes clearer. Remember the questions we asked were:

1. I am curios whether the donation have been increaseing since 2018 and possible why?
2. I am intriqued by who the top 9 donors are and whether we can see any patterns between them?
3. I am wondering whether we get more one-off donations or regular donations and what we can do to increase the regular donations?

This Power BI table is clearly showing that from 2018 the amount of donation have only gone down:

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power2.png?raw=true)

The donations have decreased from more than 10k to less than 2K. Why? We don't know yet. We need more data we can analyze to infer some reasons.

In the following Power BI table, we can see who the biggest donors have been. 

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power3a.png?raw=true)
![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power3b.png?raw=true)
![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power3c.png?raw=true)

In Power BI we can click on each donor and see that out of the 10, there are 2 donors, Arun Edwards and Alan Newman that are regular donors. the rest are one-off donors. 

In the final illustration, I can see that the foundation received more one-off donations than regular ones.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power4.png?raw=true)

Although, it would be intereseting to know why, I still don't have enough data to give an explaination.


## 6. Key Findings

This is an important metric and KPI, as the regular donations will increase the long term sustainability of the nonprofit.

The key findings Data shows that the Happy has suffered a steep decline in donations.....
1. There are 595 titles.
2. Cocomelon had the highest number of days during the pandemic. All other titles on the top 10 titles had way less number of days than Cocomelon.
3. 377 of the titles are Netflix exclusive.
4. Movie is the most watched type.
5. The top 10 Tv shows were Cocomelon, Manifest, Queen's Gambit, Outer banks, Squid game, All American, Bridgerton, Cobra Kai, Lucifer and Virgin River
6. Top 10 Movies were The Mitchell vs. The machines, How the grinch stole christmas, Vivo, 365 days, Illumination presents the grinch. The Christmas Chronicles 2, We can be heroes, Red notice, The Unforgivable and Home
7. Top 6 Stand-Up Comedy were Dave Chappelle: The Closer, Kevin Hartz: Zero fucks given, George Lopez: We'll do it for half, Jerry Seinfeld: 23 hours to kill, Chris D'elia: No Pain, Bo Burnham: Inside

## What is next?
Thank you for reading my mini case study about nonprofit donor data. Segmentation, locatiopn, age, hobbies could give us more insigths into.




doccumentation about my Netflix Dataset. To help me improve more of my basic data analytical skills I will list down a few pointers on what's next for my other projects.

- I could have improved my data story telling or I could have made a more compelling narrative by including all detailed and relevant explanation in my documentation, I should know what my target audience is and start telling my data from there. I should also be including basic terms especially for beginners reading my documentation.
- I could have improved my keypointers that can lead the audience to understand more about my data analysis. I could have make use of highlighting all important keywords and relevant data for our target audience.
- A more detailed explanation of the codes used and functions. We can use a small summary for our target audience.
- A more effective way of using visuals where our target audience can easily understand it. Always make sure you choose the proper visual to express your dataset. 
-  We will also start using SQL for our next dataset practice which involves more functions and commands that is more complex than in RStudio. We will specifically used DB Browser SQLite for our next ptractice, DB Browser works similar to SQL in some functions and commands so let us learn about it together in the next dataset. 

See you on our next project!
