# Delivering product to the SU

{% hint style="info" %}
## Roles recommended :  P\&O
{% endhint %}

## **🧭** Context&#x20;

This flow should be followed **after the Manufacturing Order has been validated** or **when a delivery has been manually created for a Service User (SU)**. At this stage, the product is ready for dispatch, and the delivery process must be completed to ensure the product reaches the SU and the stock is accurately updated.

## 🔄 Step-by-Step Flow&#x20;

### Accessing the Transfer order

{% tabs %}
{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the SU form, you'll find a tab labeled "**Stock items**". Clicking it will show all transfer orders associated with that specific Service User.&#x20;

<figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Via the Inventory application" %}
On the home page, go to the icon "Inventory".

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

You can view a list of all operation types from this page. Locate the operation type called **"Delivery Orders"**. Within this section, you'll find several useful links: a button that takes you to deliveries ready to be processed, a number indicating how many deliveries are currently waiting on another transfer, and another number showing the count of late deliveries.

<figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

Use the search bar at the top to find the correct delivery by their reference, by their patient name, SU[^1] ID ... Please ensure to select the correct option.
{% endtab %}
{% endtabs %}

### Validating the transfer order

In both cases, the process follows the step as for any other stock move. To see how to process it refer to “[Manage a stock move](../stock-management/)”.

<figure><img src="../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

&#x20;When validating this order, it signifies that the product has been received by the client and will no longer be available in stock. This action updates the inventory accordingly, reflecting the outgoing shipment and ensuring accurate stock management. This mark also the end of the process.



### 🗺️ Visual Overview&#x20;

```mermaid
graph LR
    B[Delivery Order Created]
    B --> C[Check Product Availability]
    C --> D{Are Products Available?}
    D -- Yes --> R1[Autofill]
    R1 --> L{Is the correct Lot number selected?}
    L -- Yes --> E[Validate Delivery Order]
    E --> G[Delivery Completed]
    L -- No --> F[Correct the Lot number]
    F --> R1

    D -- No --> H[Wait for internal transfer / Restock]
    H --> C
```

## What's next?&#x20;

By validating this order, you **confirm that the product** has been successfully delivered to the Service User and is no longer in stock. The inventory is automatically updated to reflect this change. With this final step completed, the process is now finished. No further action is required.

[^1]: Service provider
