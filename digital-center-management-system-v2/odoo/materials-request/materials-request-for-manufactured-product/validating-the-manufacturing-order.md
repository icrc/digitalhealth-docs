---
description: How to confirm the Manufacturing Order
---

# Validating the Manufacturing Order

{% hint style="info" %}
Roles recommended : P&0&#x20;
{% endhint %}

## **🧭** Context&#x20;

This step takes place after **all work order steps have been successfully validated**, and **all used components are now available at the Workshop location**.&#x20;

The manufacturing process is complete, and the system is ready for the **final step of the Manufacturing Order** to confirm production completion.

## 🔄 Step-by-Step Flow&#x20;

### Accessing the Manufacturing order

{% tabs %}
{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the SU form, you'll find a button labeled "**MRP Production**". Clicking it will open all manufacturing orders associated with that specific Service User.

<figure><img src="../../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Via the Manufacturing application" %}
On the home page, go to the icon "Manufacturing".

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

You can view a list of all Manufacturing Orders here. Use the search bar at the top to find the correct Manufacturing by their reference, by their patient name, SU[^1] ID ... Please ensure to select the correct option.

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Validate the Manufacturing order

To validate a Manufacturing Order (MO), click on the “Mark Done” button. Several checks are performed during validation:

1.  If any work order is still open, a pop-up will inform you to complete all work orders first.\


    <figure><img src="../../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>
2.  If the consumed quantity differs, a pop-up will warn you. After reviewing, you can either “Confirm” or “Review the consumption” in more detail\


    <figure><img src="../../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>
3.  If no serial number was assigned, a pop-up will prompt you to provide a Lot/serial number.\
    \


    <figure><img src="../../../.gitbook/assets/image (132).png" alt=""><figcaption></figcaption></figure>

To assign a Lot/serial number, return to the MO, create a new Lot manually or click the + button to add the serial number, and re-validate the record.

<figure><img src="../../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

After resolving any issues, the MO status will change to “Done” and become read-only.&#x20;

The product manufactured will enter in the stock.&#x20;

### 🗺️ Visual Overview&#x20;

TODO Mermaid graph

## What's next?&#x20;

After finalizing the manufacturing order, the next step is to deliver the prosthesis to the Service User.





[^1]: Service provider
