# Product category

Product categories play a crucial role in organizing and managing inventory effectively.

Product categories help determine how inventory is valued. Each category can be assigned a specific valuation method such as Standard Price or FIFO (First In, First Out), impacting how the cost of goods sold (COGS) and inventory valuation are calculated.

<div align="left"><figure><img src="../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure></div>

Product categories facilitate efficient logistics and organization. They allow products to be grouped based on similar characteristics, such as type, function, or usage. This grouping simplifies inventory searches, reporting, and ensures products are stored and managed logically.

Overall, product categories in Odoo are fundamental for structuring inventory management, optimizing logistics, facilitating accurate valuation, enabling detailed reporting, and automating workflows.

&#x20;

<figure><img src="../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

* 1\. Category name , required , do not use parent categ name it will be generated
* 2\. Parent category - select the apropriate parent category
* 3\. Routes - stock routes applied on this category, and all subcategories\
  Total routes is calculated based on all routes selected for this and all parent categories
* 4\. Force removal strategy - selectable per category, Usualy there will be
  * FIFO - First in First out
  * LIFO - Last In First Out
  * FEFO - First Expiry First Out (only if we use expiry dates)
* 5\. Negative Stock - in general it should not be used...
* 6\. Costing method determines ho cost of product is calculated and recorded for stock valuation purposes, available options are:
  * Standard price - price set on product is used for valuation
  * FIFO - First in First out - the valuation of stock is calculated in order of receipts of goods with appropiriate prices
  * AVCO - Average cost - Each receipt impacts the recalculation of average cost price
* 7\. Inventory valuation (trigger)\
  \- Manual - manualy (periodicaly trigger the stock (re)valuation calculation\
  \- Automated - each stock move creates automaticly the valuation layer calculation in real time
* 8\. Account properties - set them according to accounting needs, used to record valuation of stock moves in accounting
* 9\. OPTIONAL - if center uses language other than english, it is used to display Category name in english for easier support and data analyze
* 10\. - Check products in this category - WARNING - ONLY products in THIS category , not the child categories!!
* 11\. Puttaway rules - rarely used
