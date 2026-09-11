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
