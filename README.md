# Employee Identity Lifecycle Management with Microsoft Entra ID

## Project status
In progress — personal learning lab.

## Objective
Practise managing employee identities through onboarding,
department transfers, and offboarding in Microsoft Entra ID.

## Business scenario
Adera Technologies is a fictional company with HR and Finance
departments. Employees need appropriate access when they join,
updated access when their duties change, and access removed
when they leave.

## Tools
- Microsoft Entra admin center
- GitHub for project documentation

## Planned activities
- Create fictional employee accounts.
- Create department security groups.
- Update group membership during a department transfer.
- Disable a departing employee's account and revoke sessions.
- Verify changes and document results.

## Progress
- Confirmed access to my personal Entra directory.
- Confirmed my administrator account has the Global Administrator role.
- Opened the All users page.
- Created this repository for documentation.

## Documentation approach
For each activity, I will record:
1. The business requirement.
2. The action performed and why.
3. Screenshots with sensitive information removed.
4. Verification results.
5. Lessons learned.

## Lab boundaries
This project uses fictional employees in a personal lab.
Group membership alone does not enforce access to a resource;
resource permissions must be configured and tested separately.


## Activity 1 — Create an employee account

### Business requirement
A new HR Assistant, Ada Test, needs an employee account.

### Actions completed
Created Ada's account in Microsoft Entra ID with:
- Display name: Ada Test<img width="1605" height="956" alt="01-ada-user-created" src="https://github.com/user-attachments/assets/846dfdc8-9880-4e89-987d-6b8c1fbf6530" />

- Department: HR
- Job title: HR Assistant

### Verification
Account creation succeeded.
Verified that Ada's department is HR, her job title is HR Assistant,
and her account is enabled.

### What I learned
A user account represents an employee's digital identity.
Setting the department to HR does not automatically grant
access to HR resources.
### Screenshot

## Activity 2 — Create an HR security group

### Business requirement
Organize HR employees who will need read-only access
to employee records.

### Actions completed
- Created the security group SG-HR-Readers.
- Used Assigned membership.
- Added Ada Test as a member.

### Verification
Opened the group's Members page and confirmed
Ada Test was listed.

### What I learned
Group membership lets administrators manage users together.
The group does not yet grant access to employee records;
resource permissions still need to be configured.

###Screenshot<img width="1182" height="802" alt="02-hr-group-membership" src="https://github.com/user-attachments/assets/0ea8b9a6-e1c2-49be-bc6b-3e629c804b02" />


## Activity 3 — Transfer an employee between departments

### Business scenario
Ada moves from HR to Finance.
Manager approval is simulated for this lab.

### Actions completed
- Created SG-Finance-Readers.
- Removed Ada from SG-HR-Readers.
- Added Ada to SG-Finance-Readers.

### Verification
- Confirmed Ada was absent from the HR group's member list.
- ##screenshot
- <img width="1182" height="802" alt="03-hr-membership-removed" src="https://github.com/user-attachments/assets/ba79653d-707d-45a6-b02a-2d1a965c69f1" />

- Confirmed Ada was present in the Finance group's member list.
- ##screenshot<img width="1182" height="802" alt="04-finance-membership-added" src="https://github.com/user-attachments/assets/07677d51-706f-4995-b80f-81521196a593" />


[Ada's updated Finance department and job title]
###Screenshot <img width="1182" height="802" alt="05-ada-finance-profile" src="https://github.com/user-attachments/assets/6523c1fe-4dcf-4d16-b315-ac449042c138" />


### Scope
Verified group membership changes only.
No application or document permissions are connected
to these groups yet.
