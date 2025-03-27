# Create the Repair order

In Odoo, there are multiple ways to create a new repair order. You can either go to a Service User (SU) and click on the "New Repair Order" button

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

The second way will be to navigate to the "Repair" module, open "Repair Orders," and click "Create."

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

If you select a Service User who has no manufactured products, a pop-up will appear warning that no items belong to this SU. In this case, return to the previous step, “Get the product to repair.”

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

Otherwise, after selecting the partner, the system will automatically identify the product received for repair, and you will be directed to the repair order form.

The form contains two tabs:

* Component Tab: This tab lists all the products that will be removed or added to a specific prosthesis. When adding a line, you can choose to add or remove a product. If a product is added, it will be deducted from stock, triggering a transfer. If "Suppress" is selected, you can modify the destination location to either return the product to stock or move it to the scrap location.

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

* Operation Tab: This tab includes all service products required during the repair. It is mainly used for invoicing specific services, such as labor or materials, to the patient.

Once everything is set up, the next step is to confirm the repair by clicking on "Confirm Repair.".
