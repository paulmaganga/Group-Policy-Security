# Lab: Group Policy Management (GPO)

## Objective
To design and implement a structured Group Policy environment. This lab focuses on hardening system security, standardizing the user experience, and automating configuration changes across a domain-joined network.

## Technical Environment
- **Domain Controller:** Windows Server 2022
- **Client:** Windows 11 Enterprise
- **Management Tool:** Group Policy Management Console (GPMC)

## Lab Workflow: Step-by-Step

### 1. Planning & Organizational Units (OUs)
* Defined a logical OU structure (e.g., *Employees, HR, IT*) to allow for granular policy application.
* Created test user accounts within these OUs to serve as targets for policy testing.

### 2. GPO Creation & Configuration
* Created a new Group Policy Object (GPO) linked to the target OU.
* **Security Hardening:** Implemented policies to restrict access to sensitive system areas (e.g., disabling the Control Panel or restricting Command Prompt access).
* **Environment Standardization:** Configured policies for desktop background enforcement and mapped network drives to ensure all users have access to required resources.

### 3. Policy Application & Link Management
* Verified link order and precedence to ensure policies were applied in the correct sequence.
* Applied "Enforced" and "Block Inheritance" settings to understand how to manage policy conflicts.

### 4. Verification & Troubleshooting
* **Force Update:** Ran `gpupdate /force` on the Windows 11 client to trigger an immediate policy refresh.
* **Result Analysis:** Executed `gpresult /r` on the client to verify which policies were successfully applied and identify any conflicts.
* **Troubleshooting:** Investigated cases where policies failed to apply by reviewing Event Viewer logs and ensuring proper DNS/DC connectivity.

## Proof of Implementation
<img width="1900" height="877" alt="Group Policy Management" src="https://github.com/user-attachments/assets/31d1b6f0-91b6-42c6-91d3-18b392a16ccf" />


## Key Learnings
* **Security Through Automation:** Learned how GPOs allow administrators to enforce security standards at scale rather than manually configuring individual workstations.
* **Inheritance & Precedence:** Gained a deep understanding of how GPO hierarchy works and how to resolve policy conflicts using GPMC.
* **Validation:** Developed the habit of always verifying policy application on the client-side to ensure intended results, rather than assuming success based on server-side configuration.
