---
layout: default
title: Create Products Table
nav_order: 3
---

# Create your first Quick Base Table

Now it’s time to get the data into the app, data is stored in tables.  Tables are like spreadsheets, but better.  You can use them in a way that greatly reduces data entry and maintenance.  

## Review the product list spreadsheet

The first step when creating a new Quick Base app is to understand the data that we are working with. In our case, Drew provided us with three spreadsheet files, and since our first goal is to correct a product name let's start with the Product List spreadsheet. Opening the `ProductList.xlsx` file, we see that it has data in three columns and each column name is stored in the first row.

Open the spreadsheet and take a look at what what is stored inside.  

![](assets/images/prodTable.png)

Reviewing the spreadsheet, you write down the following notes:

| Column | Meaning | Type |
|:-|:-|:-|
| Product # | The product SKU | text |
| Product Name | The name of the product | text |
| Unit Price | The price | currency |

In Quick Base, you first describe what a table is going to store before we fill it with data. Let's take what we learned from the spreadsheet and configure a table to hold the product information.

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

<div markdown="span" style="padding: 1.25rem; margin-top: 1.25rem; margin-bottom: 1.25rem; border: 1px solid #eee; border-left-width: .25rem; border-radius: .25rem; border-left-color: #7253ed;" >
**Congratulations!** You created the first table in this app.
</div>

## Add a Product Using the + New Product Button

Before importing data from spreadsheets, let's test out the structure of your table manually. Add one product to the product table using the button Quick Base added when you created the table:

~~~
    1. Select `New Product`  
    2. Type product name: Flash Drive 64GB
    3. Type product #: FD0064
    4. Type unit price: 12.99
    5. Click Save & Close
~~~

Success! Now we are ready to get the rest of the products into the table and correct the product name. 

## Import the Products Spreadsheet

You prepared a table to hold the product information and added a product to the table by hand, now, let's import the rest of the products from the ProductList.xlsx file that Drew gave us:

~~~
    1. Click the Products table icon to view the homepage for this table  
    2. In the top right section of the page, select `More>Import/Export`
    3. In Choose Action, select `Import into a table from a file` 
    4. Confirm `Select Merge Field is set to Product #`
    5. _Without detailed instructions, upload the copy of Product List.xlsx you saved to your computer._  I don't understand this.
~~~

TODO
{: .label .label-red}
Screenshot

After you selected `Import From File`, the system displays a warning alerting you that importing data into a table that already contains data may update existing records. We know that there is only 1 product in the table – the flash drive you entered above. This product is not in Drew's spreadsheet, so no items will be updated. Select OK.

The next dialogue displays a preview of your data and acts like a staging area.

![](assets/images/importProdcuts.png)

This is our checklist to ensure that the data will import into the table the way that we want it to.

    1. Quick Base recognized that the spreadsheet contained field names and inserted those values in FIELD LABELS Row 1 of the table
    2. Quick Base assumed the spreadsheet data could be imported into existing fields 
    3. Click Import (with Update). 

TODO
{: .label .label-red}
Screenshot

Finally, a dialogue shows the results: 15 rows were read, 15 records were added, no records were updated, and there were no data rows with errors. **Success!**

Now, imagine what would happen if you accidentally uploaded that same spreadsheet with the same list of products into the app a second time ... would every product appear in the table twice, like shown here?

![](assets/images/dupData.png)

YUP! (...and we don't want that!) Quick Base requires that each table contains one field to use as a unique value for each record, this field is called the _key field_. If the uploaded data contains the same value of an item in the key field, it will update, vs. add, the record.  In our example, if Product # is the key field and the table already contains a record with `Product #` QC2019, Quick Base will not add another record with this value during an upload.  Instead, it will update the existing record.  This is a convenient way to quickly update values of many existing records, such as when you need to update pricing.

By default, Quick Base automatically creates a `Record ID#` field for every table and sets it as the key field.  This is useful if your data does not contain a field that will always contain unique values.  But because our Product # is always unique SKU, we can make that the key field and avoid duplicate entries in the future.

Here's how:

TODO
{: .label .label-red}
Describe how to get here

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

Ok, almost done with the Products table. Our last step is to take a look what is there and update that pesky wrong product name! Start by clicking the the Products table icon to view the homepage for this table.  

TODO
{: .label .label-red}
Screenshot

TODO
{: .label .label-red}
Provide the instructions to edit the product name here and remove it from the order form design page. 

TODO
{: .label .label-red}
Summary

[Next](createOrders.html){: .btn .btn-purple }