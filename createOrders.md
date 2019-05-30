---
layout: default
title: Create Orders Table
nav_order: 4
---

# Create an Orders Table

The Order List.xlsx spreadsheet has three columns: Order Date, Customer Name, and Order Number. Here’s a look at the first four records in the spreadsheet. 

![](assets/images/ordersTable.png)

You may wonder if you must add a new table in the app for this data, or if you can add it to an existing table. This is a question you must answer for any data you will track in your app. To decide, you should ask yourself two questions: Do I track many of these? Do I track many things about these? If the answer is yes to both, then create a table. 

In this example, the answer is yes to both. You track many orders, and you track many things about them – order date, customer name, and order #. So create a table to contain the order data:

~~~
    1. Select + New Table.  
    2. Select From scratch - Design your own table.
    3. Name the table Orders.
    4. Set A single record is called a to Order.
    5. Select an icon to represent your table. 
    6. Provide a description such as List of customer orders.
    7. Select Create.
~~~

Next add the fields of the table. These correlate to the column headings in the spreadsheet. 

![](assets/images/ordersFields.png)

~~~
    1. Type field labels Order #, Customer Name, Order Date. 
    2. Set the data types to Text, Text, and Date, respectively, as shown above. 
    3. Select Add. 
~~~

Next change the key field of this table. You did this for the products table, but each table has its own key field. By default, Quick Base automatically creates a Record ID# field for every table and sets it as the key field. But in our Orders List spreadsheet, Order # is unique, so make that the key field:

![](assets/images/ordersKeyField.png)

~~~
    1. Select the checkbox for Order #.
    2. Select Set Key.
    3. Follow the prompts (not shown above) to confirm this change. The key icon should now be next to the Order # field.  
    4. Select Exit Settings.
~~~

## Import Orders from the File

Now import the orders from the Order List.xlsx file you saved earlier:

~~~
    1. From the Orders table homepage, select More > Import/Export.
    2. Select Import into a table from a file.
    3. Confirm Select Table is set to Orders and Select Merge Field is set to Order #.
    4. Without detailed instructions, upload the copy of Order List.xlsx you saved to your computer.
    5. The system displays a warning. Select OK.
~~~

A preview of your data is displayed. As before, Quick Base has made the correct assumptions about how to import the data, so no changes are needed. Select Import (with Update). 

A page shows the results: 67 data rows were read, 67 new records were created, 0 existing records were updated, and there were 0 data rows with errors. The import was successful, and your app now contains the data from the Order List.xlsx file. 

[Next](createItems.html){: .btn .btn-purple }