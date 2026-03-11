---
description: >-
  Manage Service Users (patients) in DCMS Odoo. Learn what data syncs from
  OpenMRS, how to find a Service User by name or SU ID, and how to use the
  Service User form (tabs, stock pickings, chatter).
---

# Service User Management

## Service User Management in Odoo (DCMS)

Use **Service User Management** in **DCMS Odoo ERP** to find and manage **Service Users (patients)** created in **OpenMRS**.

This supports rehabilitation center workflows, including prosthetics/orthotics services, admissions, stock, and delivery.

This list includes Service Users with a completed _Initial Decision Form_ in OpenMRS.

### What data is synchronized from OpenMRS?

Only **identification details** are synchronized to Odoo:

* Service User name
* Age
* Gender
* Address

No clinical data is transferred to Odoo.

{% hint style="info" %}
If you cannot access the module, check your role in [Roles & Tasks](roles-and-tasks/) and confirm you can [access Odoo](odoo-entry-point/accessing-odoo.md).
{% endhint %}

### Find a specific Service User (SU)

On the home page, go to the icon "Service User Management".

<figure><img src="../.gitbook/assets/image (160).png" alt="Odoo home page showing the Service User Management app icon"><figcaption></figcaption></figure>

You will see the full list of Service Users.

Use the search bar to find a Service User by:

* **Name**
* **Service User ID (SU ID)**

Select the right suggestion in the dropdown.

<figure><img src="../.gitbook/assets/image (161).png" alt="Odoo Service User list view with search bar and SU search options"><figcaption></figcaption></figure>

### Understand the Service User (SU) form

What you see depends on the modules enabled in your center.

At the top of the form, you will find quick actions for the Service User.

Common actions include:

* Create a **new admission** (Dormitory module)
* Configure **MRP** settings (Manufacturing module)

You will have more or fewer buttons based on your configuration and permissions.

<figure><img src="../.gitbook/assets/image (170).png" alt="Service User form in Odoo with top action buttons (admission, MRP, etc.)"><figcaption></figcaption></figure>

#### Tabs and related records

At the bottom, tabs provide additional records linked to the Service User.

<figure><img src="../.gitbook/assets/image (171).png" alt="Tabs on the Odoo Service User form showing related information sections"><figcaption></figcaption></figure>

#### Stock Pickings (stock movements)

In the **Stock Pickings** tab, you can view all **stock movements** for this Service User.

Each stock picking has a reference to identify the movement type.

<figure><img src="../.gitbook/assets/image (172).png" alt="Stock Pickings tab in Odoo showing stock movements linked to a Service User"><figcaption></figcaption></figure>

#### Chatter (notes, messages, activities)

Use the chatter to:

* Leave notes and messages about the Service User
* Schedule activities and follow-ups

<figure><img src="../.gitbook/assets/image (173).png" alt="Odoo chatter on a Service User record showing notes, messages, and scheduled activities"><figcaption></figcaption></figure>

### Related guides

* [Dormitory management](dormitory-management/)
* [Materials request](manufacturing-and-delivery/)
* [Stock Management](stock-management/)
