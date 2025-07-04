# How to create Automatic replenishment

## 🧭 **Context**

This flow is used to **automatically generate Purchase Orders** when the stock level of a product drops below a configured threshold. It's commonly used for frequently consumed items, raw materials, or essential stock that must never run out.

The system checks **Reordering Rules**, **Routes**, and **Supplier information** to determine when and how to trigger replenishment. This ensures stock continuity without manual tracking.

## 🔄 **Replenishment Flow (Step-by-Step)**

### **Set a Reordering Rule**

* Go to **Inventory > Products > Reordering Rules**.
* Choose the product and define:
  * **Minimum Quantity**: When stock falls below this, Odoo will replenish.
  * **Maximum Quantity**: The system will reorder enough to reach this level.
  * **Location**: Define where the rule applies (e.g., WH/Stock).

### **Ensure Vendor Information is Set**

* Open the **Product** form.
* Under the **Purchase** tab, add at least one **Vendor**, with pricing and delivery lead time.
* The vendor must match the company and be marked as a supplier.

### **Check Routes & Procurement Method**

* Product must have a **Buy route** enabled.
* The **Procurement Method** should be _When stock is needed_ (default behavior).

### **Trigger Replenishment**

* Either wait for the **scheduled procurement job** (runs automatically based on settings), or:
* Manually trigger from:
  * **Inventory > Operations > Run Replenishment**
  * Or from the **Product** → "Replenish" button (manual trigger)

### **Review the Draft Purchase Order**

* Once triggered, Odoo creates a **draft Request for Quotation (RFQ)** with suggested quantities.
* You can review, adjust, and **confirm** it to create a Purchase Order.

## 🗺️ Visual Overview&#x20;

```mermaid
graph LR
    A[Stock Drops Below Min Quantity] --> B[Reordering Rule Triggered]
    B --> C[Vendor & Route Info Checked]
    C --> D[Draft Purchase Order Created]
    D --> E[Review and Confirm PO]
    E --> F[Receipt Created and Products Delivered]
    F --> G[Stock Replenished]

```

## **What’s Next**

After confirming the Purchase Order, follow the regular flow: the supplier ships the goods, you receive them in stock, and then process the vendor bill.
