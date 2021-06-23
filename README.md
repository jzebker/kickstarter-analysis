# Kickstarting with Excel

## Overview of Project
Using the Kickstarter data set, create 2 technical analyses deliverables on fundraising campaign outcomes for the categories given, one based on their launch dates and one based on their funding goals.  In addition, submit a written analysis of the results.
### Purpose
Provide Louise with insight and analysis on how different campaigns fared in relation to their launch dates and their funding goals.
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Visualize theater campaign outcomes with respect to their launch date in Excel using a pivot table and a line chart.  Populate the pivot table with the fields seen in the image below.

<p align="center">
  <img width="356" alt="Screen Shot 2021-06-22 at 5 32 28 PM" src="https://user-images.githubusercontent.com/84994321/123016603-dbfc8980-d37f-11eb-9afe-9bb9c5dc86e9.png" />
</p>

Make sure data is filtered by parent category "theater", displayed by month, and in descending order from left to right as in the screenshot below.  Omit 'live' outcomes.

<p align="center">
  <img width="593" alt="Screen Shot 2021-06-22 at 5 47 50 PM" src="https://user-images.githubusercontent.com/84994321/123017725-05b6b000-d382-11eb-97fa-2e3e55a95a87.png" />
</p>

Create a line chart with appropriate labels.

<p align="center">
  <img width="368" alt="Screen Shot 2021-06-22 at 5 57 23 PM" src="https://user-images.githubusercontent.com/84994321/123018418-62ff3100-d383-11eb-8c30-d6f5e51e32b2.png">
</p>

### Analysis of Outcomes Based on Goals
Visualize percentages of campaign outcomes for plays based on goal size (money requested) in Excel using a line chart.  Use the goal ranges in the image below to find the total number and percentage of successful, failed, and canceled outcomes for plays.

<p align="center">
  <img width="642" alt="Screen Shot 2021-06-22 at 6 05 14 PM" src="https://user-images.githubusercontent.com/84994321/123019096-a60dd400-d384-11eb-9d94-d1df8408ec09.png">
</p>

Totals for successful, failed, and canceled can be populated using an appropriate countif statement.  An example for "failed" "plays" in the range 20000 to 24999 is given.

   `=COUNTIFS(Kickstarter!$D:$D,">=20000",Kickstarter!$D:$D,"<25000",Kickstarter!$F:$F,"failed",Kickstarter!$R:$R,"plays")`

Create a line chart with appropriate labels from the populated table.

<p align="center">
  <img width="858" alt="Screen Shot 2021-06-22 at 6 15 36 PM" src="https://user-images.githubusercontent.com/84994321/123019715-de61e200-d385-11eb-9f33-757f8c5c8aa0.png">
</p>

### Challenges and Difficulties Encountered
Multiple conditions can be added one after the other in a COUNTIF statement.  Initially I thought writing one expression "20000<=x<25000" would work but it does not.  COUNTIFS(Kickstarter!$D:$D,">=20000",Kickstarter!$D:$D,"<25000"... would be the correct format.

I chose to omit "live" outcomes because I could not find a clear definition for them.  I thought it would mean the campaign has not ended yet however there are deadlines listed in the file that have already passed.

Another difficulty is that the first chart is filtered by parent category "theater" while the second chart is filtered by subcategory "plays" within "theater".  Louise is producing a play so it should be up to her which to use.
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
