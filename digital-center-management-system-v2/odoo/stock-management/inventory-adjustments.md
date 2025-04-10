# Inventory adjustments

To manage inventory in Odoo, you can create an inventory adjustment. Start by navigating to "Inventory" > "Operations" > "Inventory Adjustments".

<figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

&#x20;From there, create a new record and select the location you want to update. Typically, this will be either "WH/Stock" (main stock) or the "WH/Workshop" (workshop location).

If you want to include all products, even those with zero stock, make sure to check the "Include exhausted products" field.&#x20;

<figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

Next, click on "Start Inventory". This will allow you to update each product line with the actual stock value. If a product is not listed, you can click on the "Create" button to add a new line.

As you update the quantities, any lines with discrepancies between the counted stock and the stock on hand will be highlighted in red. Once all quantities are accurate, you can proceed by clicking on "Validate Inventory". This action will lock the inventory and update the stock based on the inventory adjustment.

<figure><img src="../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>
