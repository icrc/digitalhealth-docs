---
description: >-
  This chapter is about the journey of a HSU in a Physical Rehabilitation Centre
  and how the DCMS capture the data entry at the point of care.
---

# HSU Journey and Workflows



We have 2 main workflows&#x20;

1. New Service
2. Follow up/repair&#x20;

###

{% stepper %}
{% step %}
### (if necessary) Intermediate Assessment Outcome and Goal setting

Decision: Adjust service if required

Basic service plan

Financial capacity assessment (+Socioeconomic already recorded) and Financing decision&#x20;
{% endstep %}

{% step %}
**Service (s)**&#x20;
{% endstep %}

{% step %}
### Final assessment Outcome and goal setting (Automatic closure of service)

Appointment for follow up visit
{% endstep %}

{% step %}



{% endstep %}

{% step %}

{% endstep %}
{% endstepper %}

```mermaid
graph 

    A["Register the HSU or find the HSU file coming to the PRC"] --> B["Start the visit"]
    B --> C["Initial decision after registration and decision to send for new service (save and validate)"]
    C --> D["Initial Assessment (interdisciplinary team)"]
    D --> E["Initial outcome and goal setting + Basic service plan + clinical consent"]
    E --> F["Financial capacity assessment + Socioeconomic assessment + Financing decision"]
    F --> G["Any Services"]
    
    G --> G1["Technical cards"]
    G --> G2["Physiotherapy assessment"]
    G --> G3["Wheelchair assessment"]
    G --> G4["Walking Aids"]
    G --> G5["Club foot"]
    G --> G6["Cerebral palsy"]
    
    G6 --> H{"Intermediate Assessment and <br>Goal Setting (if needed)"}
    G5 --> H
    G4 --> H
    G3 --> H
    G2 --> H
    G1 --> H
    G --> H

    H -- Yes --> I["Adjust service if required + Basic service plan + Financial capacity assessment + Financing decision"]
    I --> J["Additional Services"]
    J --> K["Final assessment Outcome and goal setting + Automatic closure of service"]

    H -- No --> K
    K --> L["Appointment for follow-up visit"]

```

### &#x20;Workflow Follow up/Repair

<img src="../../../.gitbook/assets/file.excalidraw (2) (1).svg" alt="" class="gitbook-drawing">



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









*











