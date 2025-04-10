# Picking (Opertation) types

On Inventory overview you can see multiple different types of pickings.\
Picking types define the predefined moves of a product or a group of products in stock management.\
There is a few main types:

* Receipts - in general items that arrive to our stock location from vendors or customers
* Deliveries - in general when items are delivered to customer
* Internal moves - any kind of moving goods within our warehouse from one location to the other (Stock to workshop, Stock to Repair location ...)
* Manufacturing - when we produce new items and consume some components
* Repair - when we repair an already produced items and consume some components

Further more, picking types can be configured to ease the stock management,&#x20;

<figure><img src="../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

* 1\. name the operation type according to needs
* 2\. Type of operation: select between: Receipt, Delivery, Internal transfer, Manufacturing\
  if needed, specific operatin type for returns can be set,
* 3\. select sequence for numbering of pickings or set the code prefix for sequence
* 4\. set if we need to create new lots/serial numbers or use existing ones for this picking (usualy we create then on receipt, or in manufacturing, and just use existing in all other pickings)
* 5\. automation - should the system automaticly fill the operations and lot/serials or let the user select them manualy
* 6\. set default source and target locations for certain moves helps in speedup the process
