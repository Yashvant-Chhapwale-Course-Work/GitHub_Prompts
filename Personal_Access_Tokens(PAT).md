# GitHub Personal_Access_Tokens (PAT)
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **An Overview on Personal-Access-Tokens (PAT)**                                                            | >> [` CHECK CONTENT `](#what-is-a-personal-access-token-or-pat)                               |
| 1.  **Create A Personal-Access-Token (PAT)**                                                                   | >> [` CHECK CONTENT `](#generating-pat-using-github-web-interface-)                           |
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
  - Over time, they `Replaced Password-Based Authentication` for Git operations to enhance Security, with `Passwords Officially Deprecated for API use on August 13, 2021`.
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
### Generating PAT Using [GitHub Web-Interface](https://github.com/) :
  - Visit [`GitHub Web-Interface`](https://github.com/).
  - Click on Your `Profile-Picture` at the TOP-Right Corner.<br>
    ![GitHub>>Profile](https://github.com/user-attachments/assets/57ba16d4-2286-45a1-9d53-4a223377bbe9)
    <br>
  - Click on `Settings` from the Dropdown Menu.<br>
    ![GitHub>>Profile>>Settings](https://github.com/user-attachments/assets/e60f269c-8c02-474f-aedc-dc1581f6753c)
    <br>
  - Scroll Down and Click on `Developer Settings` in Settings.<br>
    ![GitHub_Settings>>Developer Settings](https://github.com/user-attachments/assets/2aca4a9d-ef6d-4cb2-b627-2ee2a441e02f)
    <br>
  - Inside Developer Settings, Click on `Personal Access Tokens` >> Select `Tokens (classic)` >> Click on `Generate new token (classic)`.<br>
    ![GitHub_Settings>>Developer Settings >> Generate Token](https://github.com/user-attachments/assets/09e38ff2-b223-4e78-a786-2a6a58f6982b)
    <br>
  - Enter an apporpriate `Token Name`. Replace **'Demo_Token'** with your **'Desired-Token_Name'**<br>
    ![Generate Token>>Enter Token Name](https://github.com/user-attachments/assets/b35e45f6-bcab-4f22-b45c-5d220c374e75)
    <br>
  - Set `Expiration`.<br>
    ![Generate Token>>Expiration](https://github.com/user-attachments/assets/21827c5f-a5cb-4446-80a2-8f04ccfdec06)
    <br>
    `Note:` You can also implement `Custom Expiration` for better Security and Control.<br>
    ![Generate Token>>Custom Expiration](https://github.com/user-attachments/assets/20d2ac36-b579-457d-be6b-562dd1e510dc)
    <br>
  - Under `Select Scopes` choose the permissions you want to grant to the token.<br>
    ![Generate Token>>Select Scopes_1](https://github.com/user-attachments/assets/7ae20ab8-1709-4f47-9df3-afad2eef295c)
    <br>
    ![Generate Token>>Select Scopes_2](https://github.com/user-attachments/assets/aec8d8ca-a996-4b26-bc3f-46d9eca3800e)
    <br>
    **Here are some `General Scopes` commonly selected for a PAT to Enhance Efficiency:**
    - `repo`
    - `workflow`
    - `write:packages`
    - **`Alert:` Any Scopes other than the three mentioned above are not recommended for General Use Tokens or Public-Access Tokens.**
    - **`Note:`If you are the Administrator then you can enable the Scopes mentioned in the Image above for General Administrative Efficiency.**
    <br>
  - Click on `Generate Token` at the bottom of the page to Create your Personal-Access-Token.<br>
    ![Generate Token>>Click on Generate_Token](https://github.com/user-attachments/assets/491d6f18-68cb-4171-8f94-016f43f77b93)
    <br>
  - **Congratulations! Your Personal-Access-Token has been successfully generated!!**<br>
    ![Copy the Personal-Access-Token](https://github.com/user-attachments/assets/98324cb9-9ef6-4aa9-b4e2-153bfad9c805)
    <br>
    `Alert!:` Make sure to Copy and Securely save your Personal-Access-Token now, as you won’t be able to View it Again!
<br>

### Generating PAT Using [GitHub Web-Interface](https://github.com/)

<br>

---
<br>
