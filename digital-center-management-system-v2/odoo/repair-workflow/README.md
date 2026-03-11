# Repair Workflow

This flow describes the **complete repair process**, starting from the reception of the item from the Service User (SU) to the final delivery of the repaired product. It includes the interaction between the technician and the **Stock Keeper**, who plays a crucial role in managing stock availability and product preparation.

1. [**Reception & Repair Initiation**](get-the-product-to-repair.md)\
   The process begins when the Service User returns the item for repair. The technician selects the correct product and associated Lot Number, then validates the picking to confirm receipt.&#x20;
2. [**Repair Order Configuration**](create-the-repair-request.md)\
   A repair order is being created. In the repair form, the technician selects the product that needs to be repaired and validates the repair setup.
3. [**Stock Check & Preparation**](prepare-the-componenent-used-in-repair.md)\
   The system checks if the required parts or materials for the repair are available in stock:
   * **If not available**, a stock picking is created and sent to the **Stock Keeper**, who prepares the necessary items.
   * The Stock Keeper retrieves the correct product from stock, prepares it, and delivers it to the **benchworker**.
4. [**Repair Execution**](start-the-repair-process.md)\
   Once the needed items are available, the technician starts and performs the repair.
5. [**Delivery of Repaired Product**](deliver-the-repaired-item.md)\
   After the repair is completed, a delivery is created to return the repaired item to the Service User. Once validated, the delivery is closed, and the product is officially returned to the SU.

This flow ensures **traceability of parts**, **accurate inventory movement**, and clear **role separation** between stock management and repair execution.

### 🗺️ Visual Overview  <a href="#visual-overview" id="visual-overview"></a>

```mermaid
flowchart TD
    A([ Receive Item from Service User]) --> B[Select Correct Product\n& Lot Number]
    B --> C[Validate the Picking]
    C --> D[Create a Repair Order]
    D --> E[Select Parts to Add\nor Remove]
    E --> F[Confirm the Repair Order]

    F --> G{Stock available\nin repair location?}

    G -->|Yes| H[Start the Repair]

    G -->|No| SK1[Receive stock picking]
    SK1 --> SK2[Get correct product\nfrom stock]
    SK2 --> SK3[Prepare product]
    SK3 --> SK4[Deliver to Benchworker]
    SK4 --> H

    H --> I[Perform the Repair]
    I --> J[End the Repair]

    J --> M[Create Delivery\nto Service User]
    M --> N[Validate the Delivery]
    N --> O([✅ Repaired item\nreturned to Service User])

    subgraph stockkeeper["Stock Keeper"]
        SK1
        SK2
        SK3
        SK4
    end

    style A fill:#4A90D9,color:#fff,stroke:none
    style O fill:#27AE60,color:#fff,stroke:none
    style G fill:#2C3E50,color:#fff,stroke:none
    style stockkeeper fill:#FFF8E7,stroke:#E67E22,stroke-width:2px,color:#333
```

### 👥 Who Does What

| Step                         | Action                                                   | Role                      |
| ---------------------------- | -------------------------------------------------------- | ------------------------- |
| Get the product to repair    | Create the stock picking (receive item from SU)          | P\&O / Benchworker        |
| Get the product to repair    | Select product, lot number and validate the receipt      | P\&O / Benchworker        |
| Create the repair request    | Create the Repair Order and select parts to add / remove | P\&O / Benchworker        |
| Create the repair request    | Confirm the Repair Order                                 | P\&O / Benchworker        |
| Start the repair process     | Click "Start Repair" to trigger the resupply move        | Benchworker               |
| Start the repair process     | Validate the "Resupply Repair" stock transfer            | Storekeeper               |
| Start the repair process     | Perform the repair and click "End Repair"                | Benchworker               |
| Quality control _(optional)_ | Fill in the QC inspection checklist                      | Benchworker               |
| Quality control _(optional)_ | Approve or reject the quality check                      | Head of P\&O / Supervisor |
| Deliver the repaired item    | Click "Deliver Item" to create the delivery order        | Benchworker / Storekeeper |
| Deliver the repaired item    | Validate the delivery and return product to the SU       | Benchworker / Storekeeper |
