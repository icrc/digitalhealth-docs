# Processing Work order

{% hint style="info" %}
## Roles recommended :  P\&o, Benchworker
{% endhint %}

## **🧭** Context&#x20;

This step takes place **after the manufacturing order has been created** and **required components have been received at the Workshop location**. At this point, the work order is ready to be processed, and the system may require validation before execution can begin—depending on your installation’s configuration.

## 🔄 Step-by-Step Flow&#x20;

### Accessing the Manufacturing order

{% tabs %}
{% tab title="Via the SU management" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the SU form, you will find two buttons: "[**MRP**](#user-content-fn-2)[^2] **Production**" and "[**MRP**](#user-content-fn-2)[^2] **Workorder**". The first opens the full production order, while the second opens only the specific workorder to be processed.

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Via the Manufacturing application" %}
On the home page, go to the icon "Manufacturing".

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

You can view a list of all Manufacturing Orders here. Use the search bar at the top to find the correct Manufacturing by their reference, by their patient name, SU[^1] ID ... Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### Workorder Steps

Inside the **Manufacturing Order**, you will find a tab called **"Work Orders"**.

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

This tab contains all the steps that need to be completed by the workshop. The user must progress through each Work Order step by step before the manufacturing process is complete..

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

Each step has a “Start”/ ”Block” button.

·       When starting a Work Order, a timer will begin until the user “Pauses” or marks it as “Done”.

·       This will help to track the time for each step.

{% hint style="info" %}
Currently only 1 person can start the step even if there is multiple person working on it.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

Depending on your installation’s configuration, certain work order stages—such as Greenlight—may require mandatory validation. In such cases, only authorized users can approve the step. To proceed, the user must click the Request Validation button and wait for approval before continuing to the next stage.

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

_Example:_

In this example I’m connected as “Head of clinician”, the only role that can approve this step.

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

### 🗺️ Visual Overview&#x20;

```mermaid
graph LR
 subgraph PW_PO["P&O / Head of P&O"]
        PW_PO_01["Validation"]
  end
    PW_01["Starting the Step"]
    PW_02["Doing the work"]
    PW_03["Is validation step"]
    PW_04["Is Last step"]
    PW_05["Finalize Manufacturing Process"]
    PW_06["Restart Process"]
    PW_07["Close the step"]
    PW_01 --> PW_02
    PW_02 --> PW_03
    PW_03 -- Yes --> PW_PO 
    PW_03 -- No --> PW_07
    PW_04 --> PW_05 & PW_06
    PW_07 --> PW_04
    PW_PO --> PW_07
PW_06
    PW_04@{ shape: diam}
    PW_03@{ shape: diam}
```

## What's next?&#x20;

After completing the work order processing, the next step is the **validation of the Manufacturing Order** to confirm everything is ready for production completion.





[^1]: Service provider

[^2]: Manufacturing Resource Planning
