---
description: New service and follow up/repair (worflow in details)
---

# Workflow User Journey

Register the HSU or find the HSU file coming to the PRC

### a. Workflow new service&#x20;

{% stepper %}
{% step %}
### Start the visit

<mark style="color:green;">Initial decision after registration</mark> and decision to send for new service (save and validate)
{% endstep %}

{% step %}
### Initial Assessment (interdisciplinary team)

* <mark style="color:green;">Initial outcome and goal setting (optional assessments)</mark>
* <mark style="color:green;">Basic service plan + clinical consent (plan service)</mark>
{% endstep %}

{% step %}
### Financial capacity assessment

<mark style="color:green;">(if not approved) Socioeconomic assessment+ Financing decision</mark>
{% endstep %}

{% step %}
### Services&#x20;

Technical cards

Physiotherapy assessment

Wheelchair assessment

Walking Aids

Club foot

Cerebral palsy
{% endstep %}

{% step %}
### Final assessment Outcome and goal setting (Automatic closure of service)

Appointment for follow up visit
{% endstep %}
{% endstepper %}

```mermaid

  flowchart TB
    %% Main workflow
    A["Register the HSU or find the HSU file coming to the PRC"] --> 
    B["Start the visit"] --> 
    C["Initial decision after registration and decision to send for new service (save and validate)"] --> 
    D["Initial Assessment (interdisciplinary team)"]

    %% Optional assessment
    D -.-> D2["Optional Assessment"]

    D --> E["Initial outcome and goal setting + Basic service plan + clinical consent"]
    E --> E1["Plan Service"]
    E1 --> F["Financial capacity assessment + socio-economic assessment"]
    E2 --> F["Financing decision if financial capacity is not approved"]
    F --> G["Any Services"]

    %% Subgraph for services (no label), all connect directly to Final Assessment
    subgraph "" direction LR
        G --> G1["Technical cards"]
        G --> G2["Physiotherapy assessment"]
        G --> G3["Wheelchair assessment"]
        G --> G4["Walking Aids"]
        G --> G5["Club foot"]
        G --> G6["Cerebral palsy"]
    
    G1 --> K
    G2 --> K
    G3 --> K
    G4 --> K
    G5 --> K
    G6 --> K

    %% Final steps
    K["Final assessment Outcome and goal setting + Automatic closure of service"]
    K --> L["Appointment for follow-up visit"]

    %% Styling
    classDef default fill:#f0f0f0,stroke:#333,stroke-width:1.5px;
    classDef optional stroke-dasharray: 5 5,stroke:#888,fill:#ffffff;
    class D2 optional;
```

### b. Workflow new service with intermediate assessment&#x20;

**In the case you need to adjust the service;**

* To add a product or additional service (such as additional physiotherapy sessions)
* To assess the progress and the objectives of the treatment; you can follow the next step.&#x20;

{% stepper %}
{% step %}
### Service&#x20;

Physiotherapy, Technical card, Wheelchair, Club Foot, Cerebral Palsy, Walking aids
{% endstep %}

{% step %}
### Intermediate Assessment Outcome and Goal setting

Decision: Adjust service if required&#x20;
{% endstep %}

{% step %}
### Basic Service Plan

Add the service (s)
{% endstep %}

{% step %}
### Financial Capacity Assessment&#x20;

if not approved:

* Select make **socioeconomic** and complete **Financing Decision**
* Select **Socioeconomic** already recorded, if you select this option you can already go to **Financing Decisio**n.
{% endstep %}

{% step %}
### Service (s)
{% endstep %}

{% step %}
### Final assessment Outcome and goal setting (Automatic closure of service)

Appointment for follow up visit
{% endstep %}
{% endstepper %}

```mermaid
flowchart TB
    %% Main workflow
    A["Register the HSU or find the HSU file coming to the PRC"] --> 
    B["Start the visit"] --> 
    C["Initial decision after registration and decision to send for new service (save and validate)"] --> 
    D["Initial Assessment (interdisciplinary team)"]

    %% Optional assessment
    D -.-> D2["Optional Assessment"]

    D --> E["Initial outcome and goal setting + Basic service plan + clinical consent"]
    E --> E1["Plan Service"]
    E1 --> F["Financial capacity assessment + socio-economic assessment (completed with financing decision if financial capacity is not approved)"]
    F --> G["Any Services"]

    %% Subgraph for services
    subgraph "" direction LR
        G --> G1["Technical cards"]
        G --> G2["Physiotherapy assessment"]
        G --> G3["Wheelchair assessment"]
        G --> G4["Walking Aids"]
        G --> G5["Club foot"]
        G --> G6["Cerebral palsy"]
        %% Intermediate Assessment after subgraph
    G1 --> H["Intermediate Assessment and Goal Setting "]
    G2 --> H
    G3 --> H
    G4 --> H
    G5 --> H
    G6 --> H

    %% Decision paths
    H -- Yes --> I["Adjust service + new plan + financial review"]
    H -- No --> K["Final assessment Outcome and goal setting + Automatic closure of service"]

    I --> J["Additional Services"]
    J --> K
    K --> L["Appointment for follow-up visit"]

    %% Styling
    classDef default fill:#f0f0f0,stroke:#333,stroke-width:1.5px;
    classDef optional stroke-dasharray: 5 5,stroke:#888,fill:#ffffff;
    class D2 optional;

```



### C. Workflow Repair or Follow up

{% stepper %}
{% step %}
### Register the HSU or find the HSU file coming to the PRC&#x20;


{% endstep %}

{% step %}
### Start the visit (Open the Episode of service)

Initial decision after registration and decision to send for follow up (save and validated)
{% endstep %}

{% step %}
### Service Follow up Assessment&#x20;

Decision: Follow up/repair or New Interdisciplinary assessment or end the follow up
{% endstep %}

{% step %}
### Financial capacity assessment

If not approved complete the socioeconomic already recorded&#x20;

* decision&#x20;
{% endstep %}

{% step %}
### Service Follow up Plan (Automatic closure of Episode of service)

If AT repair is yes, select the pertinent service category options with the Adjustment or/and Repair as service.
{% endstep %}
{% endstepper %}







```mermaid
flowchart TB
    %% Main flow
    A["Register the HSU or find the HSU file coming to the PRC"] --> 
    B["Start the visit (Open the Episode of service)"] --> 
    C["Initial decision after registration and decision to send for follow-up (save and validated)"] --> 
    D["Service Follow-up Assessment"] --> 
    E["Decision: Follow-up/Repair OR New Interdisciplinary Assessment OR End the follow-up"]

    %% Follow-up path
    E --> F["Financial capacity assessment"]
    F --> G["If not approved: complete the socioeconomic already recorded"]
    G --> H["Financing Decision"]

    H --> I["Service Follow-up Plan<br><br>If AT repair = yes → select relevant service category with Adjustment or/and Repair as service<br><br>(Automatic closure of Episode of service)"]

    I --> J["Appointment for follow-up or new service"]

    %% Styling
    classDef default fill:#f0f0f0,stroke:#333,stroke-width:1.5px;

```



### SIMPLIFIED WORKFLOW FOR WALKING AND ADL

#### Initial decision after registration

<figure><img src="../../../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure>

If you need to deliver only one walking aid and/or ADL;

<figure><img src="../../../.gitbook/assets/image (302).png" alt=""><figcaption></figcaption></figure>

if you select new service, two options are display;

<figure><img src="../../../.gitbook/assets/image (303).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (304).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (305).png" alt=""><figcaption></figcaption></figure>



{% hint style="info" %}
As you need to enter the conditions of the HSU who will receive the walking aid only, the initial assessment must bee done.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (307).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (306).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../../.gitbook/assets/image (308).png" alt=""><figcaption></figcaption></figure>

