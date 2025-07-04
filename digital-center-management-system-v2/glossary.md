# Glossary

#### 🔧 MRP / Manufacturing Terminology

* **MRP (Manufacturing Resource Planning)**: A system used to plan and manage manufacturing processes including stock, production, and delivery.
* **BoM (Bill of Materials)**: A list of all parts, components, and materials required to manufacture a product.
* **Work Order**: A specific task in the manufacturing process. Each step (e.g., cutting, assembling) is usually one work order.
* **Manufacturing Order (MO)**: A complete production request that includes all steps and materials needed to make a finished product.
* **Work Center**: A physical place or set of machines where specific manufacturing steps occur.
* **Operation**: A step in the manufacturing process, often assigned to a work center (e.g., “First assembly”).
* **Production Order**: Synonym for Manufacturing Order in this context.

***

#### 🧑‍⚕️ Roles / Personnel

* **P\&O**: Prosthetics and Orthotics — staff responsible for creating medical devices for patients.
* **Benchworker**: A technician who physically builds the devices (prostheses, orthotics, etc.).
* **SU (Service User)**: The patient or person receiving the manufactured device.
* **Head of P\&O / Head of Clinician**: A supervisor role who can approve manufacturing steps.

***

#### 📦 Inventory / Stock Management

* **Stock Picking**: The action of selecting and moving products from one location to another in inventory.
* **Internal Transfer**: Moving stock within the same company (e.g., from main warehouse to workshop).
* **Recasting**: Rebuilding or modifying an existing device by reusing some components.
* **Backorder**: A follow-up order to deliver remaining items that couldn't be delivered initially.
* **Lot/Serial Number**: A unique identifier for a product, especially useful for traceability (e.g., which device was given to which patient).

***

#### 📋 System Actions / UI Concepts

* **Confirm**: Approving a step so it moves to the next stage (e.g., confirming an MRP order).
* **Validate**: Finalizing or approving a record in the system (e.g., stock move, manufacturing order).
* **Check Availability**: Verifying that products or materials exist in stock and can be reserved.
* **AutoFill**: Automatically filling in the quantity of components to use, based on availability.
* **"Is Recasting" Checkbox**: A flag used to mark that a stock move is for recasting purposes.
* **Draft Status**: Initial status where changes can be made; not finalized.

***

#### 🧭 Navigation / Modules in Odoo

* **Service User Management**: The part of the system where you manage patients (SUs).
* **Inventory Application**: The module that handles stock and warehouse operations.
* **Manufacturing Application**: The part of Odoo where manufacturing orders and processes are managed.
