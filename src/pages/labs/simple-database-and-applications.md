---
title: Simple Database and Applications
description: Simple Database and Applications
hide_table_of_contents: false
---

# Simple Database and Applications

In this lab exercise, you will create a simple 
e-commerce database
and applications using Google AppSheet.

## Create the Database

1. Sign in the Google account that you want to use for this exercise.
1. Go to [Google AppSheet](https://www.appsheet.com).
1. Go to "Create | Database | New database".
1. If this is your first time using AppShet:
    1. Click the "Get Started" button.
    1. Click through the tutorial, if you like.
1. Click on "+ Add column".
1. For "Name", enter "Email".
1. For "Type", choose "Email".
1. Click on the "Save" button.
1. Click on "+ Add column".
1. For "Name", enter "Quantity".
1. For "Type", choose "Number".
1. Click on the "Save" button.
1. Click on "+ Add column".
1. For "Name", enter "Colour".
1. For "Type", choose "Color".
1. Check all the colours.
1. Click on the "Save" button.
1. Click on "+ Add column".
1. For "Name", enter "Item".
1. For "Type", choose "Enum".
1. Click on the "Add value" button.
1. Enter "Plate".
1. Click on the "Add value" button.
1. Enter "Bowl".
1. Click on the "Add value" button.
1. Enter "Cup".
1. Uncheck "Allow other values".
1. Click on the "Save" button.
1. Drag the existing "Status" column to the very end.
1. Click the 3 dots next to the "Assignee" column and choose "Delete column".
1. Delete the "Date" column.
1. Click the 3 dots next to the "Email" column and choose "Use column as label".
1. Delete the "Title" column.
1. Right-click just to the left of "1" for row 1 and choose "Delete row".
1. Delete the other 3 rows.
1. Click the 3 dots next to "Table 1" and choose "Table settings".
1. Change the table name to "Order".
1. Click on the "Save" button.
1. Click inside "Untitled database".
1. Change the database name to "Store".
1. Click on the main AppSheet icon.

## Create the Order Application

1. Go to "Create | App | Start with existing data".
1. For "App name", enter "New Order".
1. For "Category", choose "Other".
1. Click the "Choose your data" button.
1. Choose "AppSheet Database".
1. Choose "Store".
1. We only want this app to add new order records, so uncheck "Update" and "Delete" to the right of "Order".
1. Confirm that only "Add" shows to the right of "Order".
1. Click on the "Create app" button.
1. Click on the "Customize with AppSheet" button.
1. Click on the "Views" icon on the far left toolbar (it looks like a little mobile phone).
1. Under "View type", choose "form". This becuase we want to present
    a fill-out form by default to the customer.
1. Under "Finish view" choose "Order_Detail". This will summarize the order
    for the customer.

### Customize the Email field

1. Hover over the "Email" field in the app preview. Click on the edit
    icon (looks like a little pencil). Choose "Edit Column".
1. Expand the "Data Validity" section.
1. Check the "Require?" checkbox.
1. Expand the "Auto Compute" section.
1. Click inside the "Initial value" field area.
1. Choose the "Other" tab.
1. Way over to the far right of the "USEREMAIL()" pattern, choose "Insert".
1. Click on the "Save" button.
1. Expand the "Update Behavior" section.
1. Uncheck "Editable?". We just want to fill in the email field with the
    customer's logged in email. We don't want them to change it.
1. Scroll to the top of the dialog box.
1. Click the "Done" button at the top right.

### Customize the Quantity field

1. Hover over the "Quantity" field in the app preview. Click on the edit
    icon (looks like a little pencil). Choose "Edit Column".
1. For "Maximum value" enter "10".
1. For "Minimum value" enter "1".
1. For "Increase/decrease step" enter "1".
1. Expand the "Data Validity" section.
1. Check the "Require?" checkbox.
1. Expand the "Auto Compute" section.
1. Click inside the "Initial value" field area.
1. In the "Enter an expression" area, enter "1" (no quotes).
1. Click on the "Save" button.
1. Scroll to the top of the dialog box.
1. Click the "Done" button at the top right.

### Customize the Colour field

1. Hover over the "Colour" field in the app preview. Click on the edit
    icon (looks like a little pencil). Choose "Edit Column".
1. Expand the "Data Validity" section.
1. Check the "Require?" checkbox.
1. Expand the "Auto Compute" section.
1. Click inside the "Initial value" field area.
1. In the "Enter an expression" area, enter "Red" (yes, include the 
    quotes here).
1. Click on the "Save" button.
1. Scroll to the top of the dialog box.
1. Click the "Done" button at the top right.

### Customize the Item field

1. Hover over the "Item" field in the app preview. Click on the edit
    icon (looks like a little pencil). Choose "Edit Column".
1. Expand the "Data Validity" section.
1. Check the "Require?" checkbox.
1. Expand the "Auto Compute" section.
1. Click inside the "Initial value" field area.
1. In the "Enter an expression" area, enter "Plate" (yes, include the 
    quotes here).
1. Click on the "Save" button.
1. Scroll to the top of the dialog box.
1. Click the "Done" button at the top right.

### Customize the Status field

1. Hover over the "Status" field in the app preview. Click on the edit
    icon (looks like a little pencil). Choose "Edit Column".
1. Expand the "Data Validity" section.
1. Check the "Require?" checkbox.
1. Expand the "Auto Compute" section.
1. Click inside the "Initial value" field area.
1. In the "Enter an expression" area, enter "Not Started" (yes, include the 
    quotes here).
1. Click on the "Save" button.
1. Expand the "Update Behavior" section.
1. Uncheck "Editable?". The initial status for an order is always
    "Not Started" and we don't want the customer to be able to change it.
1. Scroll to the top of the dialog box.
1. Click the "Done" button at the top right.

### Finishing up the App

1. Click the big "SAVE" button at the top right to save your changes so far.
1. In the toolbar on the far left, click on the "Data" icon (the one
    just above the "Views" icon).
1. For the "Status" field, uncheck the "Show?" attribute. The customer
    doesn't need to see this field.
1. In the toolbar on the far left, click on the "Settings" icon (looks
    like a gear).
1. Under "App Properties" turn on the "Personal use only?" setting.
1. Click the big "SAVE" button at the top right to save your changes.

### Deploying the App

1. In the toolbar on the far left, click on the "Deploy" icon (looks
    like a rocket).
1. Click "Deployment Check".
1. Scroll down. It looks like there is an error. You can click the
    "ERROR" button to see the details. For personal use apps, this
    is not a problem.
1. Click the "Move app to deployed state despite errors" button.

### Running the App

1. In the toolbar at the top, click on the "Share" icon (looks 
    like a "+" sign next to a head-and-shoulders icon).
1. Click on "Copy sharing links" and copy "Browser Link".
1. In a new browser tab, paste the link.
1. Click on "Save" to place the first order (1 red plate).
1. Use the back arrow to go back to the order form.
1. Change the fields for 3 green Cups.
1. Click on "Save" to place the second order.
1. In another tab, go back to the AppSheet main page.
1. Go to "Databases | Store".
1. Verify that there are 2 orders in the Order table.

## Create the Process Order Application

1. Click on the main AppSheet icon.
1. Go to "Create | App | Start with existing data".
1. For "App name", enter "Process Order".
1. For "Category", choose "Other".
1. Click the "Choose your data" button.
1. Choose "AppSheet Database".
1. Choose "Store".
1. We only want this app to update existing order records, 
    so uncheck "Add" and "Delete" to the right of "Order".
1. Confirm that only "Update" shows to the right of "Order".
1. Click on the "Create app" button.
1. Click on the "Customize with AppSheet" button.
1. In the toolbar on the far left, click on the "Data" icon (the one
    just above the "Views" icon).
1. Uncheck "EDITABLE?" for "Email", "Quantity", "Colour", and "Item" fields.
1. Only Status should be "EDITABLE?" checked.

### Only Show "Not Started" Orders

1. Click on the "Views" icon on the far left toolbar 
    (it looks like a little mobile phone).
1. Click on the "Use slices to filter your data" link.
1. Click the "Create a new slice for Order" button.
1. Click in the "Row filter condition" field.
1. Click the "Create a custom expression" link.
1. In the "Enter an expression" area, enter:
    ```
    [Status] = "Not Started"
    ```
1. Click the "Save" button.
1. Click the "Done" button at the top right.
1. Click the big "SAVE" button at the top right.

### Finishing up the App

1. In the toolbar on the far left, click on the "Settings" icon (looks
    like a gear).
1. Under "App Properties" turn on the "Personal use only?" setting.
1. Click the big "SAVE" button at the top right to save your changes.

### Deploying the App

1. In the toolbar on the far left, click on the "Deploy" icon (looks
    like a rocket).
1. Click "Deployment Check".
1. Scroll down. It looks like there is an error. You can click the
    "ERROR" button to see the details. For personal use apps, this
    is not a problem.
1. Click the "Move app to deployed state despite errors" button.

### Running the App

1. In the toolbar at the top, click on the "Share" icon (looks 
    like a "+" sign next to a head-and-shoulders icon).
1. Click on "Copy sharing links" and copy "Browser Link".
1. In a new browser tab, paste the link.
1. Select one of the "Not Started" orders.
1. Click on the "Edit" button.
1. Change the "Status" to "Complete".
1. Click the "Save" button.
1. Notice the order disappears from the "Not Started" list!
1. In another tab, go back to the AppSheet main page.
1. Go to "Databases | Store".
1. Review the "Status" of each order.
