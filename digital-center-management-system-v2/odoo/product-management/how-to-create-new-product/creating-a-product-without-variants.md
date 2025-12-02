# Creating a product without variants

Simple product is created without variants. In that case one Product (product.template) corresponds to one Variant ( product.product)\
Example of such products are : Lady stockings, Plaster of paris - powder, etc...\
For such products, we need to define only a few things:<br>

<figure><img src="../../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

1. Selecting checkboxes to buy or sell will impact this product's visibility across various sections of the Odoo system.
2. Product Type: This categorization helps in understanding how a product is used or consumed:

* **Service**: An intangible product that involves performing tasks or activities for a customer.
* **Consumable**: A product that is intended to be used up or exhausted quickly during use.
* **Storable**: A product that can be stored and used over a long period without immediate consumption.



3\. - Product category - required, allows the product to be more configured and grouped

4\. - Internal reference - or code, used for faster finding the product

5\. - sales price - is basic price that will be displayed when selling or expensing this item

6\. - customer taxes - when selling the product this tax will be applied by default (can be modified by fiscal position rles)

7\. - Units of measure, Purchase unit of measure - unit of measure is used for this product internaly, while purchase unit of measure is/can be used while purchasing product.\
for example, for Plaster of paris unit of measure is Kilogram, but it can be purchased as Bag of 50 kg –
