# How to create new product

## **🧭** Context&#x20;



## Difference between Product and Product Variant&#x20;

```mermaid
flowchart TD
    A["Start - Create New Product"] --> B["Set Product Name & Type (Storable, Consumable, Service)"]
    B --> C["Configure Basic Info (Category, Barcode, UoM, etc.)"]
    C --> n1["Does your product contains variant ? (color,size ...)"]
    D["Go to Variants Tab"] --> E["Add Attributes (e.g., Color, Size)"]
    E --> F["Define Attribute Values (e.g., Red, Blue, Small, Large)"]
    F --> G["System Automatically Generates Variants"]
    G --> H["Review / Adjust Each Variant (Prices, Codes, etc.)"]
    J["Save Product"] --> K["Product was created successfully"]
    n1 -- Yes --> n2(["Creation of product with variant"])
    n1 -- No --> n3(["Creation of product without variant"])
    H --> J
    n2 --> D
    n3 --> J

    n1@{ shape: diam}
    click n2 "https://app.gitbook.com/o/llCOVrc7ZrWQ6rzyYOmd/s/nTWGcVv7ikvz7HIC0Dby/~/changes/58/odoo/product-management/creation-of-product/creating-a-product-with-variants"
    click n3 "https://app.gitbook.com/o/llCOVrc7ZrWQ6rzyYOmd/s/nTWGcVv7ikvz7HIC0Dby/~/changes/58/odoo/product-management/creation-of-product/creating-a-product-without-variants"


```

