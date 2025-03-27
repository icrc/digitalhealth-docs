# Materials request (MRP)

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
### Configure the Bill of Materials (BoM)

Create a BoM configuration to define the product attributes (e.g., side, size, color).
{% endstep %}

{% step %}
### Validate the Bill of Materials (BoM)

Confirm the configuration. In some cases, a superior’s validation is required to proceed with the manufacturing order.
{% endstep %}

{% step %}
### Stock Allocation

Retrieve the necessary components by moving stock from daily usage inventory to the workshop.
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
### Deliver the Device to the SU[^1]

* Go to the service user form.
* Check for an open delivery and complete the delivery process.
{% endstep %}
{% endstepper %}

## Flow chart

```mermaid
---
config:
  theme: mc
look: neo
---
graph TD;
    subgraph user1 ["P&O"]
    A["P&O: Identify the Service User"] --> B["P&O: Locate SU in 'Service User Management' Menu"];
    B --> C["Configure the Bill of Materials (BoM)"];
    C --> D["Create BoM Configuration (Side, Size, Color)"];
    end 
    subgraph user2 ["Head of P&O"]
    E["P&O: Validate the Bill of Materials (BoM)"];
    E -->|If Required| F["P&O: Need of Superior Validation"];
    end
    user1 --> user2
    
    E -->|Else| G["Stock picking created"];
    F --> G;
    G --> G2["Retrieve the Components from the stock"]
    G2 --> H["Benchworker: Start Manufacturing Process"];
    H --> I["Benchworker: Process Work Orders Step-by-Step"];
    I -->|If Required| J["Benchworker: Additional Validation by Another Person"];
    I -->|Else| K["Benchworker: Complete Manufacturing Order"];
    J --> K;
    K["Benchworker: Finalize Manufacturing Process"] --> L["Benchworker: Deliver the Device to SU"];
    L --> M["Benchworker: Go to Service User Form"];
    M --> N["Benchworker: Check for Open Delivery"];
    N --> O["Benchworker: Complete the Delivery Process"];
```





<img src="../../.gitbook/assets/file.excalidraw.svg" alt="" class="gitbook-drawing">



<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

[^1]: Service User
