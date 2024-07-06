# Tattoo Settings

Objects used for tattoo based services are discussed here. These objects are mostly just lookup objects, meaning simple objects you can select from a list for data consistency and so you don't need to type in a value each time. As such there is little to discuss here as they mostly just contain a name field.

These objects are used for recording supplies used in **Tattoo**, **Microblading**, **Permanent Makeup** and **Removal** [Service Sessions](../concepts/services.md).

<a href="ink"></a>

## Ink
Store your ink for adding to a service session, recording the expiration date and lot number.

Ink is a bit more detailed object than others in this list as it contains multiple fields.

|Field|Description|Example|
|-|-|-|
|**Name**|The _actual_ name of the ink.|Mediterranean Sea|
|<a href="#ink-colors">**Color**</a>|The _base_ color of the ink.|Blue|
|<a href="#ink-manufacturers">**Manufacturer**</a>|The manufacturer of the ink.|World Famous|

!!! tip "Use the Ink Feed from Painful Pleasures"

    You can import ink to add some of the most popular brands courtesy of [Painful Pleasures](https://painfulpleasures.com)! Use the Import action and select your favorite brands to add them quickly. New ink color released or did you start using a new brand? Import again, the list changes as they add new products to their catalog!

<a href="#ink-colors"></a>

### Colors
Ink colors are base colors of ink. Green, Red, Blue, Purple, etc... these are not meant to be the specific names of ink. That is what the **Name** field of the Ink object is for. When searching for ink to add to a session you can easily filter by these colors. There is little reason to add to or edit this list as we have most bases covered here.

<a href="#ink-manufacturers"></a>

### Manufacturers
Manufacturers (brands) of inks. When searching for ink to add to a session you can easily filter by these manufacturers.

## Tubes
Tubes. Only a **Name** field is required. When adding to a session you are prompted for the lot number and expiration date.

## Grips
Grips. Only a **Name** field is required. When adding to a session you are prompted for the lot number and expiration date.

## Salves
Salves. Only a **Name** field is required.

## Security
The permissions for creating/editing these objects are controlled by the `Tattoo Config` permission set.