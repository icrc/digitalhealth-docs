# Get the product to repair

{% hint style="info" %}
## Roles recommended :  ??
{% endhint %}

## **🧭** Context&#x20;

To begin the repair process, the first essential step is to receive the product that requires repair. This ensures that the item is properly registered and tracked within the system to be repaired.&#x20;

## 🔄 Step-by-Step Flow&#x20;

### Creation of the stock picking

{% tabs %}
{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the Service User (SU) form, you’ll find a button labeled **"Receive items for Repair"**. Clicking this button will trigger the creation of a stock move, allowing the system to register the product to repair.

<figure><img src="../../.gitbook/assets/image (269).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Via the Repair application" %}
On the home page, go to the icon "Repairs".

<figure><img src="../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

At the top of the screen, you'll find a button labeled **"Receive for Repair"**. Clicking this button will create a stock move, allowing the system to register the product being returned for repair.

<figure><img src="../../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Processing the receipt order

Begin by ensuring that the correct SU has been selected in both the **"Receive From"** and **"Owner"** fields. This ensures that the product being returned is properly linked to the right Service User.

<figure><img src="../../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>

Make sure the **Destination Location** is set to **"WH/Repair"**, which indicates that the product will be received in the workshop for repair.

In the **"Operations"** tab, add a new line with the product that needs to be repaired (e.g., a prosthesis).

<figure><img src="../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
Do not include items that will be used during the repair (such as bandages or replacement feet). Only select the item that is being repaired.
{% endhint %}

After confirming the product and attributes are correct, click **Save**.\
A new button labeled **"Mark as To Do"** will appear. Click this button to progress the repair intake.

<figure><img src="../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

A new tab named **"Detailed Operations"** will now be visible.

Open this tab and select the correct **Lot Number** that corresponds to the prosthesis linked to the SU.

{% hint style="info" %}
If the prosthesis was not previously recorded in the system, you can create a **new serial number** at this step.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>



Once the correct lot number has been selected, click the **"Validate"** button. This will confirm the receipt of the item and update stock accordingly.

### 🗺️ Visual Overview&#x20;

```mermaid
graph TD
    A["Start: Click 'Receive for Repair'"] --> B["Select correct SU in 'Receive From' and 'Owner'"]
    B --> C["Ensutre that 'Destination Location' is 'WH/Repair'"]
    C --> D["Go to 'Operations' tab"]
    D --> E["Add the product to repair (e.g. prosthesis)"]
    E --> H[Click Save]
    H --> I[Click 'Mark as To Do']
    I --> J["Open 'Detailed Operations' tab"]
    J --> K[Select the correct Lot number]
    K --> L{Lot exists?}
    L -- No --> M[Create new serial number]
    L -- Yes --> N[Confirm selection]
    M --> N
    N --> O[Click 'Validate']
    O --> P[✅ Product received for repair]
```

## What's next?&#x20;

After the product has been successfully received for repair and registered in the system, the next step is to create the repair order. This order will define the item to be repaired and outline the components or materials required for the repair process.

[^1]: Service provider
