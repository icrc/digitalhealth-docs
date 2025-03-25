---
description: Configuration and providing appointment
---

# MODULE APPOINTMENT



The Physical Rehabilitation Centres offer multiple services to Health Service Users (HSU). These services may have defined days and times when they are offered. For e.g Casting runs every Monday 10.00 AM - 12.00 PM. Further, we have providers in the hospital who provide these specific services to HSU. Appointments are the means by which providers tend to manage their resources and time to offer services to a HSU.

Appointment scheduling feature is intended to provide the users the ability to schedule and manage appointments for HSU in a typical ICRC Program set up. With the help of this feature one will be able to:

1. Set up services for a program
2. Create and manage appointments for an HSU

### Used By

Appointment feature can be used by any users within the Physical Rehabilitation Program and the level of access is defined based on the below set of privileges:

&#x20;1\. Manage Everyone Appointments: Create, Edit and Delete appointments for everyone

2\. Manage Own Appointments: Create, Edit and Delete appointments only for self

3: Manage Appointment Services: Create, Edit and Delete Services (This is to add new service types or make changes to service types in appointments)

Ex:

Receptionist has Manage Everyone Appointments - So receptionist should be able to schedule, modify appointments with all providers

&#x20;Hospital Project Manager Program has all of the above privileges - so hospital project manager can create or modify any appointments and has the ability to create new services or modify the existing services

### How is it used?

The Appointment scheduling App is available on the Home page

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



## Services and Service Type

### About the Feature <a href="#dicdlkkhsp6i" id="dicdlkkhsp6i"></a>

A service is that entity which is offered to a HSU by a provider. Users are expected to select a service when scheduling their appointment: Cast, Physiotherapy

### Used By <a href="#uygw4343bfn5" id="uygw4343bfn5"></a>

Typically creating/updating services and specialties are Admin activities. Users will privilege “Manage Appointment Services” will be able to create a new service or edit an existing service&#x20;

### How is it used?

Click on the Appointment Scheduling App on the Home page. Under the Admin tab of the app, the user will be able to define and edit services.

&#x20;**Adding a new Service**

1\. Click on the "Add new Service" button on the screen to access the Services Screen

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



The User would be required to provide the following details to create a new service:

* Name: Unique name for the service. Mandatory field
* Initial Appointment Status:&#x20;

To have options **Scheduled , Requested;**

1. In case of Scheduled: Appointment with this initial status by default moves to scheduled state
2. In case of Requested: Appointment with this initial status by default goes to request state and users have the option to accept or propose a new time. Once after the new time proposed, appointment by default goes to scheduled state



* Description: Describe the service

1. Duration of service: Consultation time required to offer the service to a patient.
2. Start Time & end time: The working hours for a service or availability of a service



1. For example, if the casting happens from 9.00 AM to 11.00 AM, then start time would be 9.00 AM and end time would be 11.00 AM
2. Max Load: This is the indicative maximum no. of appointments that can be booked for a service, for a given availability (start and end time mentioned above)
3.
   1. For example, the casting session can take a maximum of 10 HSU between 9.00 AM - 11.00 AM&#x20;
4. Location: A default location where a service is expected to be offered to the HSUs.
5.
   1. All locations marked as "appointment locations" in openMRS will be available in the dropdown to choose from
6. Label Color: The services can be assigned colors. On the calendar view, all the appointments booked for this service, will be displayed in this chosen color.
7.
   1. For a service with label color, when appointment is scheduled for this service and viewed from calendar view will have the color displayed (shown below are appointment with service types marked with Color)

&#x20;

Initial Appointment Status: To have options Scheduled , Requested.

*



1. In case of Scheduled: Appointment with this initial status by default moves to scheduled state
2. In case of Requested: Appointment with this initial status by default goes to request state and users have the option to accept or propose a new time. Once after the new time proposed, appointment by default goes to scheduled state
3. Description: Describe the service
4. Duration of service: Consultation time required to offer the service to a patient.
5. Start Time & end time: The working hours for a service or availability of a service
6.
   1. For example, if the casting happens from 9.00 AM to 11.00 AM, then start time would be 9.00 AM and end time would be 11.00 AM
7. Max Load: This is the indicative maximum no. of appointments that can be booked for a service, for a given availability (start and end time mentioned above)
8.
   1. For example, the casting session can take a maximum of 10 HSU between 9.00 AM - 11.00 AM&#x20;
9. Location: A default location where a service is expected to be offered to the HSUs.
10.
    1. All locations marked as "appointment locations" in openMRS will be available in the dropdown to choose from
11. Label Color: The services can be assigned colors. On the calendar view, all the appointments booked for this service, will be displayed in this chosen color.
12.
    1. For a service with label color, when appointment is scheduled for this service and viewed from calendar view will have the color displayed (shown below are appointment with service types marked with Color)

&#x20;
