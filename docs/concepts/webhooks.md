# Webhooks

Webhooks allow you to integrate REV23 with other software and services. You can subscribe to specific events in the REV23, such as when a customer is created or a release form is generated, and take that data and put it into another system.

Examples of things you can do with webhooks include:

- Storing a copy of the signed release form PDF in your preferred cloud storage such as OneDrive, Google Drive, Dropbox, etc... as a backup.
- Send a customer a welcome text message with Twilio when they are created.
- Adding a service to QuickBooks or Square to take a payment.
- Adding a customer email to MailChimp or Constant Contact to automate birthday emails.

Webhooks also allow you to supplement features that aren't implemented yet, such as emailing aftercare instructions to a customer.

In addition to notifying other services about events in REV23, you can also respond to events from other systems. Such as:

- Create a customer when a Google Form is filled out
- Create a customer record when a client books an appointment in a separate online booking app and send them a text message to fill out the online release form.

The possibilities of webhooks are limitless! Want to start a robot mop to clean your station when a session ends? YES! Webhooks can do that!

> Webhooks are a slightly more advanced feature. There may be an additional fee to use this feature of the app in future versions. While we support webhooks, our support team cannot help you design or troubleshoot these in other services.


## Security Considerations
To use webhooks users required the `subscribe:webhook` permission (located in [users](./users.md)). You must evaluate if a user truly should have this permission, because in some cases it ignores other permissions.

Because webhooks are just events that are triggered blindly when something happens in REV23, this gives users the potential to 'siphon' data. For example, a user could create a webhook to copy customer data when new customers are created to another app of their choosing... a Google Sheets spreadsheet, or even to another REV23 subscription. If you do not want your users to be able to have this level of access to your data you should not permit their use of webhooks.

## Two-way Synchronization Warning
While technically possible, these services are not intended for keeping two systems completely in sync and you can encounter endless loops. If such loops are detected your account on either side of the integration may be disabled or blocked.

Consider the following scenario of two webhooks:

- **Webhook A**: When a customer is created in REV23, create a customer record in QuickBooks.
- **Webhook B**: When a customer is created in QuickBooks, create a customer record in REV23.

Do you see the problem? If you create a customer in REV23, webhook A runs to create the customer in QuickBooks... then webhook B runs to create the customer in REV23... then webhook A runs... and so on, and so on. You're now stuck in an endless loop potentially creating thousands of duplicate records and/or having your accounts deactivated or suspended.

While you could design your webhooks to attempt to handle such things, by locating a record based on an ID and skipping if found, it becomes much more complex.

Because of this, we **strongly discourage** you from attempting scenarios that could result in endless loops. Your integrations should be one way only.

## Zapier
For our launch version, we only support Webhooks via Zapier. An online automation tool that connects two or more apps/services. You can Zapier makes it easy to design your workflows (Zaps) and automate many tasks! Find the REV23 app when designing your Zap to get started!

[Check out Zapier](https://zapier.com)


## Other and custom webhooks
We will be adding support for IFTTT shortly. Additionally, we are considering allowing custom webhook subscriptions for more advanced users to integrate into their own websites or services.

