# Service Types

Service Types are the types of procedures you perform at your studio.

## Category Types

REV23 has a set of core **Category Types**, the business scenarios that REV23 is meant to be used for. This list cannot be added to or changedd as Category Types control how the app behaves. They are:

- Tattoo
- Piercing
- Microblading
- Permanent Makeup
- Removal

Service Types are organized in a hierarchy by categories, and category types.

```text
Category Type
└─ Categories
    └─ Service Types
```

<a href="#categories"></a>

## Categories

Categories are customizable "folders" for you to organize your service types. For example, you would add Lobe, Helix and Tragus piercings to an **Ear** category.

|Field|Description|
|-|-|
|**Name**|The name of the category.|
|<a href="#category-types">**Category Type**</a>|The type of category.|

The **Category Type** is important as it acts as special instructions for how the app should treat the service types in that category. For example, hiding "Ink" and other tattoo related supplies in piercing service sessions.

## Types

Service Types are the actual names of the procedures you perform. By assigning them to the proper Category you control how the app treats the Service Type.

|Field|Description|
|-|-|
|**Name**|The name of the service type.|
|<a href="#categories">**Category**</a>|The category of the service type.|

## Users

You must assign your artists/technicians to service types so the app knows who does what! See [User Service Types](../concepts/users.md#service-types) for more information.

## Security

The permissions for creating/editing these objects are controlled by the `Service Config` permission set.
