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
journey
    title Service User Device Manufacturing & Delivery Journey

    section Identifying the Service User
      User logs into the system: 1
      User navigates to 'Service User Management': 2
      User searches and selects service user: 3

    section Configuring the Bill of Materials (BoM)
      User initiates BoM configuration: 2
      User defines product attributes (side, size, color): 3
      User proceeds to validation: 2

    section Validating the Bill of Materials (BoM)
      User confirms BoM configuration: 2
      Superior validation (if required): 1

    section Stock Allocation
      User transfers stock to workshop: 3

    section Manufacturing Process
      User initiates manufacturing order: 2
      User processes each work order step-by-step: 3
      Additional validation (if required): 1

    section Completing the Manufacturing Order
      User finalizes manufacturing process: 3

    section Delivering the Device to the Service User
      User navigates to service user form: 2
      User checks for open delivery: 2
      User completes delivery process: 3

```



<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

[^1]: Service User
