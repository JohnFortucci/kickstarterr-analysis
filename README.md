# Kickstarting with Excel

## Overview of Project
This project takes a dataset of crowd funded project , from this data a number of pivot tables and graphs are created allowing more granular analysis to answer the ultimate outcomes of crowd funded campaigns. 


### Purpose
The purpose of this analysis was to provide a tool to analyse crowd funded campaigns and the outcomes of those campaigns, whether they were ultimately :-
- Successfull
- Failed
- Cancelled

The primary focus of this analysis will be to determine the ultimate outcomes based on  :-
- Launch date
- Funding goal
## Analysis and Challenges

### Summary
Based on the data within worksheet kickstarter , two worksheets have been created :-
- Theater Outcomes by Launch Date
- Outcomes based on goals

The kickstarter sheet was modified to include a column for years this is based on the date created field , and is used in the pivot table created in the worksheet : Theater Outcomes by Launch Date

### Analysis of Outcomes Based on Launch Date

#### Overview
A worksheet has been created : Theater Outcomes by Launch Date, based on the data in kickstarter worksheet this shows the outcome based on launch date.

This sheet contains a pivot table and a line graph , the pivot table allows the data to be filtered by :-
- Parent Category
- Years

Therefore allowing the analysis of certain views of the data based on parent categories and/or specific year , by selecting the desired criteria.

It should be noted that the data within the kickstarter sheet has four possible outcomes (Succesfull , Failed , Cancelled and Live). As we cannot determine and absolutes outcome for live , this data will be eliminated from the analysis. This has been achieved by applying a filter to the column labels.

![Fileter Live Image](/resources/Outcome_filter.PNG)

#### Pivot table 
The pivot table displays :
- Launch date month in rows 
- Respective count of the outcomes (Succesfull , Failed and Cancelled) in columns. 
- A grand total column this is a total of the outcomes : Succesfull , Failed and Cancelled.

#### Line graph

The line graph displays the outcomes over calendar month.

The image below shows the kickstarter data with no filters applies.

![Overview](/resources/TO_overview.png)

##### Line graph with filters applied

The image below shows the line graph with a filter of theater is applied to this data , this graph will be used to form conclusion based on the data.

![Overview](/resources/Picture3.png)
### Analysis of Outcomes Based on Goals

##### Overview
A worksheet has been created : Outcome Based on Goals, based on the data in kickstarter worksheet this shows the outcome based on campaign financial goal.

This sheet contains a data table and a line graph. 

The data is only concerned :- 
- With outcomes that are absolute and therefore outcome status live is not included in this sheet.
- Entries in the kickstarter spreadsheet that have a subcategory of plays

##### Data table
The data table shows counts and percentages of outcomes allocated across predefined financial goal ranges. 

The data is only concerned :- 
- With outcomes that are absolute and therefore outcome status live is not included in this sheet.
- Entries in the kickstarter spreadsheet that have a subcategory of plays

The data table contains- 
- Rows showing various financial goal buckets.
- Columns showing counts of the various status (Succesful, Failed and Cancelled) allocated to the appropriate range
- To achieve this the excel COUNTIF function is used , the COUNTIF function references column F to filter based on the outcomes , column R to filter subcategory plays and Column D to determine is the entry should be included in the current range count. 
 
   For example

   =COUNTIFS(Kickstarter!$F:$F,"=successful",Kickstarter!$R:$R,"=plays",Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<=4999.99") 
   
   This will count the number of successful campaigns for subcategory plays that fall within a financial goal range of $1000 to $4999.
   The $ sign prefixing the the row reference allows the copy and pasting of the formula and allows the changing of inclusion criteria keeping the row reference static.
 
- Total projects uses the excel SUM function , totaling the Number Successful , Number Failed and Number Cancelled.
- Columns showing the outcome status (Succesful, Failed and Cancelled) based on the total number of projects that meet the goal ranges as percentages.
- To achieve this a calculation is used based on the count of outcome status divided by the total number of projects of that particular goal range. These cells are formatted as percentage cells and are formatted to 1 decimal place this was mainly for cosmetic purpose as excel was rounding some cells that would have gave a visual count of above 100%.

- The images below shows the makeup of the data table the line graph is based on
![Overview](/resources/OBG_Datatable.PNG)
### Challenges and Difficulties Encountered

During the challenge the one item I kept reviewing was the ranges of the goals for the Outcome Based on Goals , the main question being whether or not to round up or round down the decimal value if any in the goal amount. 

I reviewed the data in the kickstarter sheet to check if this would impact any of the data we are using , to do this I created a temporary column that took the value in the goal column and subrtracted the integer value of the goal for each row, if the value was greater than zero , I put text in the temporary column "Has decimal value". Then filtered the data with subcategory plays. There where no entries displayed , I concluded that this condition would not impact the data set we are concerned with but would affect some other sub categories. With that said I decided to make the range upper values to included the decimal .99.
## Results

### Conclusions based on Theater Outcomes by Launch Date

From the graph created in the Theater Outcomes by Launch date the following conclusions can be made.

1. The most successful campaigns are in the month of May.
2. In the month of December there is no significant advantage in successes. All other months showed a greater number of success to failure.

### Conclusions based on Theater Outcomes based on Goals

From the graph created in the Theater Outcomes based on Goals the following conclusions can be made. 

1. The greater the amount of the goal the chanes for failure increase , the most successful campaigns are at the lower end of the goal range. The succesful trend is on decline as the goal value increase failures become the greater value around about the $15000 goal range.
2. No campaigns got cancelled for funding issues

### Limitations of this dataset

The data set has some limitations :- 
1. The data set contains data from 2009 to 2017 , assuming we are doing this analysis in present day 2022 the data is not current.
2. The data does not represent increased funding mechanisms available for example with the increased adoption of websites like GOFUNDME.com etc , these became more prevalent      during the data renge of the data.
3. There is no method of representing current events in the data , for example you would have to assume that if data was present for 2020 / 2021 the data would be impacted by COVID 

- What are some other possible tables and/or graphs that we could create?
### Other possible tables and / or graphs

1. A table and graph of Outcomes based on goals by country.
