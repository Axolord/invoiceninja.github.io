---
extends: _layouts.user_guide 
section: content
locale: en
---

# Clients

<video width="100%" controls>
  <source src="/assets/videos/clients/create_client.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

## Creating Clients

There several ways for a client to be created, including:

* Clients > + Client
* Settings > Import | Export > Client CSV Import
* Client Portal (if client registration is enabled on Settings > Client Portal)
* API Integrator: Zapier, Integromat, APISync, or manual API calls developed using the [API Documentation](https://api-docs.invoicing.co/).

A "Client" can either represent a person or a company. If only the contact information is set the contact name will be used as the client's display name. If the client's name is set then it will be used instead.

There are three different client id fields:

* **$client.id** : Autogenerated and used by the API (ie, 7WR07SC)
* **$client.number**: Autogenerated and can be configured on Settings > Generated -Numbers (ie, 0001)
* **$client.id_number**: Standard field which can be used to store the client’s number from a different system

## Viewing Clients

To view a client, select one from the list of clients on the client panel, or by linking to it from a related invoice, project, task or transaction.  

### Overview

The overview panel presents a quick look at the paid to date, the outstanding balance of a client, public and private notes about the client, followed by a list of interactive buttons to see a client-filtered list of any category.  

You can select from **Groups, Invoices, Payments, Recurring Invoices, Quotes, Credits, Projects, Tasks, or Expenses**.  Hover your mouse over one of these categories, and the icon will turn into a "plus" symbol; it is a clickable button to create a new invoice, quote, payment, etc.  On mobile devices, you can touch and hold anywhere on the button to create new, instead of viewing a client-filtered list.

The **Client Portal** link at the bottom will take you into a new web browser tab or window, to view the client portal directly.

The "Settings" button at the bottom will take you to **Client Settings** where you can edit and configure client-specific rules, templates, behavior, etc.

The kebab menu button in the top right of this panel also has many of these functions, and is available on every tab.

### Details

This panel presents a view of the contacts listed in a client entry, and includes links directly into the client portal page as those contacts.

### Documents

The *Documents* panel provides the ability to upload documents and view documents you have linked to the client.  These uploaded files are accessible through the admin portal, or through the client portal for your clients to view themselves.  A useful way to employ the document uploads feature, is by uploading terms of service documents, contracts, or other files you would like to share with the client for any other reason.  

**Note** that uploaded documents are saved in the "public/storage" directory in a folder structure using hashed folder names to match the product entry, so backup this directory along with your database to preserve your attached documents.

### Ledger

The *Ledger* panel provides a chronological overview of transactional activities related to the client, to track cashflow in and out related to the client.  The *Ledger* highlights debits and credits on the client's account.  Objects in the *Ledger* are shortcut links, and clicking on them will bring you to the record or transaction that they describe.

### Activity

The *Activity* panel provides a chronological overview of non-transactional activities related to the client.  While the *Ledger* panel tracks credits and debits to the client's account, the *Activity* panel tracks history of new records or record modifications to the client record, or invoices, quotes, etc that are connected to the client, and which admin portal users performed those actions.  The *Activity* panel is useful for accountability within your business, and monitoring who did what, and when.

### System Logs

The *System Logs* panel provides a chronological overview of backend server activity related to your client, such as when PDFs are generated for the client, and the success or failure results of those requests.

## Editing Clients

You can edit your clients by double-tapping a client in the *Client* module list, or viewing a client and using the *Edit* button in the top right corner of the panel.  On mobile you will see a list of tabs at the top menu, for different sections to edit client data.  On a desktop you might not need to navigate tabs, because the default view is to see all the fields on one panel.  

Most of the information in a client entry or edit form is entirely optional, and some is automatically generated.  Your own business practices should dictate what sort of data you gather from your clients.

### Details

* **Name** - Client name, can be the name of an individual, group, organization, or business.  If a name is not chosen, but a contact entry with first/last name is provided, the first contact's name will be used as the client name.
* **Number** - This number is automatically generated by Invoice Ninja, for tracking purposes.  Rather than editing the numbers manually, we would suggest to edit the behavior of generated numbers under *Settings* > *Generated Numbers* > *Clients*.
* **ID Number** - The ID number field is optional.  You can use this to reference a client's ID number as it pertains to your business, such as a membership ID number.
* **VAT Number** - The VAT number field is a Value Added Tax ID number which applies mostly to countries from the European Union who need to track this sometimes for tax purposes.
* **Website** - Your client's website, optional, and for reference.
* **Phone** - Primary phone contact number for the client, organization, or business, separate from any individual contact's phone number within the client entry.

### Contacts

Every *client* has a *contacts* list, allowing you to add as many *contacts* as you like to represent any given *client*.  When viewing a client, you can see existing contacts under "Details" panel.  When editing a contact they will be listed under the *Contacts* panel.

From the admin portal, you will see the button *Add Second Contact* to expand the contact list with a new contact entry. You can only add new *contacts* to a *client* from the admin portal.  Customers cannot add more *contacts* to their *client* entry from the client portal themselves.

* **First and Last Name** - Name details for the individual contact.  Invoice Ninja automatically uses the first contact's name information to populate the client name if one is not provided.
* **Email** - Email address associated with the client, and used as their log in credential for the client portal.
* **Phone** - For reference, phone number contact information for the individual contact.

### Notes

* **Public Notes** - Any public notes about the client, public notes are typically included on any future invoices, quotes, or other documents generated for the client.
* **Private Notes** - Private notes are any comments about the client that will only ever be viewable by users on the admin portal.
* **Size** - Used to describe the size of a client that represents an organization, school, or business.
* **Industry** - Add further description to your clients to describe the type of industry they are involved in.

### Settings

* **Currency** - Default currency to apply to invoices and payments for this client.
* **Language** - The preferred language of your client.  Invoices and other documents will be generated in the client's preferred language.
* **Invoice Payment Terms** - Set a default invoice payment term length, if you have agreed on payment arrangements with your client on a regular basis.
* **Quote Valid Until** - Set a default term length for quotes given to your customer that you will honor the price in your quotes for.
* **Task Rate** - Set a default hourly rate for *Tasks* that are performed for the client.
* **Send Reminders** - Enable or disable email reminders to the client for things such as unpaid invoices.  Set fine tuned rules for the behavior of email reminders under *Settings* > *Templates & Reminders*.

### Billing Address

Standard address information fields are available here to enter a billing address for your clients with.  This information is usually also included on any invoices and other documents for the client.

### Shipping Address

Just like the billing address, standard address information fields are available here to enter a shipping address for your clients with.  Additionally, you can use the *Copy Billing* button below these fields, to simply copy the billing address information into the shipping address fields as well.

## Contacts and the Client Portal

*Contacts* are each given their own profiles in the client portal, logging in with the emails you assign them, allowing each contact to set their own password and personal settings or details on the client portal, regardless of which *client* they represent. 

When an individual self-registers on the client portal, their name and email will be added as *contact* data under a new *client*.  After signing in, they will have the opportunity to edit their *client* details in the "Profile" menu, such as company name and contact information. 

Email addresses for *contacts* are considered authentic.  For example, if an individual attempts to self-register while already being included as a *contact* for another *client* entry, the self-registration portal will force them to resubmit their personal information using a new email address, or have their email address removed from the other *client* listing. 

## Group Settings for Client Management

If many clients share the same settings, for example, the same currency or email reminder settings, you can create a group on *Settings* > *Groups* to, apply a standard set of settings to a large group of clients.

For most settings, the app will first check if the client has a value in place, if not it will check if the client belongs to a group and if that group defines a value. Finally, it will use the default value set at the company level.

The benefit of using groups is that if in the future you need to change the setting you can change it one place rather than having to update multiple clients individually. Without groups, bulk updating client settings would require using the API or an integrator.

## Custom Fields

Sometimes you need extra fields to populate additional information for your clients. With Invoice Ninja you can add up to 4 custom fields for both the client and also each contact of the client.

To create a custom field navigate to Settings > Custom fields. Advanced features including being able to include these custom fields on the invoice PDF by using the placeholders:

### Client placeholders

```
$client.custom1
$client.custom2
$client.custom3
$client.custom4
```

### Contact placeholders

```
$contact.custom1
$contact.custom2
$contact.custom3
$contact.custom4
```

<x-next url=/en/credits>Credits</x-next>