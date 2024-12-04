# GitHub Personal_Access_Tokens (PAT)
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **An Overview on Personal-Access-Tokens (PAT)**                                                            | >> [` CHECK CONTENT `](#what-is-a-personal-access-token-or-pat)                               |
| 1.  **Create A Personal-Access-Token (PAT)**                                                                   | >> [` CHECK CONTENT `](#create-a-personal-access-token-pat)                                   |
| 2.  **Create A Repository Using GitHub_CLI (gh) Commands**                                                     | >> [` CHECK CONTENT `](#repository-initialization--using-github_cli-gh--recommended)          |
| 3.  **Create A Repository Using GitHub_Web_Interface**                                                         | >> [` CHECK CONTENT `](#repository-initialization--using-github_website--recommended)         |
| 4.  **Create A Repository Using GitHub_Desktop**                                                               | >> [` CHECK CONTENT `](#repository-initialization--using-github_desktop-)                     |
| 5.  **Create A Repository Using VSCode Source_Control Tool**                                                   | >> [` CHECK CONTENT `](#repository-initialization--using-vscode-source-control-)              |
</div>
<br>

---
<br>

## What is a Personal-Access-Token or (PAT)?
  - A `Personal Access Token (PAT)` is a String of Characters (a type of API Token) that serves as an Authentication Method for accessing APIs or performing tasks on platforms like `GitHub`, `GitLab`, or other Version Control Systems.
  - It is used as a `Replacement for Passwords`, especially in contexts where `Automated or Programmatic Access` is needed.
  - `GitHub introduced Personal-Access-Tokens (PATs) on August 12, 2013`, as part of their API Authentication Mechanism.
  - Over time, they `replaced Password-Based Authentication` for Git operations to enhance Security, with `Passwords Officially Deprecated for API use on August 13, 2021`.
  <br>
  
  - **Features:**
    - **`API Authentication:`** PATs allow developers to access a platform's API Programmatically.
    - **`Git Operations:`** Used to Authenticate Git Operations (e.g. git clone, git push, git pull) instead of passwords.
    - **`Tool Access:`** Enables External Tools (e.g., GitHub CLI, GitHub Desktop) to Authenticate Securely.
    - **`Scoped Access:`** Provides Control over which Resources can be Accessed.
  <br>
  
  - **Advantages Over Password-Authentication:**
    - **`Enhanced Security:`** **PATs are Specific to Certain Tasks and cannot be used to Log In to the Web Interface**, reducing the Risk of Full Account Compromise. They can be Encrypted and Stored Securely, Avoiding Exposure of Actual Passwords.
    - **`Fine-Grained Permissions:`** **PATs allow you to grant only the Necessary Permissions, such as Read-Only or Specific Repository Access**, unlike Passwords which provide Full Access.
    - **`Scoped Usage:`** **You can Limit PATs to Specific Actions**, such as accessing APIs, workflows, or repository management, while passwords have no such scoping capabilities.
    - **`Expiration and Control:`** **PATs can be Configured to Expire automatically after a Set Period**, improving Security by Limiting their Validity.
    - **`Ease of Revocation:`** **Individual PATs can be Revoked without affecting your Main Account or Other Access Methods.** Changing a Password disrupts all Tools and Sessions using it.

<br>

---
<br>

## Create A Personal-Access-Token (PAT)

<br>

---
<br>
