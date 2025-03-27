---
description: >-
  The page provides instructions on managing product variants, particularly
  addressing how to handle combinations of attributes and values that are not
  feasible or available.
---

# Creating a product with variants

## Setting up a product with only one attribute

When a product has some attributes that will define it as differences while preserving the main data in one place, we will use variants.\
We will start with simple example:&#x20;

<figure><img src="../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

* 1\. Reference prefix / t
* 2\. Variant reference mask - when a product has variants we setup code prefix and reference mask to create final product code ( reference) by adding a part of code describing the variant\
  by setting the attribute name in brackets the code for each variant will be created automaticly. NOTE: the variant name needs to be exact match otherwise the system will raise an error!
* 3\. the number of variants is defined by the number of attributes and attribute values

<figure><img src="../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

In this example, the product has only one attribute ( Bandage width ) with 5 possible values - defining 5 possible variants.

<figure><img src="../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

Note the Internal reference of each product is generated according to Variant reference mask.

{% hint style="danger" %}
**Warning:** If your product has only one attribute with a single value, create it without variants to avoid unnecessary complexity and ensure a straightforward customer experience.
{% endhint %}

## Setting up a product with multiple attributes and values

When a product is defined with more than one attribute it will create a Cartesian product of attribute values as a final number of variants.

Here is two example : \
In this example 2 sides x 2 sizes will create 4 variants.

![](<../../.gitbook/assets/image (123).png>) <img src="../../.gitbook/assets/image (122).png" alt="" data-size="original">



In this example there is 3 attributes , and total number of variants is 24

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
For attributes color and foot size - there is more possible values , but only the selected values will define this product, (other products may have more foot size values)
{% endhint %}

## Handling special cases

In some special cases, when we have more attributes applied with multiple attribute values, some combinations are not possible/available.

For example EVA FOAM come in different sheet dimensions and thicknesses, but\
3mm and 6mm thick sheets only comes in 0.95m x 0.95m, while 12mm thick only comes in 1.10m x 1.10m\
![](<../../.gitbook/assets/image (125).png>)\
\
To do that we need to follow these steps :\
1\. Click on the "Variants" button, to see all the possible variants and check the impossible one \
2\. Then go to "Action" > "Archive" :

<figure><img src="../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

So finally, we have only the possible variants visible in the system

<figure><img src="../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>
