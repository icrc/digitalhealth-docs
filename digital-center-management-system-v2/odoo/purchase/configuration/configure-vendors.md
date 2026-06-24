# Configure Vendors

> **Role:** DCMS Administrator **Module:** Purchase → Configuration → Vendors (Contacts)

Before any purchase order can be created, the vendor must exist as a **Contact** in the system with the correct settings. This is a one-time setup step per vendor.

***

#### 📋 What You Will Need

* The vendor's official company name
* Contact details: address, phone, email
* (Optional) Payment terms agreed with the vendor
* (Optional) The vendor's currency if different from your default

***

#### 🪜 Step-by-Step Instructions

**Step 1 — Open the Contacts module**

From the main menu, navigate to:

```
Contacts
```

> The vendor is stored as a **Contact**, not inside the Purchase module directly.

**Step 2 — Create a new contact**

Click **New** in the top-left corner.

**Step 3 — Fill in the vendor information**

| Field             | What to Enter                                    |
| ----------------- | ------------------------------------------------ |
| **Name**          | Official company name of the vendor              |
| **Company**       | Leave as _Company_ type (toggle at the top)      |
| **Address**       | Street, city, country                            |
| **Phone / Email** | Main contact details                             |
| **Tags**          | _(Optional)_ Add `Vendor` tag for easy filtering |

**Step 4 — Set the vendor-specific settings**

Go to the **Sales & Purchase** tab inside the contact form.

| Field             | What to Enter                                                 |
| ----------------- | ------------------------------------------------------------- |
| **Payment Terms** | Select the agreed payment terms (e.g. _30 days_, _immediate_) |
| **Currency**      | Set if the vendor invoices in a foreign currency              |
| **Company Type**  | Ensure it is set to _Company_                                 |

\{% hint style="info" %\} The **Payment Terms** field controls how the system generates payment due dates on vendor bills. Always confirm this with your finance team before saving. \{% endhint %\}

**Step 5 — Save the contact**

Click **Save** (or navigate away — Odoo saves automatically).

***

#### ✅ Result

The vendor is now registered in the system and can be:

* Selected when creating a **Request for Quotation (RFQ)**
* Linked to products in the product's **Purchase tab** (see Configure a Product for Purchase)

***

#### 💡 Tips

* Use the **search bar** in Contacts with the `Vendor` tag to quickly find all configured vendors.
* If a vendor also supplies to multiple centers, the same contact record is shared — do not duplicate it.
* You can add **multiple contacts** (individuals) under one vendor company using the **Contacts** tab inside the company record.

***

#### ❓ Troubleshooting

| Issue                                       | Solution                                                           |
| ------------------------------------------- | ------------------------------------------------------------------ |
| Vendor does not appear when creating an RFQ | Ensure the contact is saved and set as type _Company_              |
| Wrong currency on purchase orders           | Update the currency in the **Sales & Purchase** tab of the contact |
| Duplicate vendor entries                    | Merge contacts using the **Action → Merge** option                 |
