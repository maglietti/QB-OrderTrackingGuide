---
layout: default
title: Create Reports
nav_order: 6
---

# Quick Base Reports

Remember the reports that management asked for in the morning meeting? They want to know which customers spend the most and which products produce the most revenue. We need to create a report to answer each question. Then, we can place them together on the app home page - the dashboard - so management can access them at any time.

Reports are visual displays of data. Quick Base can create pie charts, bar charts, line graphs, summary reports, and even calendars and maps. You’ve already seen the most common report Quick Base automatically creates, the table report. Each time you click a table icon in table navigation, Quick Base opens the table home page and displays the default table report for all of the table records.

## Create a Table Report to summarize Orders

Let's create a report to collect all the information from our tables and display a summary of all the orders. Management didn't ask for the report, yet, but you know that it will help everyone understand what is going on and answer questions they have asked in the past. As you think about what everyone talks about in the morning meeting, you write down the fields that the team usually has questions about.

| Field | Source Table | Type |
|:-|:-|:-|
| Order # | Orders | text |
| Order Date | Orders | date |
| Customer Name | Customers | text |
| Items Ordered | Line Items | **link** |
| Order Total | **Formula** | currency | 

As you thought about the list of items in an order, you decided that a **link** to the `line items` for each order works best. You also decide that you want to include the total for the entire order in the summary, you know that you have to write a formula to do that so you write down **formula** as the source. 

### Add a summary column

Click on the `Orders` table icon in navigation and the **Orders Home** page opens. You compare the fields in the default table report to the fields you wrote down for your summary report. They are close but not the same. Specifically, you notice that there is no order summary for each order record. Let's add one. 

There are several ways to create a summary field in Quick Base. You could define a formula like the one we used to calculate cost in the Line Items table, but there is an easier way. Because we created a table-to-table relationship between the Orders and Line Items tables, the relation itself includes a [summary field](https://help.quickbase.com/user-assistance/create_summary_field.html) feature by default. Let's use that. 

![](assets/images/image-48.png)
![](assets/images/image-49.png)
![](assets/images/image-50.png)
![](assets/images/image-51.png)

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
    11. Click the blue `OK` button
~~~

The relationship between the Orders table and the Line Items table looks like this now:

![](assets/images/image-52.png)

Click the blue `Done` button to add the field to the table configuration. Then click on `Fields` in the **Table Structure** group and verify that the Total field was added to the table.

![](assets/images/image-53.png)

Exit the Order table settings. 

### Create a custom table report

You're getting the hang of this! Now create a new report and configure it to display our summary. Start by clicking on the `Orders` table in navigation to open the **Orders Home** page and expand the Reports & Charts list by clicking on its link.

![](assets/images/image-54.png)

Create a new report by clicking on the `New` button next to the reports & charts search box.

![](assets/images/image-55.png)
![](assets/images/image-56.png)
![](assets/images/image-57.png)
![](assets/images/image-58.png)

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

> **Congratulations!** You configured your first custom report in Quick Base!

Now, verify that the Orders Summary report is correct.

![](assets/images/image-59.png)

## Create a Bar Chart to view Customer by Spend

Management is interested in knowing how the customers are performing. We have a fairly small customers but they purchase a lot from us. Let's use a bar chart to visualize the total that each customer has spent with us. This way, as customer orders are placed, management can see who is buying most and have a feel for how other customers compare. 

![](assets/images/image-60.png)
![](assets/images/image-61.png)
![](assets/images/image-62.png)

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

> You know, **celebration** time! Contrat's on creating your first data visualization!

Verify that the bar chart correctly displays how much each customer has spent this quarter.

![](assets/images/image-63.png)

## Create a Summary Report to display Products by Sales

On to the next chart for management. This time we are looking to summarize the overall revenue generated by each product. Quick Base has a built in report type for this called a "Summary Report." Let's give that a try and see if it is what management is looking for. 

![](assets/images/image-64.png)
![](assets/images/image-65.png)

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

Yup, that is exactly what they asked for. But, before we put it in the dashboard, it's a good practice to verify that the summary chart correctly displays how much revenue each product has brought in.

![](assets/images/image-66.png)

It does! On to making a management dashboard that any can look at at any time. 

[Next](dashboard.html){: .btn .btn-purple }