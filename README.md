#excel-challenge
#excel-challenge
Module 1 Crowdfunding Analysis

## Background
Crowdfunding platforms like Kickstarter and Indiegogo have been growing in success and popularity since the late 2000s. From independent content creators to famous celebrities, more and more people are using crowdfunding to launch new products and generate buzz, but not every project has found success.
To receive funding, the project must meet or exceed an initial goal, so many organizations dedicate considerable resources looking through old projects in an attempt to discover “the trick” to finding success. For this week's Challenge, you will organize and analyze a database of 1,000 sample projects to uncover any hidden trends.

## Project Steps 
- Open Excel workbook
- Use conditional formatting to fill each cell in the outcome column with a different color, depending on whether the associated campaign was successful, failed, canceled, or is currently live.
    - Create a new column called Percent Funded that uses a formula to find how much money a campaign made relative to its initial funding goal.
- Use conditional formatting to fill each cell in the Percent Funded column according to a three-color scale. The scale should start at 0 with a dark shade of red, and it should transition to green at 100 and blue at 200.
    - Create a new column called Average Donation that uses a formula to find how much each project backer paid on average.
    - Create two new columns, one called Parent Category and another called Sub-Category, that use formulas to split the Category and Sub-Category column into the two new, separate columns.
    - Create a new sheet with a pivot table that analyzes your initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per category.
- Create a stacked-column pivot chart that can be filtered by country based on the table that you created.
- Create a new sheet with a pivot table that analyzes your initial sheet to count how many campaigns were successful, failed, or canceled, or are currently live per sub-category.
- Create a stacked-column pivot chart that can be filtered by country and parent category based on the table that you created.
- The dates in the deadline and launched_at columns use Unix timestamps. 
    - Create a new column named Date Created Conversion that will use this =(((A1/60)/60)/24)+DATE(1970,1,1) to convert the data contained in launched_at into Excel's date format.
    - Do the same for Date Ended Conversion and convert data into deadline in Excel's date format. 
    - Create a new sheet with a pivot table that has a column of outcome, rows of Date Created Conversion, values based on the count of outcome, and filters based on parent category and Years.
    - Now, create a pivot-chart line graph that visualizes this new table.
- Create a new sheet with 8 columns:
    - Goal: For goal column, the criterias are: 
        - Less than 1000, 1000 to 4999, 5000 to 9999, 10000 to 14999, 15000 to 19999, 20000 to 24999, 25000 to 29999, 30000 to 34999, 35000 to 39999, 40000 to 44999, 45000 to 49999, Greater than or equal to 50000. 
    - Number Successful: type into formula bar "=COUNTIFS(crowdfunding!D:D,"<1000",crowdfunding!G:G,"successful")" for goal of less than 1000
    - Number Failed: type into formula bar "=COUNTIFS(crowdfunding!D:D,"<1000",crowdfunding!G:G,"failed")" for goal of less than 1000
    - Number Canceled: type into formula bar "=COUNTIFS(crowdfunding!D:D,"<1000",crowdfunding!G:G,"canceled")" for goal of less than 1000
    - Total Projects: type into formula bar "=B2+C2+D2" for goal of less than 1000
    - Percentage Successful: type into formula bar "=B2/E2" for goal of less than 1000
    - Percentage Failed: type into formula bar "=C2/E2" for goal of less than 1000
    - Percentage Canceled: type into formula bar "=D2/E2" for goal of less than 1000
    *Use the same formula for each criteria
- Create a line chart that graphs the relationship between a goal amount and its chances of success, failure, or cancellation.
- Create a new worksheet in your workbook, and create one column for the number of backers of successful campaigns and one column for unsuccessful campaigns.
- Use Excel to evaluate the following values for successful campaigns, and then do the same for unsuccessful campaigns:
    - The mean number of backers: =AVERAGE(B:B,B1)
    - The median number of backers: =MEDIAN(B:B,B1)
    - The minimum number of backers: =MIN(B:B,B1)
    - The maximum number of backers: =MAX(B:B,B1)
    - The variance of the number of backers: =VAR.S(B:B,B1)
    - The standard deviation of the number of backers: =STDEV.S(B:B,B1)
    *Do the same for failed campaigns
## Statistical Analysis Questions
- Use your data to determine whether the mean or the median better summarizes the data.
    - When the mean and median are about the same, the data is normally distributed. However, for both successful and failed campaigns, the mean and median are extremely far apart, making them skewed. 
- Use your data to determine if there is more variability with successful or unsuccessful campaigns. Does this make sense? Why or why not?
    We also know that when data is skewed, it is more useful to refer to the median because the mean is distorted by outliers. Therefore, there is more variability with successful campaigns because of it's higher variance and standard deviations. 

## Analysis Report Questions
- Given the provided data, what are three conclusions that we can draw about crowdfunding campaigns?
    - Categories in Film/Video, Music, and Theater are the top 3 most popular. 
    - Theater is the most popular parent category despite only 187 successes out of 344 outcomes.
    - July is the peak success month for any category.
- What are some limitations of this dataset?
    - A limitation of this dataset is that it does not include the reason some of these campaigns failed or were cancelled. 
    - Sub categories could be more specific, for example, the genre of music or the type of food.
- What are some other possible tables and/or graphs that we could create, and what additional value would they provide?
    - The average goal and amount pledged for each category




