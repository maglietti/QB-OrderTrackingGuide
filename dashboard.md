---
layout: default
title: Create a Dashboard
nav_order: 7
---

# App Dashboard

Dashboards give people one convenient place to see or access key information. It is what people see when they first sign into an app. You can create different dashboards for different roles. For now, we are going to create one dashboard for everyone. We have three reports from earlier, lets get them into the dashboard. 

![](assets/images/image-67.png)

## Add the Orders Summary Report

The orders summary table report is a good way for anyone to see information about orders and drill into the line item tht the customer selected. It is the foundation of our dashboard, so let's configure a home for it first.

![](assets/images/image-68.png)

1. Click **Customize this Page**
2. Click and drag the **Report or Chart** widget onto your page
3. Click the icon gear
4. Select the **Orders Summary** report


That looks awesome! Now every time your **Order Tracking** app is opened, the report will automatically update and display. 

** ADD SCREENSHOT**

## Add the Customer by Spend Report

Next in line is the bar chart displaying the customer spend report. 

![](assets/images/image-69.png)

1. Click and drag the **Report or Chart** widget onto your page
2. Click the icon gear
3. Select the **Customer by Spend** chart

## Add the Product by Revenue Report

Last but not least is the product revenue summary report. 

![](assets/images/image-70.png)

1. Click and drag the **Report or Chart** widget onto your page
2. Click the icon gear
3. Select the **Product by Revenue** report

Looking good!
![](assets/images/image-72.png)

## Add a Create New Order Button

Hey, while we are here and have the dashboard editor open, why don't we go ahead and add a button that lets users create new orders directly from the dashboard. That will make it a lot easier for your team to get right into the order entry form with just one click!

![](assets/images/image-74.png)

1. Drag and drop the **Button Bar** widget from the top to a spot above the reports.
2. A  popup window displays. At the top, there are three options for button type: New Record, Report, or Page. Leave the default value of **New Record**. 
3. In the New Record dropdown, select **Order**. 
4. Close this popup window.  
5. Hover your mouse over the widget top right corner to make the gear icon appear. Select this gear and deselect **Show a Title.**
6. Click **Save**

Look at that! You now have a single dashboard that allows users to view how much customers are spending, what products are selling the most, and a button to create a new order. Now that’s convenience!

[Next](conclusion.html){: .btn .btn-purple }