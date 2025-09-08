# Users

REV23 supports user accounts each with a password and unique permissions. Each service provider in your studio requires a user account. As a general rule you should also create a user account for each person that uses the app, **even counter staff.**

> **WHY ARE SHARED ACCOUNTS BAD?** Though it may be tempting to create a single "counterstaff" user account we strongly discourage it. First and most importantly, if you have a member of your staff leave, they still have access to your app with that shared password. Unless you remember to change that account password if/when someone leaves your business, and let's face it, you probably won't, you have a huge security risk since you cannot simply deactivate the account of the departing user. Additionally, most records are stamped with when they were created and modified, as well as by whom. Having a shared account reduces the usefulness of this data as you cannot track a change back to a single individual.

## Types of accounts

REV23 supports two login types.

1. [REV23 ID](rev23-id.md) (how you log onto REV23 website/software/services)

2. Username/Password stored in your tenant database

Subscription owners always use their REV23 ID to access their app. Other accounts you create are accessed via a username/password that are stored only in your database.

Using REV23 ID is fast and secure and offers a few benefits. For example, if you have multiple subscriptions you can quickly switch between them, likewise if you have only one tenant, it will automatically know which tenant to log you in to, so you don't need to type the name.

On the login screen of the app you will see the two login options. Choose the appropriate login method. In general, the owner will use REV23 ID, artists and counter staff will use a username/password.

> **REV23 ID Guest Accounts**: Users can link their REV23 ID to their user account by ensuring that the email addresses match. Upon their initial login attempt using REV23 ID, their accounts will automatically link. This action adds them as a guest to your tenant, enabling streamlined login experiences without the need to enter the tenant name repeatedly. Guests can easily switch between multiple tenants they have access to.

## Security

<a href="#permissions"></a>

### Permissions

REV23 supports an extensive set of permissions, limiting users to exactly the data they should and should not see. You should assign each user only the permissions they absolutely need to use the app.

When assigning permissions they are grouped by object type (Customers, Services, etc..) and a set of permissions for each type. While some object types have special permissions, most have this common set.

| Permission  | Description                          |
| ----------- | ------------------------------------ |
| `CREATE`    | The user is able to create an object of the type.  |
| `READ`      | The user is able to read (view) an object of the type. |
| `WRITE`     | The user is able to write (change, update, edit) an object of the type. |
| `DELETE`    | The user is able to delete an object of the type. |
| `NAVIGATE`  | This is a user interface level permission only. If the user has a navigate permission, it is generally associated with being able to see that object in the app's menu to "navigate" to. This is useful for if a user needs permissions to enter data such as needles used into a service session, but don't want to complicate their user interface with settings they never need to go change. In this case you can grant the Read permission, but turn off Navigate.  |

> There are cases where you will not see a `Read` permission for a particular type. Because some data is required to use the app at all, studio name for example, some permissions are implied automatically for every user account, even if you have not assigned any permissions.

#### Additional permission types

Some object types, such as Customer, have additional permission types outside of the core CRUD (create, read, update, delete) set.

For example:

| Permission  | Description                          |
| ----------- | ------------------------------------ |
| `EXPORT`    | Allows the user to export the customer list to CSV.  |
| `MEDICAL`   | Allows the user to see confidential medical information for the customer.  |

## Seats

REV23 uses "seats" for how we charge for the app. The base subscription comes with x seats. You need to add an additional seat for each _service providing_ user in your studio.

> You do not need seats for all users, only users that perform services. Meaning you do not need to pay for seats for counter staff, managers, etc...

When filling out a form in Kiosk only users who have been assigned seats are visible to the customer to choose from.

To assign a seat, open the user and toggle the "Assign Seat" switch. **When a user is assigned a seat, you cannot unassign them from that seat for 48 hours.** This is to prevent abuse of our licensing by assigning/unassigning users as needed between Kiosk sessions.

<a href="#service-types"></a>

## Service Types

To function properly, REV23 needs to understand the relation between Users and the [Service Types](../settings/service-types.md) they perform.

This is done through licenses, which represent the licenses issued by your local health department, including the license number and expiration dates. *Expiration notifications coming soon!

There are two ways to add a license depending on your needs.

### Category Licenses

You can assign a category license which just like a license issued from your health department allows you to perform all services in those categories (Tattoo, Piercing, PMU, Microblading, Removal).

As a general rule, assigning category licenses is easiest because one switch controls them all.

This is most useful for piercings where there are far more service types in that category than any other. By assigning the Piercing category license, the user is automatically assigned to any piercing service.

### Service Type Licenses

For more control, you can assign licenses for specific service types. Again, most useful for piercing, if you have piercers that do not perform specific types of piercings that you offer you will want to avoid assigning them a category license and instead just add the piercings they do perform here. Or perhaps you have one PMU artist that specialize in areola restoration, but no other PMU artist performs this service.

## Signature

You may provide a default signature for providers to apply to release forms. This is useful if your form requires the provider signature but you do not require it be signed each time. Set the signature in the user page in the app. You may then disable the "Require provider signature" setting in the [Template Designer](../template-designer/index.md). If that setting is enabled it will always use the signed version  from Kiosk rather than this default.

## Studios

If you have multiple [studios](../settings/studios.md), you can assign users to only the locations they actually work at to limit whether or not they appear in the [Kiosk](kiosk.md) flow. You do not need to explicitly set studios for users, users with no studio mapping will always appear.

## Webhooks

Users support the following [webhook](./webhooks.md) events:

|Event|Permission|Description|
|-|-|-|
|**user_created**|read:user| A user object was created. |
