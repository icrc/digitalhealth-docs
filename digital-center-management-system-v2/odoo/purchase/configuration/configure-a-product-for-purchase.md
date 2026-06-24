# Configure a Product for Purchase

> **Role:** DCMS Administrator **Module:** Inventory → Products _or_ Purchase → Products

Each product that is purchased from a vendor must be configured with the correct **vendor information**, including the vendor's reference and unit price. This allows the system to pre-fill purchase orders automatically and ensures accurate pricing.

***

#### 📋 What You Will Need

* The product already created in Odoo
* The vendor already configured as a contact (see Configure a Vendor)
* The vendor's unit price for this product
* (Optional) The vendor's internal reference code for the product
* (Optional) The vendor's minimum order quantity and delivery lead time

***

#### 🪜 Step-by-Step Instructions

**Step 1 — Open the product**

Navigate to the product using either path:

```
Inventory → Products → Products
```

or

```
Purchase → Products → Products
```

Search for the product by name and open it.

**Step 2 — Go to the Purchase tab**

Inside the product form, click on the **Purchase** tab.

> This tab contains all vendor-specific settings for this product.

**Step 3 — Add a vendor line**

In the **Vendors** section, click **Add a line**.

A new row will appear. Fill in the following fields:

| Field                     | Description                                                | Example                    |
| ------------------------- | ---------------------------------------------------------- | -------------------------- |
| **Vendor**                | Select the vendor from the list of contacts                | _ABC Medical Supplies_     |
| **Vendor Product Name**   | The name the vendor uses for this product _(optional)_     | _Bandage 10cm ref. BND-10_ |
| **Vendor Product Code**   | The vendor's internal reference or catalogue number        | _BND-10-REF_               |
| **Delivery Lead Time**    | Number of days between order and expected delivery         | _5_                        |
| **Price**                 | The unit price agreed with this vendor                     | _2.50_                     |
| **Min. Quantity**         | Minimum order quantity required by the vendor _(optional)_ | _50_                       |
| **Currency**              | Currency of the price _(defaults to vendor's currency)_    | _USD_                      |
| **Date Start / Date End** | _(Optional)_ Validity period for this price                | _01/01/2025 – 31/12/2025_  |

\{% hint style="info" %\} You can add **multiple vendor lines** for the same product if you source it from several vendors. When creating a purchase order, Odoo will suggest the vendor with the **lowest price** or the **preferred vendor** listed first. \{% endhint %\}

**Step 4 — Set the product's purchase settings**

Still in the **Purchase** tab, review these additional settings:

| Field                    | Description                                                                                                 |
| ------------------------ | ----------------------------------------------------------------------------------------------------------- |
| **Control Policy**       | Choose _On ordered quantities_ or _On received quantities_ — this controls when vendor bills can be created |
| **Purchase Description** | Text that will appear on the purchase order line for this product                                           |

**Step 5 — Check the General Information tab&#x20;**_**(if needed)**_

Go back to the **General Information** tab and confirm:

| Field               | Expected Value                                                                                    |
| ------------------- | ------------------------------------------------------------------------------------------------- |
| **Product Type**    | _Storable Product_ (for items tracked in inventory)                                               |
| **Unit of Measure** | Must match the unit used in purchase orders                                                       |
| **Purchase UoM**    | Set if the vendor sells in a different unit (e.g. vendor sells by _box_, stock tracked by _unit_) |

**Step 6 — Save the product**

Click **Save** (or navigate away — Odoo saves automatically).

***

#### ✅ Result

The product is now linked to the vendor with the correct price and reference. When a **Request for Quotation** is created:

* The vendor will be pre-suggested based on the product's vendor list
* The unit price will be filled in automatically
* The vendor's product code will appear on the purchase order for easy cross-referencing with the vendor's invoice

***

#### 💡 Tips

* Always enter the **Vendor Product Code** — this is essential for matching your PO lines with the vendor's invoice and avoiding errors during reception.
* If prices change periodically, use the **Date Start / Date End** fields to manage price validity without deleting old lines.
* The **Delivery Lead Time** directly impacts the system's suggested order date when using automatic replenishment — keep it up to date.
* To update prices for many products at once, use **Purchase → Configuration → Vendor Pricelists** (if enabled).

***

#### ❓ Troubleshooting

| Issue                                       | Solution                                                                                 |
| ------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Vendor price not pre-filled on the RFQ      | Check that a vendor line exists in the product's **Purchase** tab for that vendor        |
| Wrong unit of measure on the purchase order | Verify **Purchase UoM** in the General Information tab                                   |
| Product not available when creating a PO    | Ensure the product is set to **Can be Purchased** (checkbox in the Purchase tab header)  |
| Lead time not respected by replenishment    | Update the **Delivery Lead Time** in the vendor line to match the vendor's actual delays |
