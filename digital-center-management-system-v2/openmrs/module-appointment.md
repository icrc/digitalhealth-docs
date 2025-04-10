---
description: Configuration and providing appointment
---

# MODULE APPOINTMENT

The Physical Rehabilitation Centres offer multiple services to Health Service User (HSU). These services may have defined days and times when they are offered. For example Casting run every Monday 10.00 AM- 12.00PM . Appointments are the means by which providers tend to manage their resources and time to offer services to a HSU.&#x20;

Appointment scheduling feature is intended to provide the users the ability to schedule and manage appointments for HSU in a typical ICRC Program set up. With the help of this feature one will be able to:

1. Set up services for a program
2. Create and manage appointments for an HSU

Appointment feature can be used by any users within the Physical Rehabilitation Program and the level of access is defined based on the below set of privileges:

&#x20;1\. Manage Everyone Appointments: Create, Edit and Delete appointments for everyone

2\. Manage Own Appointments: Create, Edit and Delete appointments only for self

3: Manage Appointment Services: Create, Edit and Delete Services (This is to add new service types or make changes to service types in appointments)

{% hint style="info" %}
Receptionist has Manage Everyone Appointments - So receptionist should be able to schedule, modify appointments with all providers
{% endhint %}

{% hint style="info" %}
Hospital Project Manager Program has all of the above privileges - so hospital project manager can create or modify any appointments and has the ability to create new services or modify the existing service.
{% endhint %}

<figure><img src="../.gitbook/assets/image (174).png" alt=""><figcaption><p>User journey and appointment </p></figcaption></figure>

### The management appointment

The Appointment scheduling Application is available on the Home page

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## Services and Service Type

### About the Feature <a href="#dicdlkkhsp6i" id="dicdlkkhsp6i"></a>

A service is that entity which is offered to a HSU by a provider. Users are expected to select a service when scheduling their appointment: Cast, Physiotherapy

### Used By <a href="#uygw4343bfn5" id="uygw4343bfn5"></a>

Typically creating/updating services and specialties are Admin activities. Users will privilege “Manage Appointment Services” will be able to create a new service or edit an existing service&#x20;

### How is it used?

Click on the Appointment Scheduling App on the Home page. Under the Admin tab of the app, the user will be able to define and edit services. Only some roles will have access to the ADMIN button.

<figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption><p>Landing page when selecting appointment</p></figcaption></figure>

### &#x20;**Adding a new Service**

* [ ] Click on the "Add new Service" button on the screen to access the Services Screen

<figure><img src="../.gitbook/assets/image (85).png" alt=""><figcaption><p>Landing page after clicking on Admin button</p></figcaption></figure>

The User would be required to provide the following details to create a new service:

* [ ] **Service Name**: Unique name for the service. Mandatory field
* [ ] **Initial Appointment Status**:&#x20;

With two options **Scheduled , Requested;**

* In case of Scheduled: Appointment with this initial status by default moves to scheduled state
* In case of Requested: Appointment with this initial status by default goes to request state and users have the option to accept or propose a new time. Once after the new time proposed, appointment by default goes to scheduled state

- [ ] **Description:** Describe the service

* Duration of service: Consultation time required to offer the service to a patient.
* Start Time & end time: The working hours for a service or availability of a service

{% hint style="info" %}
Example: If casting occurs between 9:00 AM and 11:00 AM, the start time is 9:00 AM and the end time is 11:
{% endhint %}

* [ ] **Max Load**: The maximum number of appointments that can be booked for the service within the specified availability (start and end times

{% hint style="info" %}
For example, the casting session can take a maximum of 10 HSU between 9.00 AM - 11.00 AM&#x20;
{% endhint %}

* [ ] **Location:** A default location where a service is expected to be offered to the HSUs.

{% hint style="info" %}
All locations marked as "appointment locations" in OPENMRS will be available in the drop-down to choose from.
{% endhint %}

* [ ] **Label Color:** The services can be assigned colors. On the calendar view, all the appointments booked for this service, will be displayed in this chosen color.

<figure><img src="../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
calendar view will have the color displayed (shown below are appointment with service types marked with Color)
{% endhint %}

For a service with label color, when appointment is scheduled for this service and viewed from calendar view will have the color displayed (shown below are appointment with service types marked with Color)

&#x20;![](<../.gitbook/assets/image (88).png>)

### Service Appointment Type:

Service appointment types are the further granular categories under a service. One service may have different type of appointment types under a service

{% hint style="info" %}
For example, Initial assessment, Follow-Up Consultation under Casting service
{% endhint %}

* **Duration**: Each of these types are associated with a particular duration. This will override the service duration
* S**ervice Appointment types** can also be deleted, by clicking on the cross button beside the Service appointment type. Service Availability&#x20;

1. One can either mention a global availability for a service as mentioned in point d above or could specify a more granular availability.
2. In case of no availability defined, by default service is available on all days of the week at all times. Multiple availability can be tied to one service.
3. Example of service availability:\
   Physiotherapy session is happening on Monday and Friday from 10 AM to 12 PM and Wednesday 2 PM to 4 PM. Then the user will have 2 availabilities defined:\
   For Monday & Friday; with a start and end time of 10 AM to 12 PM\
   For Wednesday; with a start and end time of 2 PM to 4 PM
4. Max load for that availability (day)\
   \

5.
   1. The max number of HSUs that can be scheduled for a service for a defined duration in the day i.e. limit to the no.of appointments that can be booked.
   2. This value will be displayed to the user when they are booking an appointment for the service.

The screenshot below shows the Service availability and the Service Appointment Types defined:

&#x20;

![](file:///C:/Users/A571885/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

&#x20;

1.
   1. S
