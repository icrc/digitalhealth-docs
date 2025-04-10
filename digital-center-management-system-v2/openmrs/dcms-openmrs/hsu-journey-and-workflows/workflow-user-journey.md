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
    E1 --> F["Financial capacity assessment + socio-economic assessment (completed with financing decision if financial capacity is not approved)"]
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


{% endstep %}

{% step %}
### Financial Capacity Assessment&#x20;

if not approved:

* Select make **socio-economic** and complete **FInancing Decision**
* Select **Socio-economic** already recorded, if you select this option you can already go to F**inancing Decisio**n
{% endstep %}

{% step %}
### Service (s)
{% endstep %}

{% step %}
### Final assessment Outcome and goal setting (Automatic closure of service)

Appointment for follow up visit
{% endstep %}
{% endstepper %}
