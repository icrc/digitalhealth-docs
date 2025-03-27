# Product Management

The most important main data in Odoo is product.\
Very important is to know and understand the difference between Product (model product.template) and Variant (model: product.product)\
Products and Variants are accessible from most odoo main menu items like: Sales, Stock, Invoicing, Purchase, MRP...\
Product menu item (model product.template) serves as main configuration menuitem.\
When product can be configured with attributes and pre configured values, upon saving it will create appropriate number of Variants\
Example: We configure a product : T-Shirt, then we set attributes\
\- Size, with values: S, M, L, XL, XXL\
\- Color: with values: White, Black, Blue\
on saving the Product, there will be 20 Variants (cartesium product ofd attribute values...\
Proper usage of attributes and attribute values is important for proper setting up the MRP BoM Templates as well as maintaining the center product catalog.\
Usable hints

* If product name contains any of usual attributes: Small, Child, Adult, Left, Right, etc... it should be configured with variants
