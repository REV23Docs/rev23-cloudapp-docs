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

Customer medical conditions can be securely stored and viewed from the customer profile. Only users with the `medical:customer` permission are able to view these to limit confidential information for those who need to know only.