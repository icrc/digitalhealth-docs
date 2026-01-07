---
description: How to use our mobile device management service and strategies.
---

# \[WIP] Mobile Device Management for the field: the Applivery guide

Applivery is the Mobile Device Management (MDM) platform we use to manage mobile devices deployed in the field.

This guide explains the core concepts, decisions, and strategies behind our MDM setup, and how Applivery is used to reliably deploy, update, and control mobile applications across a device fleet.

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

### Result

You now have:

* An Android policy,
* To be used in a Fully Managed or BYOD devices,
* With approved public applications,
* And one or more private ICRC applications,
* Ready to be assigned to devices during enrollment.

