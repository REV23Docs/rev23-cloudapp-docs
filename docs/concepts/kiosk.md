# Kiosk

Kiosk Mode is a special, passcode protected view in the app for your customers to fill out a form. While in this mode your customer cannot access other areas of the app.

For additional protection you can enable Guided Access from your iPad Settings to prevent customers from accessing other areas of the iPad, disabling the Home button, swiping to exit, etc...

## Entering & Exiting Kiosk

From iPad you can enter Kiosk Mode from the Menu button. If a user has access to log onto the app, they are able to put the app in Kiosk mode. The user does not need permissions for anything additional to run Kiosk, for example, they do not need Create Customer permissions, as Kiosk Mode runs in as it's own special user that has only the permissions required to fill out a release form.

**To exit Kiosk Mode** on your iPad tap the Exit button in the upper-right hand corner.

You will then be prompted for your passcode and can exit this mode, returning you to the main app.

## Flow

Kiosk uses [templates](./templates.md) to control the flow of the form, though some steps are not configurable or skippable.

### Service Selection

A customer is first prompted with the service they wish to have done. First by selecting the Category Type (Tattoo, Piercing, etc...), then by Service Type.

You can select multiple service types, as long as they are in the same type category. For example, you can combine multiple piercings, but you cannot combine a tattoo and a piercing and two forms will need to be filled out.

Only service types which have a [mapping](../settings/templates/mappings.md) and [users](users.md#service-types) with an assigned seat will appear in this list.

One or both of these steps are skipped if:

- There is only one (1) detected category, i.e. if you are a tattoo only studio, the category selection will be skipped
  - and/or
- There is only one detected service type in the category. For example, if you only have one (1) tattoo service type in the category, the service type selection will be skipped after the category is selected.

### User Selection

After a service type is selected, the customer is presented with a list of users to select who is performing the service.

A user will only appear in this list if...

- They have a seat assigned.
- They have a category or service type license for the selected service type.
- If you have multiple studios, they have a studio assignment in the current studio, or, have zero studio assignments, meaning they are in all.

This step is skipped if there is only one user detected as having a seat and assigned to the selected service type.

Additionally, an "IDK" (I don't know) user appears if there are two or more users in this list. This allows them to proceed with the form without knowing who will perform the service. This is useful for studios where staff decides who will be the performing provider.

### Customer Entry

A customer is then prompted to enter their details. This can be done in one of a few ways.

1. A customer can scan the two-dimensional PDF417 barcode on the back side of their AAMVA issued identification. If successful, key information such as the customer's name, birthdate & address are extracted from the barcode and they move to the next step.

2. A customer can type their basic info name, birthdate and an email address OR phone number. With this information the app will first verify their age in accordance with the template age requirements, and attempt to locate their existing customer record. If found, the customer will be sent a text message or email containing a one time use code for them to enter. All of their data is pre-filled and they can make any corrections necessary.

3. If offline (not yet fully supported) or there is some other error preventing the barcode or lookup you can skip this screen and go directly to the customer profile page.

After determining if this is a new or existing customer they are prompted to scan the image of their government issued identification. The image is automatically cropped and straightened.

Finally, on the profile page they will fill out all necessary and optional information.

### Guardian

If the customer is under the required age but above the minimum age as defined in the [template settings](./templates.md), a guardian is required. The guardian must fill out their name and phone number, as well as scan their government issued identification.

### Contacts

Controlled by the [template settings](./templates.md), customers can be prompted for Emergency and Physician Contact information. Even if prompted as instructed by the template, they are skippable.

### Medical

Customers are prompted to fill out their medical profile with any allergies, diseases or medical conditions they may be afflicted with. This list is configured in [Medical Conditions](../settings/medical-conditions.md).

If the customer is returning, these are automatically filled out with past answers _except_ medical conditions that are flagged as Required. These must be explicitly set each session.

### Disclaimers (Template Sections/Blocks)

The customer is next presented with disclaimers, which are the sections and blocks as configured by the template. See [Templates](./templates.md) for more information.

> Sections which are set as Parent/Signature Sections are skipped if a guardian is not required.

### Source

A customer will be prompted to answer where they heard about your studio. This is configured from the [Sources](../settings/sources.md) list.

### Signatures

The customer is prompted to sign the form. Depending on various scenarios this may show 1, 2 or 3 signature boxes.

|Signature|Displayed if...|
|-|-|
|**Customer Signature**|Customer age is greater than or equal to the ```Required Age``` **OR** a guardian was required and the ```Require Minor Signature``` setting is set in the template. If you do not require minors to sign, turn this setting off. i.e. customer is legal age, or they are a minor and you require minor signatures.|
|**Guardian Signature**|The customer is less than the ```Required Age```. (i.e. a guardian is required.)|
|**User (Provider) Signature**|The ```Require User Signature``` setting is set in the template.|

### Picture

Say "cheese!" A customer is then prompted to _optionally_ add a picture of their smiling face to their profile. This helps build a relationship with your customers by remembering them when the come in for repeat visits.

!!! note "Minor Pictures"

    Customers under the age of eighteen (18) are not prompted for this step. Additionally, you cannot set a profile picture for a customer under this age from the customer profile. This is by design for safety and privacy reasons.

### Finish

Once complete, the ```Finish Message``` of the template is displayed (if set). After a short period of time Kiosk restarts and is ready for the next customer.

<a href="#guided-access-ipad"></a>

## Guided Access (iPad)

Guided Access is a feature of iPadOS to lock a user into a specific app, disabling the home button or other features of the device. This is particularly useful if you intend to leave one or more iPads unattended for customers to use for filling out their forms.

### Setup Guided Access

1. Go to iPad Settings
2. Tap Accessibility
3. Tap Guided Access
4. Tap the toggle to turn Guided Access on.
5. Set a Passcode or use Touch/Face ID
6. Set the Display Auto-Lock (for unattended iPads, this should probably be `Never`).

### Enter Guided Access

1. Open the REV23 app.
2. Depending on your iPad, you will enter Guided Access by
    - Triple-clicking the Top Button (on iPads without a Home button)
    - Triple-clicking the Home Button
3. Enter Kiosk mode from the main menu.

### Exiting Guided Access

Depending on your iPad, you will exit Guided Access by:

- Double-clicking the Top Button (on iPads without a Home button)
- Double-clicking the Home Button

You will then either enter your Guided Access Passcode (not Kiosk passcode) or Touch/Face ID to exit the session.
