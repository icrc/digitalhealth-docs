# Materials request for Manufactured product

In this section, we will explain the flow of the Manufacturing Resource Planning (MRP) process in Odoo, specifically for handling a service user requests for medical devices such as prostheses, orthotic, crutches, wheelchairs, walking aids or other materials.

## Prerequisite

The process begins when a service user requests a specific device. This triggers a series of steps to ensure the requested item is properly configured, manufactured, and delivered.

## MRP Process Flow

{% stepper %}
{% step %}
### Identify the service user

Locate the service user in the "Service User Management" menu.
{% endstep %}

{% step %}
### [Create the Bill of Materials (BoM)](creating-the-bom-configuration.md)

Create a BoM configuration to define the product attributes (e.g., side, size, color).
{% endstep %}

{% step %}
### [Validate the Bill of Materials (BoM)](managing-mrp-order.md)

Confirm the configuration. In some cases, a superior’s validation is required to proceed with the manufacturing order.
{% endstep %}

{% step %}

{% endstep %}

{% step %}
### Manufacturing Process

* Start the manufacturing order.
* Process each work order step-by-step.
* In certain cases, an additional validation by another person may be required.
{% endstep %}

{% step %}
### Complete the manufacturing Order

Finalize the manufacturing process once all work orders are completed.
{% endstep %}

{% step %}
### Deliver the Device to the SU

* Go to the service user form.
* Check for an open delivery and complete the delivery process.
{% endstep %}
{% endstepper %}

## Flow chart

```mermaid
---
config:
  theme: mc
---
flowchart TD
 subgraph user1["P&O"]
        B@{ label: "Locate SU in 'Service User Management' Menu" }
        A["Identify the Service User"]
        C["Configure the Bill of Materials (BoM)"]
        D["Create BoM Configuration (Side, Size, Color)"]
        E["Validate the Bill of Materials (BoM)"]
  end
 subgraph user2["Head of P&O"]
        F["Validate the Manufacturing order"]
  end
 subgraph user3["P&O"]
        n2["Validate the Manufacturing order"]
  end
 subgraph Bencworker["Benchworker"]
        G2["Retrieve the Components from the stock"]
        H["Start Manufacturing Process"]
        I["Process Work Orders Step-by-Step"]
        K["Finalize Manufacturing Process"]
  end
    A --> B
    B --> C
    C --> D
    D --> E
    user1 --> n1(["Need a Superior Validation"])
    n1 -- Yes --> user2
    n1 -- No --> user3
    F --> G["Stock picking created"]
    G --> G2
    G2 --> H
    H --> I
    K --> L["Deliver the Device to SU"]
    L --> M["Go to Service User Form"]
    M --> N["Check for Open Delivery"]
    N --> O["Complete the Delivery Process"]
    user3 --> G
    I --> K
    B@{ shape: rect}

```

