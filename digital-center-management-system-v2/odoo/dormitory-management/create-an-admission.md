# Create an admission

To create an admission for a Service User (SU), you can either start from the SU form or from the Admission list. Here's how the process works:

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

1. **Create an Admission:**
   * From the SU form or Admission list, initiate the admission process.
   * Based on the patient's gender, the system will automatically select an appropriate ward (e.g., for a female patient, the Women’s Area will be selected).

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. **Adding a Caregiver:**
   * If the SU has a caregiver, go to the second tab, labeled "SU Companion." Here, you can add caregivers.
   * Only caregivers previously created for this specific SU will be visible in this tab.
   * Each caregiver entry must be admitted separately, as the dates for each caregiver might differ.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Multiple Caregiver Entries:**

> It is possible to add the same caregiver multiple times with different dates (e.g., the caregiver may be present on different days).

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. **Plan the Admission:**
   * When the users data are populated, we need to set the start and end plan dates, and check availability of resources.\
     Note that admission state is Draft
   * Planing Dates can be entered with time value, (eg: plan discharge of bed @10:00 and next admission on same bed can be @14:00 after cleaning).
   * Plan Start and End dates can be entered as current, past or future
   * The objective of planing is to position the service user on a bed not occupied or reserved in that period.
4. You can modify admissions in states Draft (light blue color) or Plan (light green color) with all values
5. Admission in state Admitted (light red color) can oly be modified with Plan end date, nothing else is allowed.
6. With multiple options for planed/occupied/available beds, throughout wards and buildings, the timeline view is provided.\
   The rows represent all available beds, and the columns are dates and times.\
   Timeline navigation options:
   * In order to modify one admission first click on it once, and then
   * Move mouse to left or right border of admission line until mouse icon changes to that side arrow, then click and drag to respectfuly moodify start or end date
   * Move the mouse more to middle of admission line (mouse icon looks like hand) then, click and drag the whole admission ove times and/or beds\
     \- left/right moves the start and end values of admission\
     \- up/down changes selected bed for admission
   * To move trough the timeline, click on grey background to move over beds or periods\
     \- left/right moves the timeline\
     \- up/down scrols trough beds ( in case you have more than can fit to screen)
   * Ctrl + Mouse wheel : Time line zoom in / zoom out - increase or decrease time scope
   * Click on bed name (right rows names) will show you state and occupancy for selected bed
7. To visualise and plan admissions, click on Manage overlaping button to open timeline plan view

<div align="center" data-full-width="false"><figure><img src="../../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure></div>

8. Activating the Admission:
   * Once the admission is planned, click the "Activate" button at the top of the main admission record.
   * Also, select the small checkbox on the corresponding SU Companion Line for each caregiver.

<figure><img src="../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

* Plan Start and End dates can be entered as current, past or future.\
  Depending on those dates different behaviour of button will be:
*
  * Both dates are in past: the SU admission will be activated, admitted and discharged with planned dates.\
    Admission will end in state Discharged
  * Start date is in past, release date is in future: the SU will be admitted, the bed shown as occupied,\
    Admission will be in state Admitted
  * Both dates are in future: The selected bed will be shown as Planned (or reserved) for SU,\
    Admission will be in state Planned

8. Status Update:
   * After activation, the status of the admission record will change to "Plan" for both the main admission and the caregiver(s).

This process ensures that both the SU and their caregiver(s) are properly admitted with accurate tracking of dates and status.
