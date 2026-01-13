---
description: How to use our mobile device management service and strategies.
---

# \[WIP] Guide to Mobile Device Management for the field

This guide explains the core concepts, decisions, and strategies behind our MDM (Mobile Device Management) setup, and how Applivery is used to reliably deploy, update, and control mobile applications across a device fleet.

Applivery is the Mobile Device Management (MDM) platform we use to manage mobile devices deployed in the field.

> You may be familiar with other Mobile Device Management solutions used at ICRC (such as Workspace ONE, as of early 2026).
>
> We use a separate service — Applivery — because our operational model requires the ability to **transfer ownership and responsibility of managed device fleets to local partners** once an engagement or project comes to an end, something not possible with our internal solution.

## Why Mobile Device Management?

Field deployments require strong control over both **applications** and, in some cases, the **devices themselves**. Without MDM, ensuring consistency, security, and operational reliability at scale quickly becomes unmanageable.

MDM allows us to:

### Control the application lifecycle

* Ensure the latest version of an application is installed.
* Deliver apps directly to devices with minimal user interaction (auto-install or fast install).
* Remove obsolete or deprecated applications remotely.

### Enforce security and compliance on managed devices

* Allow-list approved public apps (e.g. WhatsApp, authenticator apps).
* Block all other unapproved applications.
* Restrict or enforce specific device capabilities to ensure professional use.

In practice, Applivery lets us define **Policies** that act as reusable templates. These policies standardize device behavior and give us centralized control over application deployment and device configuration across an entire fleet.

### Device Ownership Models

Before deploying an application, the first decision is always the same:

**Are users provided with ICRC devices, or are they using their own?**

This determines the management model.

### Fully Managed Devices

* Owned and provided by ICRC.
* Dedicated exclusively to professional use.
* Can be factory-reset, remotely configured, and tightly controlled.
* Full device policies apply (apps, settings, restrictions).

### BYOD (Bring Your Own Device)

* Personally owned devices.
* Management must remain non-intrusive.
* Applications are deployed inside a **Work Profile**, isolated from personal data.
* Only professional apps and policies are managed.

Choosing the correct model is foundational: it defines which policies can be applied, how intrusive management can be, and what level of security enforcement is acceptable.

<figure><img src=".gitbook/assets/Screenshot 2026-01-06 at 15.45.40.jpg" alt=""><figcaption></figcaption></figure>

**How to read this diagram**

* Devices are enrolled into Applivery.
* During Enrollment, the ownership model is determined:
  * Fully Managed.
  * BYOD (Work Profile).
* The ownership model defines which Policies can be applied.
* Policies control:
  * Device configuration.
  * Security restrictions.
  * Application deployment.
* Applications are pushed, updated, or removed automatically.
* Users interact only with the managed applications, not the MDM itself.

## Common Operations

This section describes the most common day-to-day operations performed in Applivery.

> Note: we only work with Android devices.

### 1. Login

Access to Applivery requires an existing account with sufficient permissions.

#### Prerequisites

* You must have **Workspace Admin** permissions.
* These permissions must be granted by an existing Workspace Admin.

Without this permission level, you will not be able to create policies, manage apps, or configure devices.

Next up we review **Policies**. They are framework of settings and rules presiding over application deployments to devices. When you plan to deploy one or more applications for a specific project/area, you define a dedicated policy, re-use an existing one, or even duplicate an existing one that you slightly tweak for the new deployment.&#x20;

> ⚠️ **Important**\
> Policies are used for Fully Managed or BYOD fleets alike — it is both best practice and a technical necessity to create two different policies for the same deployment if this deployment enrolls using both models.

This guide presents the **creation of Policies** (below).&#x20;

### 2. Creating a Policy

#### Step 1 — Create the policy

1. From the main menu, go to: **Device Management → Policies**
2. Click **Create Policy**.
3. In the creation modal:
   * Platform: **Android**
   * Name: **\<APP NAME> Fully Managed** or **\<APP NAME> BYOD** (e.g. ALMANACH Fully Managed), depending on your intent.
   * Policy type: **Empty policy**
4. Click **Create**.

You are now on the policy configuration page.

#### Step 2 — Add public apps (Google Play)

1. In the left menu, select **Apps**.
2. Click **Add App**.
3. The Google Play modal opens.
4. Search for the public app you want to include\
   (e.g. _Google Authenticator_).
5. Click **Approve**.
6.  If prompted about permission handling updates:

    * Choose the **“Revoke...”** option

    ![](<.gitbook/assets/Screenshot 2026-01-06 at 16.07.13.jpg>)
7. Validate each step until the modal closes.

Repeat this process for **each public app** you want bundled into the policy.

#### Step 3 — Add private (ICRC) applications

1. In the left menu, select **Apps**.
2. Click **Add App**.
3. In the left submenu of the modal, choose **Private Apps**.

**Case A — The app already exists**

* Select the ICRC application from the list.
* Validate until the modal closes.

**Case B — The app is not present**

1. Click the **“+”** button (bottom-right of the modal).
2. Upload the application binary provided by the engineering team.
3. Set the application name using the convention: **\<App Name> \<Env>** (e.g. ALMANACH Prod).
4. Validate all steps until the modal closes and the app appears in the policy.

#### Step 4 — Save the policy

* Click **Save changes** (top-left of the screen).\
  ![](<.gitbook/assets/Screenshot 2026-01-06 at 16.12.13.jpg>)

> ⚠️ **Important**\
> Changes are not applied until the policy is explicitly saved.

***

#### Result

You now have:

* An Android policy,
* To be used in a Fully Managed or BYOD devices,
* With approved public applications,
* And one or more private ICRC applications,
* Ready to be assigned to devices during enrollment.

### 3. Enrolling Devices

Device enrollment is the process that links a physical device to Applivery, applies a policy, and makes the device manageable.

#### Step 1 — Start an enrollment

1. From the top menu, go to: **Device Management → Devices**
2. Click **Enroll Device** (or **Enroll Multiple Devices** from the button submenu).

#### Step 2 — Configure the enrollment

In the enrollment modal:

**Enrollment type**

* Choose one:
  * **Fully Managed**
  * **Work Profile (BYOD)**
  * If **Fully Managed** is selected, leave the option below the enrollment type dropdown as default.

**Employee**

* Select an **Employee** from the list.
* This is primarily for organisational and communication purposes. Ideally, this should be:
  * The field contact responsible for overseeing deployment with local helpers.
  * If no suitable Employee exists yet, you may assign the enrollment to yourself.

> The selected Employee will receive system emails related to the enrollment\
> (e.g. deployment instructions or enrollment codes).

**Policy**

* Click **Add policy**.
* Select the policy you created or selected previously.

**Additional options**

1. Click **More options** to reveal additional fields.
2. Fill in:

* **Tags**\
  Add tags according to your organisational or project needs.
*   **Display name**\
    Use a clear, meaningful naming convention:

    ```
    <Project> <Enrollment Type> <ID>
    ```

    Example:

    ```
    Somalia BYOD Device 01
    ```
* Check **Send instruction email to employee**.

3. Click **Create enrollment**.

#### Step 3 — Confirm enrollment instructions

You will be shown the screen: **Enrollment instructions for Android \<enrollment type>.**

* You do **not** need to change anything on this screen.
* Review the instructions for your own understanding.
* Click **Confirm Enrollment**.

The enrollment status will now show as **Pending**.

Use the back arrow at the top of the screen to return to the Devices list (if you are not redirected automatically).

#### Step 4 — Share enrollment instructions

Back on the **Devices** screen:

* The enrollment appears as an entry in the Devices table.
* Clicking it allows you to view the instructions again.

⚠️ **Important**

* The person performing the enrollment on the physical device needs the **QR code** from these instructions. **Consider the QR code shown as uniquer, per enrollment/device.**
* Even if the assigned Employee receives the instructions by email, we **strongly recommend** sharing them directly yourself (e.g. via email or secure messaging).

#### Step 5 — Complete enrollment on the device

* Once the enrollment is completed on the physical device:
  * The enrollment entry automatically becomes a **Device** entry.
  * Device-specific information (model, OS, identifiers) appears.
* This confirms the enrollment was successful.

#### Operational guidance

* Prepare **one enrollment per device**.
* Share the corresponding instructions individually for each device.
* **Do not reuse enrollment instructions across devices — it shows one QR code → specific per-device.**
* If your field contact is responsible for the enrollment of devices, we suggest you do an first couple of enrollment with them directly (via videoconference).

### 4. Updating policies

Any change made to a policy — whether it concerns device configuration or applications — only takes effect once the policy is explicitly saved.

This applies to:

* Adding, removing, or updating applications
* Changing Fully Managed device settings
* Modifying restrictions or configuration options

#### Important rule

> **A policy is not updated until the “Save Policy” button is clicked. It's easy to miss: it is on the  upper-left side of the screen.**

If changes are not saved, they will **not** be propagated to devices.

#### How policy updates are applied

Once the policy is saved:

* The policy version is incremented.
* All devices currently equipped with this policy automatically receive the update.
* Updates are applied silently in the background.

#### How to verify that devices received the update

1. Go to: **Device Management → Devices**
2. In the Devices table:
   * Check the **Last update** column. It should show a very recent timestamp.
3. In the **Policies** column:
   * Hover over the policy name in the device row.&#x20;
   * A cogwheel icon is displayed with a number next to it.&#x20;
   * This number corresponds to the **policy version currently running on the device**.
   * Verify that this version number matches your most recent policy update.

#### Troubleshooting delayed or missing updates

If a device does not reflect the policy update:

1. Ensure the device is:
   * Powered on
   * Connected to the internet (Wi-Fi or mobile data)
   * Left online long enough for the update to be applied
2. If the update still does not appear:
   * Contact the field focal point.
   * Walk them through the following steps:
     1. Plug the device into a power source.
     2. Verify active internet connectivity.
     3. Perform a **simple device restart.**

In most cases, policy updates are applied shortly after connectivity is restored.

#### Operational guidance

* Always save the policy after making changes.
* Always verify policy version propagation on at least one device.
* Avoid making multiple successive changes without validation in between.
