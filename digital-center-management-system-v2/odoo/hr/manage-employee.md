# Manage employee

## Create/Update an Employee

**Go to the Employees Module**: Open the **"Employees"** app from the main dashboard.

**If the employee already exist**: Locate the employee you want to update using the search bar or list view.\
Then click on their profile and press the **"Edit"** button.

**If not, Click on Create**: Press the **"Create"** button to add a new employee.

<figure><img src="../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>



1. Name of the Employee
2. Job position
3. Some tags, You can create tags for your employee to be able to filter or group them
4. This part is most important, this will create the organigramme of your center.

On the first tabs, you can find the work address and location, along with the organizational chart based on the "Manager" mentioned above. You'll be able to set the approver for time off requests and select the employee's planning. The correct timezone will be set by default

<figure><img src="../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

On the second tabs, you will found lor of private information of the employee. It's preferable to not put too many sensitive data about the employee.&#x20;

<figure><img src="../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

## Hide old employee

1. **Go to the Employees Module**: Open the **"Employees"** app from the main dashboard.
2. **Find the Employee**: Locate the employee you want to archive using the search bar or list view.
3. **Open Employee Record**: Click on the employee’s name to access their profile.
4. **Archive the Employee**: Click the **"Action"** button (top-right corner), then select **"Archive"** from the dropdown menu.
5. **Confirmation**: The employee is now archived and will no longer appear in active employee lists, but their data remains in the system.

To restore the employee later, go to **Filters > Archived**, open their profile, and click **"Unarchive"**.

```mermaid
graph TD;
    %% HR Initiates the Employee Creation
    A["HR: Log into Odoo"] --> B["Go to Employees Module"];
    B --> C["Click on 'Create' to Add New Employee"];

    %% Employee Information Entry %%
    C --> D["Enter Employee Details (Name, Position, Department, etc.)"];
    D --> E["Assign a Work Email & Contact Details"];
    E --> F["Set Contract Type & Start Date"];
    F --> G["Upload Necessary Documents (ID, Resume, etc.)"];

    %% System Configurations
    G --> H["Assign User Access Rights"];
    H --> I["Link Employee to Payroll & Attendance"];
    I --> J["Define Work Schedule & Time Off Policies"];

    %% Final Validation & Activation
    J --> K["Review & Validate Employee Information"];
    K --> L["Save & Activate Employee Profile"];
    L --> M["Employee Successfully Created in Odoo 🎉"];

```

