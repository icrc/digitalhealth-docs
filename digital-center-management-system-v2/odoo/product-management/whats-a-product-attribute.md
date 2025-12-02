# What's a product attribute

Product attribute help us to define multiple product variants with product codes generated according to specified rule, and manage it from one product (template).\
Product can be configured by using multiple attributes, and allowing specified attributes values for that product.

To access the list of available product attributes, (stock manager) go to :\
**Inventory -> Configuration -> Products -> Attributes**<br>

<figure><img src="../../.gitbook/assets/image (93).png" alt="" width="560"><figcaption></figcaption></figure>

When creating new attribute, check if it already exists or is used...

* 1\. Attribute name - needs to be unique and not too long ( as it will be displayed in the full display name of product...
* 2\. attribute code - not required, as it can add a part of code to product (variant) code. test before usage!
* 3\. display type - select behaviour / how it is displayed on various parts of odoo
* 4\. Variants creation mode&#x20;
  * Instantly - when product is created and attribute and values assigned, odoo will create all product variants
  * Dynamicly - odoo will create a product variant only ohen it is used in sales order/expense line for selected attrib
  * Never - product variants will never be created for any of these atrribute values

Important - this option canot be changed once the first product is configured with this attribute/values

* 5\. Attribute values - configure all possible values -\
  \- note: when configuring one product, you can use all or just selected attribute values\
  ![](<../../.gitbook/assets/image (94).png>)<br>
  * 1\. attribute VALUE name must be unique
  * 2\. the part of code added to product code for this value
  * 3\. Is custom value - if checked, every time will be required to enter custom value
