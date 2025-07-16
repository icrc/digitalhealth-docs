# Start the Repair process

{% hint style="info" %}
## Roles recommended :  Benchworker / Storekeeper
{% endhint %}

## **🧭** Context&#x20;

This step happens **after the repair order has been confirmed**. At this point, all the repair details are already filled in. The system will reserve the products needed for the repair. Then, the **Storekeeper** prepares these items and gives them to the **Technician**. Once the materials are ready, the technician can start the repair. This part of the process makes sure that everything needed for the repair is available and ready to use.

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



### Start the repair order

To start the repair process in Odoo, click on "Start Repair". If an error pop-up appears, refer to \[[this guide](broken-reference)].

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

If the configuration is correct, all components in the list should be in the "Waiting Another Move" state, indicating that a transfer is in progress to replenish the repair stock.&#x20;

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

The next step involves the storekeeper, who needs to go to "Resupply Repair" in the Inventory module to validate the transfer once the user collects the components. This step follows the standard stock move process, which you can review in detail \[here].

### Validate the resupply order

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

Once the transfer is validated, returning to the Repair Order will show that all components are now in the "Available" state, with their reserved quantities updated.

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

### End the repair

When the repair is complete, simply click on "End Repair". The repair process is now finalized, and the stock has been updated accordingly in Odoo.

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>



### 🗺️ Visual Overview&#x20;

```mermaid
graph LR
    A[Access the Repair Order] --> B[Start the Repair]
    B --> C[System Reserves the Product]
    C --> D[Storekeeper Prepares Items from Stock]
    D --> E[Items Handed to Technician]
    E --> F[Perform the Repair]
    F --> G[End the Repair]
```

## What's next?&#x20;

Once the repair is completed, the next step will depend on how your center is set up:

* If your center uses a **Quality Control** process, the repaired product will go through a quality check before it can be delivered. This step helps ensure that the item meets the required standards.
* If there is **no Quality Control step**, you can move directly to the **Delivery of the repaired product** to the Service User.

Both options are part of the final steps to make sure the Service User receives a functional and properly tracked item.

[^1]: Service provider
