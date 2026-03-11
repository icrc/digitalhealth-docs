# Receiving Purchased Products

{% hint style="info" %}
Recommend roles : Stock Managers, DCMS Admin
{% endhint %}

## 🧭 **Context**

This process takes place **after a Purchase Order has been confirmed** and the supplier has shipped the goods. Once the delivery is expected, the system automatically generates an **Incoming Shipment** (also known as a _Receipt_) that must be validated to record the products in stock.

This step ensures that inventory levels are updated, products are available for production or sales, and the vendor bill can be matched to the received quantities.

## 🔄 **Receiving Process (Step-by-Step)**

### **1. Access the Incoming Transfer**

* Go to **Inventory > Operations > Receipts**, or
* From the confirmed Purchase Order, click on the linked **Receipt** in the smart button area.

### **2. Click "Check Availability"**

* This reserves the incoming stock move.
* The status will change to **Ready**.

### **3. Print Picking List (Optional)**

* Click the **Print** button > Select **Picking Operations** to generate a PDF.
* If the button isn’t visible, make sure the transfer is saved.

### **4. Choose How to Record Quantities**

You have several ways to proceed:

* ✅ **AutoFill & Validate**
  * Click **AutoFill**, then **Validate**.
  * The system fills in the received quantities and confirms the receipt.
* ✅ **Validate Directly**
  * Click **Validate** without entering “Done” quantities.
  * A pop-up will prompt: _"Do you want to process all reserved quantities?"_
* ✅ **Manual Entry**
  * Enter the **Done** quantities line by line under the “Detailed Operations” tab.
  * If you don’t see reserved quantities, click the three dots ⚙️ and enable the _Reserved Quantity_ column.

### **5. Validate the Receipt**

* Once the correct quantities are filled in, click **Validate**.
* If not all items are received, Odoo will ask whether to **create a backorder**:
  * Choose **Backorder** if the rest will come later.
  * Choose **No Backorder** if the remaining items will not be delivered.

***

## 🎯 **What’s Next**

After validating the receipt, the products are now officially in stock. The next step is typically to proceed with **registering the vendor bill** if it hasn’t been created yet, or to update the bill with the actual received quantities.
