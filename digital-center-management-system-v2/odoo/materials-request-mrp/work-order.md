# Work order



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

If the Tier Validation module is installed and the Work Order stage is Greenlight or any other validation step, only specific users will be able to validate this step. The user must request validation for this step by clicking the "Request Validation" button.  They will need to wait for approval before proceeding to the next step.

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

This process may vary depending on the center's configuration. The validation settings are directly managed within the Tier Validation module. To check the configuration, you can refer to the module settings.

_Example:_

In this example I’m connected as “Head of clinician”, the only role that can approve this step.

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

