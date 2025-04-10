---
description: Process flow of the Dormitory Management
---

# Dormitory management

```mermaid
flowchart TD
    A["Start - New Admission"] --> B["Select Date of Admission"]
    B --> C["System Predefines Available Bed"]
    C --> D["Change Bed assignation (Optional)"]
    D --> E{"Is there a caregiver?"}
    E -- Yes --> F["Create Admission for Caregiver"]
    E -- No --> H["Activate Admission (Reserve Bed)"]
    H --> I["SU Arrives → Admit to Dorm"] & J["Caregiver Arrives → Admit to Dorm"]
    I --> K["Discharge SU"]
    J --> L["Discharge Caregiver"]
    K --> M{"Is there a caregiver?"}
    M -- Yes --> N["Discharge All caregiver"]
    M -- No --> O["Create Invoice"]
    N --> O
    F --> H
```

