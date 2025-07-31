# Customers

Customers represent ... ok look, you know what a customer is. Here's the important stuff to know.

## Creating Customers
In general customers are mainly meant to create themselves via [Kiosk](kiosk.md). In fact, currently iPad doesn't have a "New Customer" button.

## Importing Customers

You can import a CSV (comma separated values) file of your customers from a number of existing relevant apps.

> Only customer profile information is imported, not history.

If we do not have support for the app you wish to import from, you can format your CSV file to match our layout and use the `Other` file type.

Your CSV file must have a header and column names must match our expected values. Rename any column from your existing file to match our expected values, for example if the CSV you wish to import uses `First Name` as the column for a customer's first name, you must change that to be `FirstName` (without a space) for REV23 to import the file. The order does not matter. The **bold** fields below are required to be in the file, though they don't necessarily need data in them.

- **FirstName**
- **LastName**
- **Email**
- **PhoneNumber**
- **Birthdate**
- MiddleName
- Nickname
- Gender
- Street
- City
- State
- PostalCode
- Country
- Occupation
- Notes

## Exporting Customers

Likewise, you can export your customer list to CSV. Nothing much here. The big thing to note is a user must be assigned the `export:customer` permission to perform this operation.

## Medical Conditions

Customer medical conditions can be securely stored and viewed from the customer profile. Only users with the `medical:customer` permission are able to view these to limit confidential information for those who need to know only. See [Medical Conditions](../settings/medical-conditions.md) for more information.

## Flags

Customers can be flagged for past behavior to alert you to a potential issue. You can apply multiple flags to a customer and will see a visual indicator in the customer record when a flag is present. See [Flags](../settings/flags.md) for more information.

## Merging Duplicate Customers

There are two methods for merging a duplicate customers.

1. In the Customer List select **Find Duplicates** (currently iOS only). This will search for customers that have the same birthdate and last name, showing you the first that was created. Tapping that customer will show you the found duplicates, allowing you to select each that you wish to merge.

2. In a Customer Detail screen select **Merge Duplciates** to show customers that have the same birthdate and last name. This will merge the select customers into the the target that was opened.

This will merge services, notes, files and more, as well as attempt to fill gaps in the data, using the most recent entered information first.

# Webhooks

Customers support the following [webhook](./webhooks.md) events:

|Event|Permission|Description|
|-|-|-|
|**customer.created**|read:customer| A customer object was created. |