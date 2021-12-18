# Excel-Challenge-Kickstarter

## Background

Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.

Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. For this project, I organized and analyzed a database of 4,000 past projects in order to uncover any hidden trends by utilizing conditional formatting and pivot tables. 


## Procedure

![Kickstarter Table](Images/FullTable.png)

Using the database provided, I modified and analyzed the data of 4,000 past Kickstarter projects to attempt to uncover some market trends.

* Used conditional formatting to fill each cell in the `state` column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.

  * Created a new column O called `Percent Funded` that uses a formula to uncover how much money a campaign made to reach its initial goal.

* Used conditional formatting to fill each cell in the `Percent Funded` column using a three-color scale. The scale should start at 0 and be a dark shade of red, transitioning to green at 100, and blue at 200.

  * Created a new column called `Average Donation` that uses a formula to uncover how much each backer for the project paid on average.

  * Created two new columns, one called `Category` and another called `Sub-Category`, which used formulas to split the `Category and Sub-Category` column into two parts.

  ![Category Stats](Images/CategoryStats.png)

  * Created a new sheet with a pivot table that analyzed the initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per **category**.

  * Created a stacked column pivot chart that filtered by country based on the table I created.
  
   ![Subcategory Stats](Images/SubcategoryStats.png)

  * Created a new sheet with a pivot table that will analyzed the initial sheet to count how many campaigns were successful, failed, or canceled, or are currently live per **sub-category**.

  * Created a stacked column pivot chart that filtered by country and parent-category based on the table I created.

* Converted timestamps in `deadline` and `launched_at` columns to a normal date using excel formula.

  ![Outcomes Based on Launch Date](Images/LaunchDateOutcomes.png)

  * Created a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.

  * Created a pivot chart line graph that visualizes this new table.

* Created a report in Microsoft Word to answer the following questions. see Excel Challenge Discussion Questions.doc

1. Given the provided data, what are three conclusions we can draw about Kickstarter campaigns?
2. What are some limitations of this dataset?
3. What are some other possible tables and/or graphs that we could create?

##Excel Challenge Discussion Questions

1.	Given the provided data, there are a few conclusions we can draw about Kickstarter campaigns. The first one is that Kickstarter campaigns are more likely to be successful than not if we look at all campaigns in general, without regarding the category they fall in. However, another conclusion we can come to is that Kickstarter campaigns in certain categories are more likely to be successful than others based on the data provided. Kickstarters that fall in the performing arts categories (theatre, music, plays) compose most campaigns and are also the most likely to be successful. However, campaigns specifically regarding food are more likely to fail than to succeed. 

2.	Some of the limitations of the dataset are the number of campaigns in certain categories and sub-categories. Most successful sub-categories fall in the larger categories of theatre, music, and film/video. While these are the most successful categories, they also have the most overall number of campaigns. The least successful categories are a lot less abundant in number of campaigns than their successful counterparts. Food, games, journalism, publishing, and photography all have less than half of the number of campaigns than the most successful categories (theatre, music, and film/video) have.

3.	See reports table 1 thru 10. We could create charts to visualize trends could include a pie chart using the total number of campaigns for each category. This chart would illustrate the overall composition of Kickstarter campaigns in general where we would see the majority composing of theatre, music and film/video. We could also create specific pie charts for each category illustrating the number of successes vs. the number of failures. Here we would be able to easily visualize which categories are most successful percentage-wise. We could also create a bar chart of categories and their total amounts pledged to see which categories acquire the most funding. One other chart we could create would be a bar chart illustrating number of successes and number of failures for certain ranges of campaign goals to see if there is a point at which campaigns are less likely to start being successful. 

## Further Analysis

* Created a new sheet with 8 columns:

  * `Goal`
  * `Number Successful`
  * `Number Failed`
  * `Number Canceled`
  * `Total Projects`
  * `Percentage Successful`
  * `Percentage Failed`
  * `Percentage Canceled`

* In the `Goal` column, created 12 rows with the following headers:

  * Less than 1000
  * 1000 to 4999
  * 5000 to 9999
  * 10000 to 14999
  * 15000 to 19999
  * 20000 to 24999
  * 25000 to 29999
  * 30000 to 34999
  * 35000 to 39999
  * 40000 to 44999
  * 45000 to 49999
  * Greater than or equal to 50000

  ![Goal Outcomes](Images/GoalOutcomes.png)

* Using the `COUNTIFS()` formula, counted how many successful, failed, and canceled projects were created with goals within the ranges listed above. Populated the `Number Successful`, `Number Failed`, and `Number Canceled` columns with this data.

* Added up each of the values in the `Number Successful`, `Number Failed`, and `Number Canceled` columns to populate the `Total Projects` column. Then, using a mathematical formula, found the percentage of projects that were successful, failed, or canceled per goal range.

* Created a line chart that graphed the relationship between a goal's amount and its chances at success, failure, or cancellation.

## Further Statistical Analysis

If one were to describe a successful crowdfunding campaign, most people would use the number of campaign backers as a metric of success. One of the most efficient ways that data scientists characterize a quantitative metric, such as the number of campaign backers, is by creating a summary statistics table.

* Created a new worksheet in workbook, and created a column each for the number of backers of successful campaigns and unsuccessful campaigns.

  ![Images/backers01.png](Images/backers01.png)

* Used Excel to evaluate the following for successful campaigns, and then for unsuccessful campaigns:

  * The mean number of backers. (see Backers Tab)

  * The median number of backers.(see Backers Tab)

  * The minimum number of backers.(see Backers Tab)

  * The maximum number of backers.(see Backers Tab)

  * The variance of the number of backers.(see Backers Tab)

  * The standard deviation of the number of backers.(see Backers Tab)

* Used data to determine whether the mean or the median summarizes the data more meaningfully.

* Used data to determine if there is more variability with successful or unsuccessful campaigns.

