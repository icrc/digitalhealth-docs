---
description: >-
  This chapter is about the appointment module and how to provide allocated
  times for the Health Service User. It reflects the user journey within the
  rehabilitation cyce.
---

# MODULE APPOINTMENT

Configuration and providing appointment

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

<figure><img src="../.gitbook/assets/image (174).png" alt=""><figcaption><p>User journey and appointment </p></figcaption></figure>

### The management appointment

The Appointment scheduling Application is available on the Home page

<figure><img src="../.gitbook/assets/image (3) (2).png" alt=""><figcaption></figcaption></figure>

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
   Physiotherapy session is happening on Monday and Friday from 10 AM to 12 PM and Wednesday 2 PM to 4 PM. Then the user will have 2 availability defined:\
   For Monday & Friday; with a start and end time of 10 AM to 12 PM\
   For Wednesday; with a start and end time of 2 PM to 4 PM
4. Max load for that availability (day)\
   a. The max number of HSUs that can be scheduled for a service for a defined duration in the day i.e. limit to the no.of appointments that can be booked.

&#x20;     b. This value will be displayed to the user when they are booking an appointment for the service.

The screenshot below shows the Service availabilities and the Service Appointment Types defined:

\
![](<../.gitbook/assets/image (176).png>)

### &#x20;Creating and Managing Appointments

#### How is it Used?![](file:///C:/Users/A571885/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)

&#x20;Click on the Appointment Scheduling App on the Home page. Under the "Manage Appointments" tab of the app, click on Appointments List tab.

#### Create Appointments

1. Click on the "Add new Appointment" on the Appointments list Tab

<figure><img src="../.gitbook/assets/image (179).png" alt=""><figcaption><p>Add new appointment </p></figcaption></figure>



2. The user will have to fill the details of the appointment in the Add new Appointment slider

<figure><img src="../.gitbook/assets/image (178).png" alt=""><figcaption><p>Appointment page </p></figcaption></figure>



The following details are required to create an appointment:

{% hint style="info" %}
Selecting a HSU, Service/service type and Date is mandatory to create an appointment.
{% endhint %}

* HSU: The HSU can be searched for using HSU name or ID
* Service: The service is selected from the drop down. This will further filter the appointment types under it.
* Service Appointment Type: The service appointment type will be selected from a drop down.
* Walk-in Appointment: Users can mark an appointment as a walk-in. By default, appointments are marked as Scheduled.
* Date of Appointment: This will be chosen from a date picker. Only current and future dates are allowed.&#x20;
* Time slot: Select the time slot for an appointment.

The drop down will suggest possible slot times based on service availability.

End time will auto populate based on the duration of the service/ service appointment type. Default of 30 mins if no duration are mentioned.



Users can override the suggested times.

<figure><img src="../.gitbook/assets/image (180).png" alt=""><figcaption><p>Information showing the times for the appointment is not available</p></figcaption></figure>

Providers: Select the provider for the appointment from the drop down. Only those providers with provider attribute Available for appointments set to true will be shown. This setting is available in OpenMRS>Administration>Providers>Manage Providers

<figure><img src="../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

·         Location:  By default the location will be Service location. User can change the location as applicable.

**Warnings to the user**

·         If service availability is defined, if the user chooses a day or timings outside the availability, there will be a warning to the user.

·         Booking a patient simultaneously in overlapping times will warn the user of the conflict.

·         In both cases mentioned above, the user can still go ahead and book an appointment by ignoring the warning

&#x20;

&#x20;![](<../.gitbook/assets/image (182).png>)

Screenshot below showcasing the warning message when scheduling an appointment outside of the slot availability time.



### Manage Appointments

#### Edit Appointments

1. Click on the appointment that you want to edit.
2. Click on the edit button on the Button below

&#x20;

<figure><img src="../.gitbook/assets/image (188).png" alt=""><figcaption><p>Calendar view</p></figcaption></figure>

3. In case of scheduled appointment when user selects Edit, then appointment opens as shown below, where user have the option to edit Location, Provider and the Date/time of the appointment.

<figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

4. In case of past appointments or appointments that have been marked as Missed/Canceled/Completed, only Notes field can be edited.

### Accept Appointments

In case of appointment status as Requested - User will be able to accpet the appointment and doing so will change the appointment status to accepted.

Or user can Edit the appointment and propose the new time and once done an appointment by default will have the status accepted.

&#x20;

<figure><img src="../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

### Status of Appointment

**Appointments can be marked as Checked-in, Cancelled, Missed or Complete.**

* Check -in - Will mark the appointment status as Checked -In
* Complete - Will mark the appointment status as completed
* Cancel - Will mark the appointment as cancelled. Once marked as cancelled appointment gets removed from the calendar
* Missed - Will mark the appointment as Missed as shown below

<figure><img src="../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>





