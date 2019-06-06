---
layout: default
title: Create Products Table
nav_order: 3
---

# Create your first Quick Base table

Quick Base stores data in tables. Tables are like spreadsheets, but better.  Understanding how tables work is the first step in your journey to creating an app.  

## Review the product list spreadsheet

Drew provided three spreadsheet files, and since our first goal is to correct a product name let's start with the Product List spreadsheet. Opening the `ProductList.xlsx` file, we see that it has data in three columns. The name for each column is stored in the first row.

Open the spreadsheet and take a look at what what is stored inside.  

![](assets/images/prodTable.png)

Reviewing the spreadsheet, you write down the following notes:

| Column | Meaning | Type |
|:-|:-|:-|
| Product # | The product SKU | text |
| Product Name | The name of the product | text |
| Unit Price | The price | currency |

In Quick Base, you first describe what a table is going to store before filling it with data. Let's take what we learned from the spreadsheet and configure a table to hold the product information. Start by clicking the **New Table** button from the app navigation bar and selecting **From scratch - Design your own table.**

![](assets/images/newTable.png)

Configure the table by giving it a name and information that describe how it will be used.

~~~
    3. Name the table: Products
    4. A single record is called a: Product
    5. Select an icon to represent your table - we chose the hand cart
    6. Provide a description: List of products we sell
    7. Click the `Create` button
~~~

Creating the table is the first half of the configuration process, next we describe the table fields and what they store. Add fields to the table based on what we observed in Drew's spreadsheet.  

![](assets/images/newFields.png)

~~~
    1. Fill in a `Field Label` for each of the column names from the spreadsheet
    2. Select the data type for each field based on what we observed
    3. Click the `Add` button
~~~

<div markdown="span" style="padding: 1.25rem; margin-top: 1.25rem; margin-bottom: 1.25rem; border: 1px solid #eee; border-left-width: .25rem; border-radius: .25rem; border-left-color: #7253ed;" >
**Congratulations!** You created the first Quick Base table!
</div>

SCREENSHOT
{: .label .label-red }

## Import the products spreadsheet

Let's import the products from the ProductList.xlsx file that Drew gave us:

THIS WORKFLOW IS WRONG
{: .label .label-red}

~~~ 
    1. In the top right section of the page, click `Import/Export`
    2. In Choose Action, select `Import into a table from a file`
    3. Leave Select Merge Field set to Record ID#
    4. Click the `Choose File` button and navigate to the `ProductList.xlsx`
    5. Click the `Import From File...` button
~~~

Screenshot
{: .label .label-red}

The **Import** dialogue allows you to configure how the file is imported

![](assets/images/importProdcuts.png)

    1. The first row of Drew's spreadsheet contains the Field Names, make sure this is checked.
    2. We have already defined the fields and we want the data imported to them
    3. Look at the data and field names and make sure they are like the spreadsheet
    3. Click the `Import` button

Screenshot
{: .label .label-red}

Finally, a dialogue shows the results: 14 rows were read, 14 records were added, no records were updated, and there were no data rows with errors. 

<div markdown="span" style="padding: 1.25rem; margin-top: 1.25rem; margin-bottom: 1.25rem; border: 1px solid #eee; border-left-width: .25rem; border-radius: .25rem; border-left-color: #7253ed;" >
**Success!** You have imported your first spreadsheet to Quick Base
</div>

As an aside, what do you think would happen if you accidentally uploaded that same spreadsheet with the same list of products into the app a second time ... would every product appear in the table twice, like shown here?

![](assets/images/dupData.png)

YUP! (and we don't want that!) Quick Base requires that each table contains one field to use as a unique value for each record, this field is called the _key field_. If the uploaded data contains the same value of an item in the key field, it will update, vs. add, the record.  In our example, if Product # is the key field and the table already contains a record with `Product #` QC2019, Quick Base will not add another record with this value during an upload.  Instead, it will update the existing record.  This is a convenient way to quickly update values of many existing records, such as when you need to update pricing.

By default, Quick Base automatically creates a `Record ID#` field for every table and sets it as the **key field.**  This is useful if your data does not contain a field that will always contain unique values.  But because our Product # is always unique SKU, we can make that the key field and avoid duplicate entries in the future.

Here's how:

~~~
    1. Click the icon for the Products table in the App nav bar
    2. Click the gear icon in the blue box next to the `Products > Products Home` breadcrumb
    3. Click `Fields (8)` in the **Table Structure** group
~~~

Let's set the `Product #` field to be the **Key** for the Products table.

![](assets/images/keyField.png)

~~~
    1. Check the checkbox for Product #
    2. Click `Set Key`
    3. Click the `Set Key` button in the pop-up  
    4. Verify that the gold key moved to the `Product #` field
    4. Click `Exit Settings` in the top left section of the screen.
~~~

Your future self will thank you for setting this up now. 

## View the Table Report

Ok, almost done with the Products table. Our last step is to take a look what was imported and update that pesky product name! Start by clicking the the Products table icon to view the homepage for this table. Note that whenever you click on a table button in the app nav bar, it will display the default _table report_ in the table's **Home** page. 

Screenshot
{: .label .label-red}

## Update a Record

We can easily see the wrong product name in the table, we can correct the product name in the product list from the home page. 

We are looking for Product # `CA6018` which has the wrong product name `Cat 9 Cable 10ft`, this is really a Cat 6 cable. 

~~~
    2. In the Search bar, enter CA6018.
    3. The table shows only the one product that matches 
    4. Click the `Grid Edit` button in the app nav bar 
    5. Double click on the wrong product name
    6. Correct the product name
    7. Click the green Save button
    8. Verify that the product name was updated 
~~~

In just a few clicks, you updated this product name in the products table now it will be correct in all of the orders. 

Summary
{: .label .label-red}

[Next](createOrders.html){: .btn .btn-purple }