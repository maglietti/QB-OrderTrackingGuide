---
layout: default
title: Table Relationships
nav_order: 5
---

# Understanding related data

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

## Create the Line Items Table

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

## Relate the line items and products tables

When adding line items to an order, you want to be able to simply pick a product number from a dropdown list and have the associated product name and unit price auto-fill for you. To make this work, connect the Line Items table to the Products table using a table-to-table relationship.

~~~
    1. In the left panel of the Line Items Settings page, select Table-to-table relationships. 
    2. If you see Use new experience at the top right of the page, make sure it is turned on.  
    3. In the top right section, select  
    4. Set Line Items connects to to Products. 
    5. Select the option that indicates Products may have many Line Items and select Next.
    6. Set Lookup 1 to Products-Product Name.
    7. Set Lookup 2 to Products-Unit Price.
    8. Select Create Relationship.
~~~

Congratulations! You just created the first table-to-table relationship in this app. 

## Relate the line items and orders tables

Create a table-to-table relationship between the Line Items table and the Orders table. Then you’ll import the Order Details.xlsx file, and line items will automatically connect to the orders in the Orders table.

~~~
    1. In the top right section, select + New Relationship.  
    2. Set Line Items connect to to Orders.
    3. Select the option that indicates Orders may have many Line Items and select Next. 
    4. On the next page, the reference field for Line Items defaults to Related Order. Do not make any changes. Select Next. 
    5. On the Add Lookup Fields page, set one lookup field to Orders - Customer Name. 
    6. Select Create Relationship. 
~~~

![](assets/images/relationships.png)

You now have two relationships. This will make creating line items within orders much simpler than manually maintaining a spreadsheet. We can tell you that, but seeing is believing. After you import the existing line items, you’ll create an order from scratch in the user interface. 

## Rename Fields

Now that you’ve connected these tables and added some lookup fields, this is a good time to rename some fields on the Line Items table. Quick Base automatically named some fields Related Products, Related Order, Product – Unit Price, and Order # - Customer Name, but those names might not make sense to users of this app. Rename those fields:

~~~
    1. In the left panel of the Line Items Settings page, select Fields.
    2. Select Related Products to adjust the field’s properties.
    3. For Label, replace Related Product with Product # and select Save.
    4. Select Related Order to adjust the field’s properties.
    5. For Label, replace Related Order with Order # and select Save.
    6. Without detailed instructions, change the labels of the following 2 fields:
~~~

|From|To|
|:---|:-|
|Order - Customer Name|Customer Name|
|Product - Unit Price|Unit Price|

~~~
    7. Select Exit Settings in the upper-left.
~~~

## Import the line items data

You’ve created the line items table and connected it to both the Products table and the Orders table. Now its time to populate this table with the data from Drew’s spreadsheet. Then you can say goodbye to those spreadsheets!

~~~
    1. From the Line Items table homepage, select More>Select Import/Export.
    2. Select Import into a table from a file.
    3. Confirm Select Table is set to Line Items, and Select Merge Field is set to Record ID.
    4. Without detailed instructions, import the copy of Order Details.xlsx you saved to your computer.
~~~

The next page displays the preview of your data. Set values as described below:

![](assets/images/itemsTable.png)

~~~
    1. Confirm First Row is List of Field Names is checked.
    2. Confirm the Order # column is set to be imported To Existing Field. 
    3. Change the Record Owner column from To Existing Field to Create New Field. 
        a. Confirm the FIELD LABELS value is Line #.
        b. Set FIELD TYPE to Text.
    4. Confirm the Product # column is set to be imported To Existing Field.
    5. Confirm the columns for product name and unit price are set to Do Not Import. That data is already in your Products table. 
    6. Confirm the Quantity column is set to Create New Field
        a. Confirm the FIELD TYPE is set to Numeric. 
        b. Confirm the FIELD LABELS is set to Quantity. 
    7. If other columns appear in your preview, do not import them. 
    8. Select Import. 
    9. A message is displayed warning the import will create 2 new fields. Select OK.
~~~

The resulting page indicates the number of records and fields created. Congrats! Your app now contains all the data from Drew’s spreadsheets. 

[Next](orderFormDesign.html){: .btn .btn-purple }