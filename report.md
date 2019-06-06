---
layout: default
title: Create a Report
nav_order: 6
---

# Create a report

Remember the report that management asked for? She asked to see what customers are spending the most and what products are selling the best. Create two charts, then place them together on the app home page - the dashboard - that management can access at any time to view the current reports. 

Reports are visual displays of data. They can be pie charts, bar charts, line graphs, summary reports, and even calendars and maps. You’ve already seen a few reports that Quick Base automatically created, including an embedded report on a form displaying line items. 

## Create a Chart for Customer by Spend

You can create reports on all your tables. A report can include data from just its own table or may include data from several tables. For your first report, build a chart based on the Line Items table:
 
![](/assets/images/lineItemsReport.png)

    1. View the Line Items table.
    2. Select Reports & Charts.

Here you can see the two reports Quick Base automatically created for you when you created the table. These are both List reports which list the data in a spreadsheet format. You are going to build a chart report:

    3. Select + New.
    4. Select the radio button for Chart.
    5. Select Create.
    6. Give the chart an appropriate name, such as Customers by Spend. Keep in mind that you can rename reports at any time. 
    7. Enter a description of your choice. The description is important because without it, regular users of this app may not  kn w what the report is for, even if the name is clear. You can update the report description at any time. 
    8. Select the checkbox for Show description on chart page so app users can view the description.

Skip over the Reports & Charts Panel section. In the Chart Details section, provide content to create the chart:

    1. Select the button Select a type of chart and select Pie.
    2. Set Series to Customer Name.
    3. Set Data Values to Unit Price.
    4. Set Summarize by to (summed).
    5. Skip the Sorting section.
    6. Select the checkbox for Data labels always visible. 
    7. Set Display value as to Value. Feel free to change this later to see what else is possible.

There are plenty of other settings to play with, but those are the load-bearing ones for this exercise. Go ahead and explore, but when you’re done, select Save in the upper-right and view the results. 

Move your cursor over the pie chart to see additional information. If you want to make further changes, select Customize this Report in the upper-right. Later, you can always go to Settings > Reports & Charts to find this report and make further changes.

Here’s the great thing about reports in Quick Base: once you’ve created one type, you can easily create others. Creating various types of reports will not only help you pick the right way to display your data, but will provide some much-needed variety for users poring over data all day. 

Create a Summary Report of Products by Spend

Let’s get back to the VP’s request. This time, use a summary report to show the top selling products. 

    1. In the Line Items table, select Reports & Charts.
    2. Select + New.
    3. Select the radio button for Summary.
    4. Select Create.
    5. Name the report Products by Spend.
    6. Provide an apt description, such as This lists all products by value sold. 
    7. Select the checkbox for Show description on report page.
    8. In the Summarize Data section, set Summarize to Unit Price.
    9. Do not change the default values for Summarize By and Display As.
    10. In the Grouping and crosstabs section, set Group by to Product Name. 
    11. Do not change the default value for Combine.
    12. In the Sorting section, set Sort to Custom order.
    13. Set Sort by to Unit Price (tot) and from high to low.
    14. That’s it! Select Save to view the results. 


[Next](dashboard.html){: .btn .btn-purple }