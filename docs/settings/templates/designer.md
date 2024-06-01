# Template Designer

The Template Designer, currently available on web only, is how you design the flow of your template/form.

Templates consist of settings, **sections**, and **blocks**.

A **block** is text you want your customer to read, a statement you want them to agree to, or a question for them to answer.

A **section** is simply a group of blocks.

Depending on your needs your template may have just one section and one paragraph block, or it may be broken down into multiple sections with a full length questionnaire. This is entirely up to you!


The outline of a template design looks like this

```
- Start Message (optional)

Sections
└─ Section 1 (At least one section is required per template)
    └─ Block 1 (At least one block is required per section)
    └─ Block 2
    └─ Block 3
└─ Section 2
    └─ Block 1
    └─ Block 2
   
- Finish Message (optional)
```

Let's look at a practical example

```
- Start Message
    "Welcome to <studio name>!"

Sections
└─ Disclaimers
    └─ Paragraph: "By filling out this form you are agreeing to the following..."
    └─ Yes/No: Are you pregnant or breast-feeding?
    └─ Yes/No: Are you allergic to latex?
    └─ Time: When did you last eat?
└─ Additional Release
    └─ Initials: Photo consent
    └─ Initials" Verified spelling of tattoo if applicable
└─ Parent/Guardian Section
    └─ Document: Scan a copy of the birth certificate
   
- Finish Message
    "Thank you! Please hand the device back to studio staff and we will begin your service shortly!"
```

As you can see a template can be very flexible and powerful.


## Template Options

### Common Options

- **Version Name**: The name of the template version (multiple version support coming soon). This allows you to have multiple versions of a template for historical reasons, setting only one to be the active one. You can use version numbers like 1.0, 2.0, or dates such as 2024-Jan-1. Whatever makes this most sense to you.

- **Title**: The title of the template which will be printed on the top of the generated document.

- **Paper Kind**: The size of paper you wish to generate the document with for printing purposes.
    - Letter
    - Legal
    - A4

- **Show Logo**: If checked, your studio logo (if available) will be printed on the generated document.

### Release Form Options

> Currently, Templates are limited to release forms. Soon you will use templates for Deposits and other scenarios.


Release Form templates have additional settings.

- **Required Age/Minimum Age**: See [age requirements](#age-requirements).

- **Prompt Emergency Contact**: If checked, the form will prompt the customer for an optional emergency contact.

- **Prompt Physician Contact**: If checked, the form will prompt the customer for an optional physician contact.

- **Require Provider Signature**: If checked, the form will require a signature from the provider/artist.

- **Require Minor Signature**: If checked, the form will require a signature from the minor, in addition to the parent/guardian signature.

- **Show Medical Conditions**: If checked, the medical conditions table will be shown on the generated document. This does not control whether they are display to the customer in Kiosk.

<a name="age-requirements"></a>
#### Age Requirements
You can specify the customer age rules for filling out a form within the template. There are two settings to control the behavior of the form.

1. **Required Age**: This is the required age in order to fill out this form without a parent or guardian. In most cases, this is 18.

2. **Minimum Age**: This is the minimum age required to fill out this form _with_ a parent or guardian.
    - **If blank**, this means that even if a parent/guardian is present, you do not offer this service. For example, if you do not tattoo minors, period, leave this blank.
    - **If set**, this is the minimum age that is able to fill out this form. For example, if you pierce minors, but require they be at least 8 years old, set this to 8. If you have no minimum, set this to 0.


## Start/Finish Messages
Each template has two designated sections on the top (start message) and bottom (finish message). These allow you to provide instructions for filling out the form, as well as instructions for after the form has been completed. These do not show up on your release form and are cues to customer via the user interface only.


## Sections

A section is a logical group of blocks. Each section can have its own specific options to control the layout and flow of the release form, both when filled out by your customer, and how it is rendered on the final PDF.

- **Title**: The title of the section. This shows in Kiosk, as well as a title on the generated document.
- **Break Page**: If checked, this section will begin a new page on the generated document.
- **Parent/Guardian Section**: If checked, this section will only appear in instances where a guardian is required. It will not be shown in Kiosk or on the generated document if the customer meets the [age requirements](#age-requirements).

## Blocks

Blocks represent the actual content on a form. A block can be a paragraph of text, or a question you want the customer to answer. Blocks allow for an extremely customizable and flexible form.

Below we will discuss each block type and their behavior.

| Block Type | Purpose |
| - | - |
| **Paragraph** | A block of text to read. This can be a single line, or multiple lines and paragraphs. |
| [**Initials Entry**](#initials-entry) | The typed initials of the customer. |
| **Text Entry** | A typed text response from the customer. Best for short, single line answers. |
| **Multi-Line Entry** | A typed text response where you anticipate the answer may be a bit longer than a single line. |
| [**Select Entry**](#select-entry) | A drop down/popup that allows the customer to select from a list of predefined values. |
| [**Yes/No Entry**](#yesno-entry) | A yes or no question. |
| **Yes/No & Text Entry** | A yes or no question with an optional text field for the customer to type in additional detail. |
| **Date/Time Entry** | A date & time value i.e. Oct 31, 2024 at 10:00 AM. |
| **Date Entry** | A date value. i.e. Oct 31, 2024. |
| **Time Entry** | A time value. i.e. 10:00 AM. |
| [**Photo Upload**](#photo-upload) | Upload a picture or photo. |
| [**Document Upload**](#document-upload) | Upload or scan a document. |

All blocks (except **Paragraph**) have additional common options. Common options include

- **Required**: If checked, a value _must_ be provided.
- **Review**: If checked, this block and its response will be highlighted to the user in the Service Session. These are important questions you want to ensure the provider sees an answer to.

## Block Behaviors

Some blocks are obvious to how they will behave. Others have special behaviors or options that are important to know.

<a href="#initials-entry"></a>
### Initials Entry
A block that requests the initials of the customer be typed in. For example customer 'John Doe' will required initials `JD` to be entered.

If this block is placed in a section designated as a Parent/Guardian section, this will require the Guardian's initials instead of the customer.

<a href="#select-entry"></a>
### Select Entry
A block that allows the customer to select from a list of predefined values. To use this block you must add items to the the list. This will appear as a dropdown box or popup depending on the platform.

<a href="#yesno-entry"></a>
### Yes/No Entry
A block that allows the customer to answer a yes or no question.

This block type has an additional setting of **Required Value** which enforces the customer select a particular value. If a value other than the required value is chosen, they are not allowed to proceed with filling out the form.

A required value allows for _Must answer Yes_, _Must answer No_, or _Accept Any_, which means either value is acceptable. A common example of this type of entry is:

```
Text: Are you currently pregnant or breast-feeding?
Required Value: Must answer no
```

If the customer answers _Yes_ to this question, the form cannot proceed.

> The rendered input of this block changes depending on the **Required** setting. If Required, individual Yes & No buttons are displayed, no default is selected and the customer must choose one of them. If this block is not required, an on/off switch is displayed, where the default value is no (off).

<a href="photo-upload"></a>
### Photo Upload
A block that allows the upload of a photo. On web this block shows an upload box allowing the customer to select a file from their computer. On iPad this block shows the camera.

This photo is included on the generated document.

<a href="document-upload"></a>
### Document Upload
A block that allows the upload of a document. On web this block shows an upload box allowing the customer to select a file from their computer. On iPad this block shows a document scanner which automatically crops, straightens and converts the image to black & white and stores it as a PDF. 

The document is included as a link only in the generated document.

<a href="#template-mappings"></a>
## Template Mappings

After you've created your template you must map it to a Service Category Type. Go to Settings > Templates > Mappings and remove any existing mapping from the desired category and add your new template.

> Future versions will allow multiple templates per service type.


## Markdown

While not required, REV23 allows you to format your templates with Markdown to add **bold** and *emphasized* text, formatted lists, and more. **You can learn how to use Markdown in just a couple of minutes** to add additional structure and clarity to your templates. Markdown is used across many popular websites including Reddit, and even this very user guide, so you can take this knowledge with you to other corners of the web.

Examples of Markdown:

|Type|Or|... To Get| 
| - | - | - |
| `*Italic*` | `_Italic_` | *Italic* |
| `*Bold*` | `__Bold__` | **Bold** |

REV23 supports basic Markdown only. For security, formatting and/or usability reasons, some features such as using raw HTML are disabled.

[Learn Markdown](https://commonmark.org/help/)