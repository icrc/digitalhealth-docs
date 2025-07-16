# Deliver the repaired Item

{% hint style="info" %}
## Roles recommended :  Benchworker / Storekeeper
{% endhint %}

## **🧭** Context&#x20;



## 🔄 Step-by-Step Flow&#x20;

### Access the Repair order

If you're **not already inside a Repair Order**, follow the steps below to access one.\
If you're **already in an existing Repair Order**, you can skip this part and move on to the next step.

{% tabs %}
{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the Service User (SU) form, you’ll find a tab labeled **"Repair orders"**. Opening this tab will show the list of all the repair order link to this specific SU.&#x20;

<figure><img src="../../.gitbook/assets/image (281).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Via the Repair application" %}
On the home page, go to the icon "Repairs".

<figure><img src="../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

You can view a list of all Repair order here. Use the search bar at the top to find the correct repair by their reference, by their product to repair, SU[^1] ID ... Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Create the delivery item

On the Repair form, click the **"Deliver Item"** button. This will automatically create a **Delivery Order** to handle the return of the repaired product to the Service User.

<figure><img src="../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

The deliver order is now created and marked as ready, will appear in the Service User (SU) form under the "Stock Picking" tab. This picking record will have a specific name that typically includes "RMA-OUT," indicating that it is a repair (RMA) being sent out.&#x20;



<figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

You can also find the same stock move in the Inventory module under the "Deliver REPAIRED" picking type.

<div align="left"><figure><img src="../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure></div>

Once the Stock Picking is open, the process follows the same steps as any other picking. Simply click on "Auto-Validate," and the correct quantity will be set automatically.

<figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

If the product has a Lot Number, verify that the correct one is assigned before proceeding. Then, click on the "Validate" button to update the status to Done.

For more details on managing stock picking, please refer to this [Guideline](../stock-management/).

### 🗺️ Visual Overview&#x20;

```mermaid
graph TD
    A[Open the Repair Order form] --> B[Click Deliver Item button]
    B --> C[Delivery Order is created and marked as Ready]
    C --> D["Delivery appears in SU form under Stock Picking tab(RMA-OUT)"]
    C --> E[Delivery also visible in Inventory > Deliver REPAIRED]
    D --> F[Open the Delivery Order]
    E --> F
    F --> G[Click Auto-Validate]
    G --> H{Does the product have a Lot Number}
    H -- Yes --> I[Verify Lot Number is correct]
    H -- No --> J[Proceed to validation]
    I --> K[Click Validate to mark as Done]
    J --> K

```

## What's next?&#x20;

Once the delivery is validated and completed, it confirms that the patient has received their repaired product. The system will automatically update the stock to reflect this. This step marks the official end of the repair process.

[^1]: Service provider
