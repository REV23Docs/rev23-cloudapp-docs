# iOS Version History

## 1.3.6 (2025 Sept 8)

- Fixed a bug that prevented login on iOS 26 (beta)
- Introduced a (proposed) fix for a bug that would sometimes result in a 404 error when editing a session's details such as price or placement. Since we've never been able to reproduce this one is a stab in the dark.

## 1.3.5 (2025 Jul 31)

### Find Duplicate Customers

In the ... menu in the Customer list, you will now find a new Find Duplicates option. This will show you customers that have potential duplicates based on their last name and birthdate. Tap one to see the duplicates and decide which you want to merge.

See [Merging Duplicate Customers](../concepts/customers.md#merging-duplicate-customers) for more information.

### Kiosk Exit Change

The four corner tap sequence to exit Kiosk has been removed and replaced with an Exit button in the top right corner. This was based on user feedback that the tap sequence was unnecessary and tedious, potenitally slowing users down if they only have one device.

### Kiosk Polish

Kiosk has received some visual polish making required fields easier to identify, as well as new ways to exit and start over.

- The start over button, previously found as a large circular button in the bottom right has been moved to the top left with a clear label as to the intent and match the new Exit button.
- Required fields are now easier to identify by making them bold and blue with stylized lables.
- Markdown support has been enhanced in Templates by stylizing your headers, bullet points and more.

#### Additional Changes

- The ability to select and copy/paste, auto-fill text in the main app has been restored. This functionality remains disabled in Kiosk for securit and privacy reasons.
- Fixed a bug that could cause a crash when opening a user from Security > Users.
- Signing out of REV23 ID will no longer clear your Portfolio options.
- You can now create a user without specifying an email address, though this user will not be able to reset a forgotten password.
- Fixed a bug with some drivers license barcodes that would not read if the data contained 'garbage' on the end of the data.
- Signature is now cropped horizontally if the signature does not take the entire width of the canvas (matching the web UI behavior).
- Fixed a bug that prevented onboarding new tenants in the initial studio setup screen.
- Various improvements and bug fixes.

## 1.3.4 (2025 Jul 11)

### Portfolio Slide Show

Go to **Settings > Portfolio** to add photos or albums from your Photos app (albums are the preferred method so you can more easily manage them and share them across devices). The images will cycle when Kiosk is idle on the Welcome screen.

See [Portfolio](../ipad/portfolio.md) for more information.

#### Additional Changes

- Navigation Bar is now always visible when scrolling. Previously in screens like Customer or Service detail if you scrolled to the bottom you would need to scroll to the top to see the < Back button again. This is now always visible.
- Added filter to user list
- Screen mirroring the app to another display caused issues. The app needs to be restarted after starting a screen mirroring session now.
- Service filter settings are now saved per user.
- The clear signature button on Kiosk has been made larger and more clear with a new eraser icon.
- Added a clear button to the color pickers
- Removed restrictions on deleting completed services and now let force delete take this over
- Deleting a session could cause a 404 error when trying to reload the view
- Various UI touch-up updates.

## 1.3.3 (2025 Jun 1)

### Color Customization

Added color customization to users, studio, service categories and service types. Service colors are currently the most noticable, the other settings will be more subtle, but used in future updates.

- Users: Overrides the system defined color for user initial colors. If not set will use the system generated color.
- Studio: Overrides the system defined color for the studio initials. If not set will use the system generated color.
- Service Categories: Displays an indicator on lists of services with types of that category. If not set no indicator will be visible unless specifically set on the service type level.
- Service Types: Displays an indicator on lists of services of that type. If not set, it will use the color set on the category level.

#### Additional Changes

- Added short name to Studio. Reserved for future use.
- Fixed a crash that could happen during maintenance alerts if the scheduled time was formatted a certain way.
- Forced upgrade alerts that direct you to app store when we specify a minimum version. Too many people staying on older versions that prevented maintenance work.
- Various improvements and bug fixes.

## 1.3.2 (2025 May 15)

- Some Drivers licenses contained QR codes which were being being scanned incorrectly. This has been disabled and only the PDF417 barcode is recognized by the camera.
- Notes has a new chat like appearance.
- Fixed a bug that caused service type selection in Kiosk to be skipped if there were two service categories that both only had one service type, i.e. Tattoo and Microblading categories, with a single Tattoo and Microblading service type
- User interface polish.
- Maintenance and update banners.
- Various improvements and bug fixes.

## 1.3.1 (2025 Apr 15)

- User interface improvements
- Service filter user selection is now hidden if current user does not have permission service:read.all permission.
- When adding supplies to a session there is now better guidance when the lists are empty instead of just an empty list with an add button.
- Some areas used an incorrect user avatar color.
- User detail was not showing preset signatre.
- When creating a new service type the category is now set to the selected category if available.
- Various improvements and bug fixes.

## 1.3 (2025 Mar 29)

### Service Filter

You can now filter services in the service list by status, provider, type, category, etc...

### Force Delete

Added the ability to force delete to certain objects when initial deletion fails due to business rules. For example, if you attempt to delete a service/session with signed forms you would encounter an error and have to delete the forms first. Now, if a user has a permission that would enable them to delete the object(s) preventing an object deletion (in this case `form:delete`) the first delete attempt will still fail, and prompt if you'd like to delete the related objects.

#### Additional Changes

- Fixed a crash that could happen when taking a picture of customer ID image.
- Reduced the amount of time popup alerts are visible
- Enhanced chat to auto-fill some details from the user.
- Various improvements and bug fixes.

## 1.2.2 (2025 Feb 28)

- A pencil icon now shows in the customer medical conditions when a write-in value was provided.
- Various improvements and bug fixes.

## 1.2.1 (2025 Feb 26)

- Fixed a crash caused by template select blocks with no items.
- Using any email action now uses the default Mail app set in iOS settings.

- Various improvements and bug fixes.

## 1.2 (2025 Feb 19)

- Improved the consistency of nav bar headers.
- Polished many user interface areas to increase consistency across app.
- Various improvements and bug fixes.

## 1.1 (2025 Jan 24)

### Flags

Added [Flags](../settings/flags.md) to customers to allow you to easily flag customers to be alerted to future problematic encouters.

#### Additional Changes

- Replaced REV23 logo with app icon when starting Kiosk.
- Various improvements and bug fixes.

## Older Versions

> There isn't much sense in documenting changes in these versions. It was a mad rush to fix and polish as much as possible after the initial release and are listed here for historical data tracking only.

- 1.0.5 (2025 Jan 6)
- 1.0.4 (2024 Dec 23)
- 1.0.3 (2024 Dec 2)
- 1.0.2 (2024 Nov 12)
- 1.0.1 (2024 Oct 23)
- 1.0 (2024 Oct 18)
