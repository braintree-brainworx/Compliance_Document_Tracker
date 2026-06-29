---
layout: NewLayout
title: Welcome to Braintree Support
description: Support and documentation for Braintree's Compliance Document extension to Microsoft Dynamics 365 Business Central
---

# Compliance Document Tracker

  - [Configuration and Setup](#configuration-and-setup)
    - [Set up new Number Series](#set-up-new-number-series)
    - [Capture Setup fields](#capture-setup-fields)
    - [Issuing Authorities](#issuing-authorities)
    - [Document Types](#document-types)
    - [Entity Defaults](#entity-defaults)
    - [Link Skills to Certifications](#link-skills-to-certifications)
  - [Managing Documents for Entities](#managing-documents-for-entities)
    - [Create a new document](#create-a-new-document)
    - [Approve the document](#approve-the-document)
    - [Managing documents from the entity - Example : Customer](#managing-documents-from-the-entity---example--customer)

## Configuration and Setup

### Set up new Number Series
1. Search for No. Series
2. Create new number series for:
   1. Statutory documents
   2. Course Numbers
   3. Training Tasks
   4. Training Classes
   5. Training document numbers (certificates)

### Capture Setup fields
Search for Statutory Documents Setup.

![alt text](docs/images/image-4.png)

Capture fields for document management
* Statutory Documents number series - used to number entries in the statutory documents table
* Expiry warning period - a date formula which indicates how long before expiry you would like the system to warn you.

Capture fields for training administration
* Course number series
* Training document number series
* Class number series
* Training job number (if integrating to Projects module)
* Class No. Series - for identifying classes

### Issuing Authorities
The organisations (including your own) that are responsible for issuing or certifying the documents you need to maintain are defined here.

From the Statutory Documents Setup page, click on Issuing Authorities. 

![alt text](docs/images/image-5.png)

Capture the data as follows:

![alt text](docs/images/image-6.png)

*   Code : unique code to identify the organisation
*   Name - full name of the organisation
*   Membership number - if you have a registration number with the external organisation, enter it here
*   Vendor number - link to a vendor to facilitate payment of membership fees.

### Document Types
The types of document which your organisation needs to store, and the rules of how to manage them, are entered here.  From the Statutory Documents Setup, select 'Document Types':

![alt text](docs/images/image-7.png)

Capture the information as follows:

| Field Name    | Details                                                   |
| ---           |---                                                        |
|Statutory Documents Code | A unique code to identify the type of document  |
|Issuing authority | Select the Issuing authority responsible for this document type|
|Validity          | If the document has a limited validity, enter a date formula to calculate the expiry date from date of issue|
|Area of jurisdiction|Free text, indicating where the document is valid eg Global, National, Site|
|Document importance| Optional / Recommended / Mandatory|
|Duplicates allowed| If multiple editions of the same document type can be issued to a particular entity, tick on. If ticked off, the system will prevent you from capturing more than one edition of a document.|
|Extension Period   |                                                      |
|Maximum Extensions allowed |   |
|Associated Entities:|Select the entities to which the document type can be attached: Customer / Vendor / Fixed Asset / Item / Resource / Service Item / Employee |    |


### Entity Defaults
This function allows you to define the suggested list of documents that need to be collected for a particular entity. For example, for a new customer, you may want to collect their company registration, VAT registration, BBBEE certificate.

From the Statutory Documents Setup, select 'Entity Defaults'.

Enter fields as follows:

| Field Name                | Statutory Document Type                       | 
| --                        |--                                             |
|Entity Type                | Select from the available entities            |  
|Statutory Document Types   | Select the document type from the list        |
|Document Importance        |                                               |

Repeat for each document required for the entity type. Example:

![alt text](docs/images/image-8.png)

## Managing Documents for Entities
An entity is a master record against which you wish to store and manage documents. This could be a supplier, customer, inventory item, fixed asset, resource or employee.

You can manage the documents via an administration role centre, and you can also view and manage the documents for a particular entity from the relevant master maintenance record.

Make sure that your profile is set to 'Document Manager'. The role centre should look something like this:

![alt text](docs/images/image-19.png)

### Create a new document
1. Click on '+ Statutory Document' OR open one of the cues, and click New.
   
   ![alt text](docs/images/image-14.png)

2. The Document No. will be allocated automatically from the number series defined during Setup.
3. Enter the Document Association (Vendor / Customer / Item / Asset / Resource / Employee), and select an entity to which the document should be attached. 
4. Select the document type. The system will automatically populate the validity and issuing authority.
   
   ![alt text](docs/images/image-15.png)

5. Enter the date of issue.
6. Enter the number of the document.
8. If the documents have been received, attach them to the entry, and update the status to 'Received'.

### Approve the document
If you have the appropriate authority, you can update the status of the entry to 'Approved'.

## Managing documents from the entity - Example : Customer
1.  Select Customers.
2.  Open the card for a customer.
3.  To load the default document types, click on Customer -> Statutory Documents -> Create Default Statutory Documents.
   
![alt text](docs/images/image-16.png)

4.  The Statutory Documents fact box will display a list of the documents required.

![alt text](docs/images/image-17.png)

5.  Click on Customer -> Statutory Documents -> Statutory Documents. This will open the list of documents linked to the customer. You can now capture the remaining information such as the date of issue.

The above process applies to all entities.