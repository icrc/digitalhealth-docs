# Start the Repair process

{% hint style="info" %}
## Roles recommended : &#x20;
{% endhint %}

## **🧭** Context&#x20;



## 🔄 Step-by-Step Flow&#x20;

### Access the Repair order

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





To start the repair process in Odoo, click on "Start Repair". If an error pop-up appears, refer to \[[this guide](broken-reference)].

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

If the configuration is correct, all components in the list should be in the "Waiting Another Move" state, indicating that a transfer is in progress to replenish the repair stock.&#x20;

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

The next step involves the storekeeper, who needs to go to "Resupply Repair" in the Inventory module to validate the transfer once the user collects the components. This step follows the standard stock move process, which you can review in detail \[here].

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

Once the transfer is validated, returning to the Repair Order will show that all components are now in the "Available" state, with their reserved quantities updated.

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

When the repair is complete, simply click on "End Repair". The repair process is now finalized, and the stock has been updated accordingly in Odoo.

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

[^1]: Service provider
