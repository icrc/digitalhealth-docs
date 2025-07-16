# Managing MRP Order

{% hint style="info" %}
## Roles recommended :  P\&O, Benchworker
{% endhint %}

## **🧭** Context&#x20;

This flow should be followed **after the BoM configuration has been created**. &#x20;

## 🔄 Step-by-Step Flow&#x20;

### Creation of the MRP order

The creation of the MRP Order is being done on the form of the previous BoM Configuration.&#x20;

Once you have verified the components to be consumed and defined the operations in the BoM configuration, you can proceed to create a Manufacturing Order by clicking the "Create MRP Order" button located on the top ribbon.

<figure><img src="../../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>

This action initiates the creation of a Work Order that includes all the necessary components for consumption and will open in on a pop-up. The Work Order starts in a draft status.

{% hint style="info" %}
Even if you close the pop-up without saving the MRP order had been created
{% endhint %}

### Accessing the MRP order

{% tabs %}
{% tab title="From the BoM Configuration" %}
After the direct creation, you should still be on the BoM configuration, you can found within the form the direct link to the manufacturing order.

<figure><img src="../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

&#x20;
{% endtab %}

{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the SU form, you'll find a button labeled "**MRP Production**". Clicking it will open all manufacturing orders associated with that specific Service User.

<figure><img src="../../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Via the Inventory application" %}
On the home page, go to the icon "Manufacturing".

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

You can view a list of all Manufacturing Orders here. Use the search bar at the top to find the correct Manufacturing by their reference, by their patient name, SU[^1] ID ... Please ensure to select the correct option.

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Confirm an MRP order

It's important to note that depending on your security role, you may not have the authorization to confirm the MRP order. Typically, only physiotherapist, orthotist or authorized personnel can confirm this MRP order, ensuring that the manufacturing process proceeds accurately and according to plan.

_Technically: If the user does not have the role (group\_mrp\_manager), they will not see the "Confirm" button and will be unable to proceed with any actions related to confirming the Manufacturing Resource Planning (MRP). Only users with this specific role will have the "Confirm" button enabled._

Before proceeding to confirm the MRP, these authorized users must ensure that all products intended for consumption are thoroughly checked for accuracy. This includes verifying quantities and addressing any issues such as missing products.

&#x20;If adjustments are needed, the user can edit existing lines or create new ones following the same process for the BoM configuration outlined here.

Once all product details are correct, the user can proceed to confirm the MRP by clicking the "Confirm" button.

<figure><img src="../../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

Upon confirmation, the system will reserve the necessary stock for this order. Typically, products are available in the main stock but may need to be transferred to the workshop.

<figure><img src="../../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

By default, the system generates a transfer order from the main stock to the workshop, which can be accessed directly from the MRP order or through the Inventory module.

<figure><img src="../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

Additionally, if the Purchase module is properly configured, confirming the Purchase Order (PO) will trigger the creation of purchase orders to vendors. For more details on this process, refer to the specific guidelines provided.

### 🗺️ Visual Overview&#x20;

TODO Mermaid graph

## What's next?&#x20;

After finalizing the manufacturing order, the next step is to deliver the prosthesis to the Service User for the stock manager and for the P\&O to wait for this stock allocation for processing the Manufacturing order.

[^1]: Service provider
