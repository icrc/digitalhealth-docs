# Repair Process



🔄 Repair Workflow Overview

This flow describes the **complete repair process**, starting from the reception of the item from the Service User (SU) to the final delivery of the repaired product. It includes the interaction between the technician and the **Stock Keeper**, who plays a crucial role in managing stock availability and product preparation.

1. **Reception & Repair Initiation**\
   The process begins when the Service User returns the item for repair. The technician selects the correct product and associated Lot Number, then validates the picking to confirm receipt. A **Repair Order** is then created.
2. **Repair Order Configuration**\
   In the repair form, the technician selects the product that needs to be repaired and validates the repair setup.
3. **Stock Check & Preparation**\
   The system checks if the required parts or materials for the repair are available in stock:
   * **If not available**, a stock picking is created and sent to the **Stock Keeper**, who prepares the necessary items.
   * The Stock Keeper retrieves the correct product from stock, prepares it, and delivers it to the **benchworker**.
4. **Repair Execution**\
   Once the needed items are available, the technician starts and performs the repair.
5. **Delivery of Repaired Product**\
   After the repair is completed, a delivery is created to return the repaired item to the Service User. Once validated, the delivery is closed, and the product is officially returned to the SU.

This flow ensures **traceability of parts**, **accurate inventory movement**, and clear **role separation** between stock management and repair execution.

### 🗺️ Visual Overview  <a href="#visual-overview" id="visual-overview"></a>

```mermaid
flowchart TD
 subgraph askProduct["Stock Keeper"]
        G0["Receive stock picking"]
        G2["Prepare Product"]
        G1["Get Correct Product from Stock"]
        G3["Deliver to Benchworker"]
  end
    A["Receive Item from Service User"] --> B["Select Correct Product & Lot Number"]
    B --> C["Validate the Picking"]
    C --> D["Create a Repair Order"]
    D --> E["Select Product for Repair"]
    E --> F["Validate the Repair"]
    F --> n1["Is Stock Available?"]
    G1 --> G2
    G2 --> G3
    G["Retrieve stock from the store keeper"] --> H["Start the Repair"]
    H --> I["End the Repair"]
    I --> J["Create Delivery to Service User"]
    J --> K["Close the Delivery"]
    n1 -- No --> G0
    n1 -- Yes --> H
    G3 --> G
    G0 --> G1

    n1@{ shape: diam}
 click A href "https://icrc.gitbook.io/dcms/odoo/repair-process/get-the-product-to-repair"

```

