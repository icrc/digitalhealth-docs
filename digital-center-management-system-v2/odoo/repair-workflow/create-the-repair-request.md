# Create the repair request

{% hint style="info" %}
## Roles recommended :  P\&O, Benchworker
{% endhint %}

## **🧭** Context&#x20;

This step takes place **after the product has been received for repair** and properly registered in the system. At this point, the item is physically available in the repair location, and the repair process can begin. The following flow focuses on the **creation and configuration of the Repair Order**, which will define the work to be done and the components involved. Whether you initiate the repair from the **Service User form** or directly from the **Repair list view**, this process ensures the repair is properly tracked and aligned with inventory movements.

## 🔄 Step-by-Step Flow&#x20;

### Creation of the Repair order

{% tabs %}
{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the Service User (SU) form, you’ll find a button labeled **"New repair order"**. Clicking this button will trigger the creation of a repair order, allowing the system to know the product to repair.

<figure><img src="../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Via the Repair application" %}
On the home page, go to the icon "Repairs".

<figure><img src="../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

You can view the list of existing repair orders from the **Repair Orders** menu. To initiate a new repair process, simply click on the **"Create"** button.

<figure><img src="../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Via the previous step" %}

{% endtab %}
{% endtabs %}

If you have selected a Service User where the product to repair was not been received correctly, a pop-up will appear warning that no items belong to this SU. In this case, return to the previous step, “[Get the product to repair.](get-the-product-to-repair.md)”

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

Otherwise, after selecting the partner, the system will automatically identify the product received for repair, and you will be directed to the repair order form.

### Configuring the repair order

The form contains two essential tabs.\
The first is the **"Parts"** tab. This section lists all the products that will be either used or removed from a specific manufactured product during the repair process.\
Here, you can add new entries by clicking on **"Add a line"**. When adding a line, you’ll have the option to specify whether a product is being **added** (used in the repair) or **removed** (taken out of the original item).

{% hint style="danger" %}
Only include items that will be used during the repair (such as bandages or replacement feet). Do not select the item that is being repaired.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (267).png" alt=""><figcaption></figcaption></figure>

If "Removed" is selected, you can modify the destination location to either return the product to stock or move it to the scrap location.

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

The second tab is "Operations". This section includes all service products required during the repair. It is mainly used for invoicing specific services, such as labor or materials, to the patient.

{% hint style="info" %}
This tab is only relevant if the center is using the **Invoicing** module.
{% endhint %}

Once everything is set up, the next step is to confirm the repair by clicking on "Confirm Repair".

<figure><img src="../../.gitbook/assets/image (268).png" alt=""><figcaption></figcaption></figure>

### 🗺️ Visual Overview&#x20;

```mermaid
graph LR
    A[Start: From SU Form]
    A1[Start: From Repair list view]
A --> B 
A1--> B
    B[Create Repair Order]
    B --> C[Verify Selected Product]
    C --> D[Add/Remove Components for Repair]
    D --> E[Confirm the Repair]
```

## What's next?&#x20;

After the confirmation of the repair order, the next step is to initiate the repair process by retrieving the required products from stock and moving them to the designated repair location (e.g., "WH/Repair"). This operation is carried out by the Stock Manager, who ensures that all necessary components are physically available at the repair site. It is important to note that the repair workflow cannot proceed until this stock move is completed, as the materials must be present and correctly registered in the system before any repair activities can begin.



[^1]: Service provider
