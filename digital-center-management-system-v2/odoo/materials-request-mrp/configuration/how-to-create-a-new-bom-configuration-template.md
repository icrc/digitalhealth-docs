---
description: 'Recommended role : P&O and DCMS Admin'
---

# How to create a new BoM Configuration Template

To configure a Bill of Materials (BoM) in the Odoo Manufacturing module, start by navigating to "Settings" > "BoM Config Template". Click on "Create" to begin the process.

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Select the product that will be manufactured or create a new product if necessary. Ensure that the product has the "Manufactured" checkbox selected to make it available for selection here. If you need guidance on configuring a new product, you can find instructions \[here].

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

When you select a product, the Reference and Name fields will automatically update based on the selected product. However, you can still modify the name and reference if needed.

Notes : If your Odoo instance supports multiple languages, you can update the translation for the product in any other installed languages.

Next, click on "Configure Attributes" . Select the attributes you want for your product. By default, the attributes will match those of the product, but you can select different attributes if needed.

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

These will be displayed with the "main product" column unchecked. You can use the three-dot menu to show more columns, such as "Allowed Value".

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Here, you can add or remove values as required.

&#x20;(Only if you are on edit mode)

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

Finally, click on "Start BoM Configuration". Two tabs will appear: "Components" and "Operations". These tabs allow you to define the components and operations necessary for manufacturing the product.

<figure><img src="../../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>

Let’s first begin by creating a new work order line in the Operations tab, When selecting the operation, if you want to create a new one, you can write the name of the new operation and click on "Create and Edit". This will open the form for further details.

Here is an explanation of the fields and options available:

<figure><img src="../../../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

1\.     Name:  This is the name of the operation that will be displayed.

2\.     Work Center: Select the work center where this operation will take place. The work center refers to a specific location or set of equipment where manufacturing activities are performed.

3\.     SU Needed: Indicate if the service user presence is required for this operation.

4\.     Green Light: Check this box if the operation requires approval before proceeding.

5\.     Default Duration: Set the default duration for this step, indicating how long the operation is expected to take.

6\.     Description: Provide a detailed description to guide users on what needs to be done during this operation.

Next, navigate to the Components tab. When adding a line, you must first select the product category. This selection will filter the available products, showing only those associated with the chosen category.

Once you are satisfied with the configuration template, click on “Approve”.

<figure><img src="../../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

The BoM Template will now appear under the BoM section, ready for use in the manufacturing process.

