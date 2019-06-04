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

In Quick Base, you first describe what a table is going to store before filling it with data. Let's take what we learned from the spreadsheet and configure a table to hold the product information.

![](assets/images/newTable.png)

~~~
    1. Click the `New Table` button from the navigation bar
    2. Click `From scratch - Design your own table`
    3. Name the table: Products
    4. A single record is called a: Product
    5. Select an icon to represent your table - we chose the hand cart
    6. Provide a description: List of products we sell
    7. Click the `Create` button
~~~

Creating the table is the first half of the process, now we have to describe the data that the table will hold. Add fields to the table based on what we observed in Drew's spreadsheet.  

![](assets/images/newFields.png)

~~~
    1. Fill in a `Field Label` for each of the column names from the spreadsheet
    2. Select the data type for each field based on what we observed
    3. Click the `Add` button
~~~

SCREENSHOT and EXIT SETTINGS
{: .label .label-red }

<div markdown="span" style="padding: 1.25rem; margin-top: 1.25rem; margin-bottom: 1.25rem; border: 1px solid #eee; border-left-width: .25rem; border-radius: .25rem; border-left-color: #7253ed;" >
**Congratulations!** You created the first table in this app.
</div>

## Add a product using the new product button

Before importing data from spreadsheets, let's test out the structure of your table manually. Add one product to the product table using the button Quick Base added when you created the table:

~~~
    1. Select `New Product`  
    2. Type product name: Flash Drive 64GB
    3. Type product #: FD0064
    4. Type unit price: 12.99
    5. Click Save & Close
~~~

Success! Now we are ready to get the rest of the products into the table and correct the product name. 

## Import the products spreadsheet

You prepared a table to hold the product information and added a product to the table by hand, now, let's import the rest of the products from the ProductList.xlsx file that Drew gave us:

THIS WORKFLOW IS WRONG
{: .label .label-red}

~~~
    1. Click the Products table icon to view the homepage for this table  
    2. In the top right section of the page, select `More>Import/Export`
    3. In Choose Action, select `Import into a table from a file`
    4. Confirm `Select Merge Field is set to Product #`
    5. Without detailed instructions, upload the copy of ProductList.xlsx you saved to your computer.  ***I don't understand this***
~~~

Screenshot
{: .label .label-red}

After selecting `Import From File`, the system displays a warning alerting you that importing data into a table that already contains data may update existing records. We know that there is only one product in the table – the flash drive you entered above. This product is not in Drew's spreadsheet, so no items will be updated. Click OK.

The next dialogue displays a preview of your data and acts like a staging area.

![](assets/images/importProdcuts.png)

    1. Quick Base recognized that the spreadsheet field
    2. Quick Base assumed the spreadsheet data could be imported into existing fields 
    3. Click Import (with Update)

Screenshot
{: .label .label-red}

Finally, a dialogue shows the results: 15 rows were read, 15 records were added, no records were updated, and there were no data rows with errors. **Success!**

What would happen if you accidentally uploaded that same spreadsheet with the same list of products into the app a second time ... would every product appear in the table twice, like shown here?

![](assets/images/dupData.png)

YUP! (and we don't want that!) Quick Base requires that each table contains one field to use as a unique value for each record, this field is called the _key field_. If the uploaded data contains the same value of an item in the key field, it will update, vs. add, the record.  In our example, if Product # is the key field and the table already contains a record with `Product #` QC2019, Quick Base will not add another record with this value during an upload.  Instead, it will update the existing record.  This is a convenient way to quickly update values of many existing records, such as when you need to update pricing.

By default, Quick Base automatically creates a `Record ID#` field for every table and sets it as the key field.  This is useful if your data does not contain a field that will always contain unique values.  But because our Product # is always unique SKU, we can make that the key field and avoid duplicate entries in the future.

Here's how:

Describe how to get here
{: .label .label-red}

![](assets/images/keyField.png)

~~~
    1. Check the checkbox for Product #
    2. Click `Set Key`
    3. Follow the prompts (not shown above) to confirm this change. 
       The key icon should now be beside the  Product # field.  
    4. Click `Exit Settings` in the top left section of the screen.
~~~

Your future self will thank you for setting this up now. 

## View the Table Report

Ok, almost done with the Products table. Our last step is to take a look what is there and update that pesky product name! Start by clicking the the Products table icon to view the homepage for this table.  

Screenshot
{: .label .label-red}

## Update a Record

Now that your app is up and running, use it to correct the product name in the product list. First look at the product list to confirm it is incorrect, as your team members reported:

Change to use grid edit ~ more familiar to a spreadsheet user
{: .label .label-red }

~~~
    1. Select the Products table.
    2. In the Search, enter CA.
    3. The results show 2 cables. The product name for CA8018 is incorrect. 
    4. Select the pencil icon to the left of the Product Name. 
    5. The page refreshes. Look at how many orders contain this cable and the incorrect product name.
    6. At the top of the page, change the product name to Cat 8 Cable 8ft.
    7. Select Save & close.
    8. Select the pencil icon for CA8018 again to view the orders for this product. Notice that all the orders now reflect the updated product name. 
~~~

In just a few clicks, you updated this product name in the products table and on all orders. 

Summary
{: .label .label-red}

[Next](createOrders.html){: .btn .btn-purple }