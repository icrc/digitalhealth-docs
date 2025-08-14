# Create an admission

{% hint style="info" %}
Roles recommended : Dormitory manager
{% endhint %}

## **🧭** Context: <a href="#context" id="context"></a>

Creating an admission for a Service User (SU) is a crucial administrative step that ensures proper coordination of accommodations and services. Each admission represents a defined period during which the SU is expected to stay in the facility. It allows staff to assign a bed, monitor presence, and manage logistics such as caregiver stays, meal planning, and room availability. This process also supports reporting and tracking, ensuring transparency and accountability in dormitory usage. Admissions must be created accurately to reflect the real-world presence of the SU and their companions.

## 🔄 Step-by-Step Flow

### Creation of the admission

To create an admission for a Service User (SU), you can either start from the SU form or from the Admission list.

{% tabs %}
{% tab title="Via the SU form" %}
On the home page, go to the icon "Service User Management".

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

You can view a list of all SU[^1]s here. Use the search bar at the top to find a patient by their name or SU[^1] ID. Please ensure to select the correct option.

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Inside the Service User (SU) form, you’ll find a button labeled **"Create admission"**. Clicking this button will trigger the creation of the admission request.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Via the Admission list" %}


On the home page, go to the icon "Service User Management".

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

At the top of the screen, in the header, you’ll find a menu labeled **“Admissions”** Click on it to open the Admission section, then click on **“Create New Admission”** to start a new admission process for a service user.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}



Now that the admission is created we need to fill in the information, first check/fill the service user field to ensure that you have selected the correct Service user.

Based on the patient's gender, the system will automatically select an appropriate ward (e.g., for a female patient, the Women’s Area will be selected).

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### **Adding a Caregiver**

the Service User (SU) has a caregiver, go to the second tab labeled **"SU Companion."** In this tab, you can add admission records for caregivers and specify the dates they will be present. Each caregiver must be admitted individually, as their availability may vary.

{% hint style="info" %}
Only caregivers previously created for this specific SU will be visible in this tab.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

You can also add the same caregiver multiple times with different dates if they are present on different occasions.

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 🗺️ Visual Overview&#x20;

```mermaid
graph LR
  A[Access the service user form] -->  C[Create the admission] 
  B[From the menu Admission] --> C
  C --> D[Create admission for caregiver]
   
```

## What's next?&#x20;



[^1]: Service provider
