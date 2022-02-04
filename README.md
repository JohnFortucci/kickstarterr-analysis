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
Markup :- Rows showing various financial goal buckets.
- Columns showing counts of the various status (Succesful, Failed and Cancelled) allocated to the appropriate range
  - To achieve this the excel COUNTIF function is used , the COUNTIF function references column F to filter based on the outcomes , column R to filter subcategory plays and Column D to determine is the entry should be included in the current range count. 
  - For example : 
    =COUNTIFS(Kickstarter!$F:$F,"=successful",Kickstarter!$R:$R,"=plays",Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<=4999") , this will count the number of successful campaigns that fall within a financial goal range of $1000 to $4999.
- Columns showing the outcome status (Succesful, Failed and Cancelled) based on the total number of projects that meet the goal ranges as percentages.
### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
