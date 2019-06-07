---
layout: default
title: Create Reports
nav_order: 6
---

# Quick Base Reports

Remember the reports that management asked for in the morning meeting? They want to know which customers spend the most and which products produce the most revenue. We need to create a report to answer each question. Then we can place them together on the app home page - the dashboard - so management can access at any time.

Reports are visual displays of data. Quick Base can create pie charts, bar charts, line graphs, summary reports, and even calendars and maps. You’ve already seen the most common report that Quick Base automatically creates, the table report. Each time you click a table in the navigation, Quick Base opens the table home page and displays the default table report displaying all of the table records.

## Create a Table Report to summarize Orders

The first report that we are going to create will collect information from all of our tables and display a summary of all orders. Management didn't ask for the report today, but you know that it will help them understand the other reports and answer questions that they have asked in the past. You think about what everyone talks about in the morning meeting and write down the fields that the team usually has questions about.

You write down the following thoughts:

| Field | Source Table | Type |
|:-|:-|:-|
| Order # | Orders | text |
| Order Date | Orders | date |
| Customer Name | Customers | text |
| Items Ordered | Line Items | **link** |
| Order Total | **Formula** | currency | 

As you thought about the list of items in the order, you decided that you really want to **link** to that data rather than including it in the summary table. You also decided that you want to include the total for the entire order in the summary, you know that you have to write a formula to do that so you write down **formula** as the source. 

### Add a summary column

You click on the `Orders` table in navigation and the **Orders Home** page opens. You compare the fields in the default table report to the fields you wrote down for your summary report. They are close but not the same. Specifically, you notice that there is no order summary for each order record. Let's add one. 

There are several ways to create a summary field in Quick Base. You could write a formula like the one we used to calculate cost in the Line Items table, but there is an easier way. Because we created a table-to-table relationship between the Orders and Line Items tables, includes a [summary field](https://help.quickbase.com/user-assistance/create_summary_field.html) feature by default. Let's use that. 

~~~
    1. Click on the Orders table in navigation 
    2. Click the Gear icon to open table settings
    3. Click on Table-to-table relationships in the Table Structure group
    4. Click on the Orders -> Line Items relationship
    5. Click on `Add Summary Field`
    6. Select `A summary of a specific Field`
    7. Select `Total` for the field
    8. Select `Line Total` from the field list
    9. Click the blue `Create` button
    10. Name the field "Total"
~~~

Relationship between the Orders table and the Line Items table looks like this:

SCREENSHOT
{: .label .label-red }

Click the blue `Done` button to add the field to the table configuration. Then click on `Fields` in the Table Structure group and verify that the Total field was added to the table.

SCREENSHOT
{: .label .label-red }

Exit the Order table settings. 

### Create a custom table report

Just like when we create a new table, we need to create a new Quick Base report and then configure it to display what we want. Start by clicking on the `Orders` table in navigation to open the **Orders Home** page and expand the Reports & Charts list by clicking on its link.

SCREENSHOT
{: .label .label-red }

Create a new report by clicking on the `New` button next to the reports & charts search box.

SCREENSHOT
{: .label .label-red }

~~~
    1. Select Table in the New report pop-up
    2. Name: Orders Summary
    3. Description: Summary of customer orders
    4. Select Custom columns
    5. Select the Report Columns
    6. Select `Sort or group on other fields` in the Sourting & Grouping group
    7. Select `sort from hight to low by`
    8. Select `Order Date` from the list of fields
    9. Click the blue `Save` button
    10. Name: Orders Summary in the save report pop-up
    11. Description: Summary of customer orders
~~~

Verify that the Orders Summary report is correct

SCREENSHOT
{: .label .label-red }

## Create a Bar Chart to view Customer by Spend

Say something here...

SCREENSHOT
{: .label .label-red }

~~~
    1. Click New
    2. Select `Chart` on the New report pop-up
    3. Name: Customers by Spend
    4. Description: Quarterly spend by each customer
    5. Select `bar` as the chart Type in the Chart Details group
    6. Select `Customer Name` and `Equal Values` for the x axis
    7. Select `Line Total` and `(summed)` for the y axis
    8. Select `Order Date` and Group by: `Quarter` for the Series
    9. Click the blue `Save` button
~~~    

Verify that the bar chart correctly displays how much each customer has spent this quarter.

SCREENSHOT
{: .label .label-red }

## Create a Summary Report to display Products by Sales

Say something here...

SCREENSHOT
{: .label .label-red }

~~~
    1. Click New
    2. Select Summary from the New Report pop-up
    3. Name: Products by Revenue
    4. Description: Products sorted by revenue
    5. Summarize: `Line Total`
    6. Summarize By: `Totals`
    7. Display As: `Normal Value`
    8. Group By: `Product Name`
    9. Combine: `Equal Values`
    10. Sorty by: `Line Total (tot)`
    11. Select `from hight to low`
    12. Click the blue `Save`button
~~~

Verify that the summary chart correctly displays how much revenue each product has brought in.

SCREENSHOT
{: .label .label-red }


**Summary**

Write something here...


[Next](dashboard.html){: .btn .btn-purple }