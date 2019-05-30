---
layout: default
title: Create Items Table
nav_order: 5
---

# Create the Line Items Table

Drew kept track of items for each order on the Order Details.xlsx spreadsheet. It has six columns: Order #, Line #, Product #, Product Name, Unit Price, and Quantity. Here’s a look at the first four records in the spreadsheet. 

![](assets/images/itemsTable.png)

Order 444111 has three line items: Quick Charger, Quick Tablet, and Quick Phone, and the order is for a quantity of three each. 

You need to get the order detail into your app so you can keep track of every line item. You may wonder if you could simply add the line items to the existing Orders table. Do you really need a separate table for the line items? Whenever you need to track something, decide if you can add fields to an existing table or if you must create a whole new table. To decide, ask yourself two questions:

* Do I track many of these?
* Do I track many things about these?

If the answer is yes to both, then create a table. 

For line items, the answer to both is yes. You are tracking many line items, and many things about line items, such as quantity, product number, product name, and unit price. So you need to create a table for line items. 

You will build the table a little differently this time. Because data related to the line items is already in the app, you can take advantage of Quick Base functionality to make entering line items in the user interface a snap! You will be able to add one or more line items to an order by selecting the product number from a dropdown menu, and have the product name and unit price auto-fill. 

Earlier in this exercise, you added data related to line items to tables. Specifically, you added product numbers, product names, and unit prices to the Products table, and you added the order numbers and order dates to the Orders table. Rather than entering all this data into the Line Items table, you can pull it from existing tables. In technical terms, you first create a table-to-table relationship between the tables. Then you pull many values from the different tables together using lookup fields – something you’ll learn more about shortly. 

Begin by creating a table to contain the line items.  

~~~
    1. Select + New Table.  
    2. Select From scratch - Design your own table.
    3. Name the table Line Items.
    4. Set A single record is called a to Line Item.
    5. Select an icon to represent your table. 
    6. Provide a description such as This table tracks line items and connects orders and products.
    7. Select Create.
~~~

Instead of adding fields, select Cancel. The fields automatically created by Quick Base for every table are displayed. Shortly, you’ll import the Order Details.xlsx file containing the line item detail, and this will automatically create some fields for you!

But first, you need to build table-to-table relationships between the Line Items table, the Products table, and the Orders table. Once you master how to build table-to-table relationships, you will fully realize the power of Quick Base. 

[Next](relationships.html){: .btn .btn-purple }