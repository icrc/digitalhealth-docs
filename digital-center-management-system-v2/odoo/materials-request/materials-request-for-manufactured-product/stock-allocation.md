# Stock allocation

{% hint style="info" %}
## Roles recommended :  P\&O, Stock Manager
{% endhint %}

## **🧭** Context&#x20;

This flow occurs **after the Manufacturing Order has been confirmed**. The Stock Manager is responsible for following this process to retrieve and reserve all necessary products and components for the manufacturing operation. By completing these steps in the system, the Stock Manager ensures that materials are correctly allocated, prepared, and validated before production begins.&#x20;

## 🔄 Step-by-Step Flow&#x20;

### Accessing the Materials request

{% tabs %}
{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the SU[^2] form, you will find a tab called "Stock Pickings", where all stock movements created for this [SU ](#user-content-fn-2)[^2]are listed. In this case, we will open the one with the "Waiting" status.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Via the Inventory application" %}
On the home page, go to the icon "Inventory".

<figure><img src="../../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>

You can view a list of all operation types from this page. Locate the operation type usually called **"Picking Components"**. Within this section, you'll find several useful links: a button that takes you to deliveries ready to be processed, a number indicating how many pickings are currently waiting on another transfer, and another number showing the count of late pickings.

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Use the search bar at the top to find the correct picking by their reference, by their patient name, SU[^1] ID ... Please ensure to select the correct option.
{% endtab %}
{% endtabs %}



## Material request form explanation

In this form, you can see the source location and the destination location on the top left. The scheduled date, the deadline, and the source document are displayed on the top right.

<figure><img src="../../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

&#x20;If it's an internal transfer, you will see a checkbox "Is recasting" that indicates whether the picking component is used for recasting. This checkbox is purely informational and does not perform any actions. To know more about recasting go to this section “Ask for recasting”.

There are two main tabs in this form: "Detailed Operations" and "Operations".

<figure><img src="../../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

The "Detailed Operations" tab shows the specific operations required for the stock move, including any reserved quantities and lot numbers if necessary.

The "Operations" tab shows the amount of product requested for the move. If the move is in draft status, only the "Operations" tab with the amount of product requested will be visible.

## Processing the materials request stock move

Click on the “Check availability” button to reserve the product, which will change the stock move status to "Ready".

<figure><img src="../../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

The user can print a PDF file to see which products need to be moved by clicking on the print button and selecting “Picking operations”. If the button is not visible, save the record, and the button will appear.

![](<../../../.gitbook/assets/image (50).png>)&#x20;

There are multiple ways to progress this order:

1\.     Clicking on "AutoFill", then click on “Validate”.

It will AutoFill all the quantities available in the tabs “Detailed operations”

2\.     Directly clicking on "Validate"¨

If no “Done quantities” are recorded, a pop-up will ask if you want to process all the reserved quantities before validating. If you apply it will AutoFill all the quantities available.

<figure><img src="../../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

3\.     Updating the quantity line by line.

Sometimes the reserved quantity is hidden. To show it, click on the three dots and select "Reserved quantity". This will display the quantity to be retrieved and the correct value to populate in the done column.

<figure><img src="../../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

&#x20;Once the quantities are correctly populated, click on "Validate". After validation, the system will ask if you want to create a backorder for any remaining products not yet delivered. If you want to deliver or pick up these components later, create a backorder. If you do not want to deliver the remaining products, select “No backorder”.

This step is mostly the same for Every stock move, only the Stock location / Destination change.

### 🗺️ Visual Overview&#x20;

```mermaid
graph TD
    A[Click 'Check Availability' button] --> B[Stock move status changes to 'Ready']
    B --> C[Click 'Print' button and select 'Picking operations']
    C --> D{Is 'Print' button visible?}
    D -- No --> E[Save the record]
    E --> C
    D -- Yes --> F[Print PDF of products to be moved]

    F --> G[Progress Order]

    subgraph Progress Options
        G --> H1[Click 'AutoFill' then 'Validate']
        G --> H2[Click 'Validate' directly]
        G --> H3[Update quantities line by line]
    end

    H2 --> I{Are 'Done quantities' recorded?}
    I -- No --> J[Popup: Process all reserved quantities?]
    J -- Yes --> H1
    J -- No --> K[Validate as is]

    H3 --> L[Click three dots > Select 'Reserved quantity' to show reserved qty]

    H1 & K & L --> M[Quantities populated correctly]

    M --> N[Click 'Validate']

    N --> O{Create backorder for remaining products?}
    O -- Yes --> P[Create backorder for later delivery]
    O -- No --> Q[Select 'No backorder' to skip remaining delivery]

    P & Q --> R[Process complete]

```

## What's next?&#x20;

After reserving and validating the components, the next step is to proceed with processing the Workorder within the Manufacturing Order (MRP). Depending on the outcome, there may also be an optional request for additional components, such as for recasting, if needed.

[^1]: Service provider

[^2]: Service User
