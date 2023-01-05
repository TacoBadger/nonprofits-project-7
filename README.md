# Nonprofit Dataset (Project 7)

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/NonProfits.png?raw=true)

# Introduction

Lately I have been very interested in how Power Bi can help nonprofits. With Power BI, you can gain insights into your operations and performance, and make data-driven decisions that can help you achieve your mission and goals. I can think of 4 main ways nonprofits can use Power BI analysises:

- Donor analysis: Power BI can be used to analyze donor data, such as donation amounts, frequency, and sources, to better understand donor behavior and identify trends. This can help charities target their fundraising efforts more effectively and improve donor retention.

- Program effectiveness: Charities can use Power BI to track and monitor the effectiveness of their programs and initiatives, such as the number of people served, the impact of the program, and the resources required. This can help charities allocate resources more efficiently and optimize program design.

- Financial analysis: Power BI can be used to analyze financial data, such as revenue, expenses, and fundraising performance, to identify trends and areas for improvement. This can help charities manage their finances more effectively and make informed decisions about budgeting and resource allocation.

- Impact reporting: Charities can use Power BI to create interactive dashboards and reports that showcase the impact of their work and communicate it to stakeholders. This can help charities demonstrate the value of their work to donors, volunteers, and the public.

In this case study, I will limit the scope to a donor analysis. I made fictive non-profit called The Be Happy Foundation, and I also made a dataset of fictive donors.

Please note that this document is for practice purposes only.

## Authors
- [@TacoBadger](https://github.com/TacoBadger)

## Table of Contents

  - [Dataset](#dataset)
  - [Method](#method)
  - [Ask](#ask)
  - [Prepare](#prepare)
  - [Process](#process)
  - [Analyze](#analyze)
  - [Key findings](#key-findings)
  - [What is next](#what-is-next)
 

## Dataset
[The Be Happy Foundation Donor Data](https://github.com/TacoBadger/nonprofits-project-7/blob/main/Excel%20Nonprofits.xlsx)

This dataset consist of 100 rows of fake data, I used www.random.org to generate both names and numbers.

It includes:
- Id. This is unique identifier of each donor, from D000100 to D000199.
- Donor. This is the name of the donor which comprise of both first name and surname.
- Anonymity. This field can be populated with Yes and No. In this example, no one of the 100 donors wanted to be anonymous.
- Regular Donation. This column is populated with regular or one-off donation. 
- Amount. This fiels shows the DKK amount of each contribution.
- Date of donations. This data goes from 2018 to 2022.
- Status reason. This data shows whether the donor is an active or passive contributor.


## Method
I used the Google Data Analytics framework with the following 6 steps:
1. Ask - Ask effective questions
2. Prepare - Verify data's integrity, check data credibility and reliability, check data types and merge datasets
3. Process - Clean, remove and transform data and document cleaning processes and results
4. Analyze - Identify patterns and draw conclusions
5. Share - Create effective visuals
6. Key findings - Answer the questions and solve the problems


## Ask
Since I made my own mini dataset - the questions could potentially be a bit skewed towards my own interest. Naturally the data would be less messy and there could also be selection bias with the gap between the sample and the entire target group. 

With that in mind I have 3 questions.

1. I am curious whether the donation have been increaseing since 2018 and possibly why?
2. I am intriqued by who the top 9 donors are and whether we can see any patterns between them?
3. I am wondering whether we get more one-off donations or regular donations and what we can do to increase the regular donations?


## Prepare
In this case study, I will use 2 programs, Excel and Power BI.

Firstly, I made a mini dataset of 100 rows inside excel:

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel1.png?raw=true)

Here you can see all the columns and rows.

Later on, I used the data in the Excel to work on my Power BI Dashboard.

You can download the dashboard https://github.com/TacoBadger/nonprofits-project-7/blob/main/nonprofitpowerbi.pbix or you can see how it looks like here

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power1.png?raw=true)


## Process
In this step I took the time to process and clean the data in the Excel file. Purposely, I did not create any null values in this dataset, and all entries are not anonymous. I also took some time to clean out all the spelling mistakes and duplicates. I did all this manually, because the dataset is relatively small, however this can also be done programmatically in Excel or Power BI.


## Analyze
The first things I did in Excel was generating a table.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel2.png?raw=true)

From there, I could generate a pivot table.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel3.png?raw=true)

In this pivot table, you can see the date of the donations and also the donor.

Now I generated a graph to get a better overview of donation types and the total amount donated per time periods.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/excel4.png?raw=true)

This graph turned out a bit messy and hard to read. You can of course make some improvements, however, it is time to move to Power BI, so we can utilize the great visualizations.


## Share
In this section, we will use Power BI. Remember the questions we asked were:

1. I am curios whether the donation have been increaseing since 2018 and possible why?
2. I am intriqued by who the top 9 donors are and whether we can see any patterns between them?
3. I am wondering whether we get more one-off donations or regular donations and what we can do to increase the regular donations?

This Power BI table is clearly showing that from 2018 the amount of donation have only gone down:

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power2.png?raw=true)

The donations have decreased from more than 10k to less than 2K. Why? We don't know yet. We need more data we can analyze to infer some reasons.

If I have to take a guess, we can say that the economy in 2018 was before covid, which could be the reason why Sum of the Amount that year was 100% higher than any other years. The following year, between 2019-2021 it stabilized. In 2022 it dropped another 50%, this year the war in Ukraine started resulting in higher gas prices and fears in many countries in Europe, including Denmark.

In the following Power BI table, we can see who the biggest donors have been the follwing 8 people. 

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power3a.png?raw=true)
![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power3b.png?raw=true)
![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power3c.png?raw=true)

In Power BI we can click on each donor and see that out of the 10, there are 2 donors, Arun Edwards and Alan Newman that are regular donors. the rest are one-off donors. With the data we have, it is hard infer any patterns between them, however, the amount they donated is very close to 2.000 DKK each 

In the final illustration, I can see that the foundation received more one-off donations than regular ones.

![](https://github.com/TacoBadger/nonprofits-project-7/blob/main/power4.png?raw=true)

Although, it would be intereseting to know why, I still don't have enough data to give an explaination. To increase the regular donations, it would optimal to interview both segments and understand their motives and why they donate to us.


## Key findings

In this case study, we worked with a donor analysis based on 100 row of fake data. We found a clear trendline with donations going down over the last 5 years.

With minimal data, we learned that DKK. 2000 is the maximum amount any donor want to contribute to our foundation. We also learned that most of our donors are one-off donors.

Before we can figure out how we can get more regular donations and increase the long term sustainability of our nonprofit, we have to get into the dialogue with our exisisting donor to learn what they like and dislike about our work at the Be Happy Foundation.

In addition, more transaction, location and motivation data would also help us understand the donors.

## What is next
Thank you for reading my mini case study about nonprofit donor data. To improve the case, I would need to have more data I can analyze, preferably, real life data about locatiopn, age and hobbies about our donors.

In addition, I would need to learn more about campaigns, track the results, and improve on past performances with a data driven approach to see how we can attract new donors.

I also think it makes sense to segment all the old donors, from active to passive donors, to see how we can re-engage with them in a meanful way.
