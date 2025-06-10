---
description: /
---

# Odoo

<details>

<summary>Wrong attribute or Product not found in BoM Config</summary>

To solve this problem, first close the message and click on "ReConfigure". In a scenario where, for instance, the Foot Sach 2.0 in "Beige" is not available

<img src="../../.gitbook/assets/image (12) (1).png" alt="Attributes for the foot SACH 2.0" data-size="original">

You have two options: either change the BoM's color selection to an available option or update the product variant to include the "Beige" color if it's applicable.

</details>

<details>

<summary>No access to user form</summary>

When doing backup of database,  attachement is being deleted or modified.

To resolve this issue you need to go to “Config” > Attachement. Then select all and delete it.

It will solve the error, you can regenerate assets bundle if you want but it’s not necessary.

</details>

<details>

<summary>Issues with stock picking </summary>

The product are in the right stock but can’t be reserved :

A product is missing in the move

The wrong lot number as been selected :

System will prevent to have negative value.

</details>

<details>

<summary>No rules found to replenish a product</summary>

Error : ![](<../../.gitbook/assets/image (13) (1).png>)

Check on the product if there is the “Replenish On Order(MTO)”

![](<../../.gitbook/assets/image (14) (1).png>)

</details>

<details>

<summary>Insufficient Quantity on repair</summary>

![](<../../.gitbook/assets/image (15) (1).png>)

Multiple reason possible :

* The product to repair was removed from the repair stock
* The product used in the repair was not send or is not in stock please check with your stockmanager



</details>

<details>

<summary>There is too many product on repair stock</summary>

If when checking the repair location you see such prothesis that means that some of the repaired prothesis was either not delivered back or not yet repaired.

</details>

