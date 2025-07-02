# Managing stock move

## What is a stock move :&#x20;

In Odoo, a **Stock Move** represents the transfer of a product from one location to another and is essential for inventory management. It can be triggered by various operations such as manufacturing, internal transfers, or warehouse adjustments, Every move is linked to an Operations types that define the processus and the Source/destination location.

A stock move goes through different statuses: it starts as **Draft**, then moves to **Waiting for Availability** while Odoo checks if the required stock is present. Once available, it becomes **Ready**, and after validation, it is marked as **Done**, updating inventory levels.

During processing, stock moves may require validation, either manually or through automated rules like FIFO or FEFO. Depending on warehouse settings, operations can involve barcode scanning, batch picking, or multi-step transfers. Additionally, products can be tracked using **Lot Numbers** or **Serial Numbers** to ensure traceability.

&#x20;Once completed, the stock move updates the **source location** by reducing stock and increases stock in the **destination location**. If **perpetual inventory valuation** is enabled, the transaction is logged in inventory records.



## Process of any stock move

Click on the “Check availability” button to reserve the product, which will change the stock move status to "Ready".

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

The user can print a PDF file to see which products need to be moved by clicking on the print button and selecting “Picking operations”. If the button is not visible, save the record, and the button will appear.

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

There are multiple ways to progress this order:

1\.     Clicking on "AutoFill", then click on “Validate”.

It will AutoFill all the quantities available in the tabs “Detailed operations”

2\.     Directly clicking on "Validate"¨

If no “Done quantities” are recorded, a pop-up will ask if you want to process all the reserved quantities before validating. If you apply it will AutoFill all the quantities available.

<figure><img src="../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

3\.     Updating the quantity line by line.

Sometimes the reserved quantity is hidden. To show it, click on the three dots and select "Reserved quantity". This will display the quantity to be retrieved and the correct value to populate in the done column.

<figure><img src="../../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>

Once the quantities are correctly populated, click on "Validate". After validation, the system will ask if you want to create a backorder for any remaining products not yet delivered. If you want to deliver or pick up these components later, create a backorder. If you do not want to deliver the remaining products, select “No backorder”.

This step is mostly the same for Every stock move, only the Stock location / Destination change.

### 🗺️ Visual Overview&#x20;

```mermaid
flowchart TD
    A[Start - Stock Move Initiated] --> B[Create a Stock Picking]
    B --> C[Add Products and Quantities]
    C --> D[Choose Source and Destination Locations]
    D --> E[Confirm Picking]
    E --> F[Check Availability]
    F --> G{Is stock available?}
    G -- Yes --> H[Reserve Stock]
    G -- No --> I[Wait for Replenishment / Manual Reserve]
    H --> J[Validate Picking]
    J --> K[Stock Quant Updated]
    K --> L[Stock Move Completed]
    I --> G

```

