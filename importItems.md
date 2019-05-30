---
layout: default
title: Import Line Items
nav_order: 7
---

# Import the line items data

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

## View an Order

Check out the power of table relationships by viewing an order:

~~~
    1. Select the Orders table.  
    2. Select order 444111 to view it. 
    3. All three line items for this order are displayed.
~~~

Technically speaking, the order’s information is displayed on a form. The top of the form shows the fields for order number, customer name, and order date. The bottom of the form is a report that is pulling data from the Line Items table. Behind the scenes, Quick Base created this report and named it Embedded for Orders because it is embedded on the Orders form. The report is good, but notice that line items and quantities are not displayed. So you need to make a minor adjustment to this report. 

[Next](orderFormDesign.html){: .btn .btn-purple }