# Medical Conditions

The list of medical conditions are displayed while filling out a release form in [Kiosk](../concepts/kiosk.md) and on the [Customer](../concepts/customers.md) profile page. From the customer profile page a user can also quickly add a new condition (i.e. Prone to Fainting) if a newly discovered condition pops up mid-session.

|Field|Purpose|
|-|-|
|**Name**|The name of the medical condition|
|**Condition Type**|The type of medical condition, **Allergy**, **Condition**, or **Disease**|
|<a href="#input-types">**Input Type**</a>| The type of entry for the condition. See below. |
|**Required**|Whether the entry of this condition is required.|
|**Display Order** (_hidden_)|You can control the position of the medical condition by dragging/dropping it to the desired position on both web and iPad platforms.|

<a href="#input-types"></a>

## Input Types

Input types control how the medical condition will appear to be entered.

|Type|Behavior|
|-|-|
|**Yes/No**|A yes or no box for the customer to select from. The rendered input of this condition changes depending on the **Required** setting. If Required, individual Yes & No buttons are displayed, no default is selected and the customer must choose one of them. If this condition is not required, an on/off switch is displayed, where the default value is no (off). |
|**Yes/No & Text**|The same as a Yes/No input type with an additional text field to collect additional data (i.e. "Medications")|
|**Text**|A text field for the customer to type any additional data (i.e. "Other")|

## Security

There is a special `medical:customer` permission for [Users](../concepts/users.md) which controls the ability to see a customer's medical conditions in their profile.

The permissions for creating/editing these objects are controlled by the `Medical` permission set.
