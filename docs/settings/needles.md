# Needle Settings

Needles used for tattoo & piercing based services are discussed here.

These objects are used for recording supplies used in **Tattoo**, **Microblading**, **Permanent Makeup** and **Removal** [Service Sessions](../concepts/services.md).

Store your needles for adding to a service session, recording the expiration date and lot number.

A needle is a bit more detailed object than others as it contains multiple fields.

|Field|Purpose|Example| .. or |
|-|-|-|-|
|**Name**|The name of the needle|8RL|20g 4mm|
|**Manufacturer**|The manufacturer of the needle.|Peak|Precision |
|**Service Categories**|The service categories of the needle.|Tattoo|Piercing|

> **Service Categories Note:** The Categories field can accept multiple Category Types, for example needles that are used in Tattooing and Permanent Makeup.

## Properties

### Manufacturers

Manufacturers (brands) of needles. When searching for ink to add to a session you can easily filter by these manufacturers.

## Security

The permissions for editing these objects are controlled by the `Needle Config` permission set.
