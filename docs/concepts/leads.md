# Leads

!!! abstract "Preview Feature"

    Leads are currently supported on web only. This feature is experimental and due to change based on feedback.

## What the !@#$ is a lead?

Leads are a fancy corporate word for people who may turn into a client. In REV23 they are more or less people on your cancellation/interest list. Sure, we could have picked another word, but 'Lead' is a lot shorter than 'Person on your interest or cancellation list', and kind of a universally accepted term for someone that can turn into money. So let's go!

## Using Leads

When you have someone that is interested in getting tattooed by you at a later date due to your books being closed, they want on your cancellation list, or you just aren't sure you want to take the project yet, you can add them to the list... well, they can add themselves.

Direct them to the /list page of your REV23 site (i.e. https://`yourdomain`.rev23.com/list). They can fill out key details such as creating their customer profile as well as what they want, their availability and budget.

## Searching Leads

When you have a no show or cancellation and want to fill it quick, check your leads! You can go to the Leads list in the app. Using filters you can quickly narrow down to who you want to call to bring in.

For example, "Available now" will look at customer who have availability during that day of week and time of day.

## Webhooks

Leads support the following [webhook](./webhooks.md) events:

|Event|Permission|Description|
|-|-|-|
|**lead.created**|read:lead| A lead object was created. |
