# GitHub Personal_Access_Tokens (PAT)
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                        |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1 .  **An Overview on Personal-Access-Tokens (PAT)**                                                            | >> [` CHECK CONTENT `](#what-is-a-personal-access-token-or-pat)                                     |
| 2 .  **Generate A `Classic Personal-Access-Token (PAT)` using GitHub Web-Interface**                            | >> [` CHECK CONTENT `](#generating-classic-token-using-github-web-interface-)                       |
| 3 .  **`Regenrating` the Existing `Classic Personal-Access-Token (PAT)`**                                       | >> [` CHECK CONTENT `](#regenerating-the-existing-classic-tokens-)                                  |
| 4 .  **`Updating` the Existing `Classic Personal-Access-Token (PAT)`**                                          | >> [` CHECK CONTENT `](#updating-the-existing-classic-tokens-)                                      |
| 5 .  **Generate A `Fine-Grained Personal-Access-Token (PAT)` using GitHub Web-Interface**                       | >> [` CHECK CONTENT `](#generating-fine_grained-token-using-github-web-interface-)                  |
| 6 .  **`Regenrating` the Existing `Fine_Grained Personal-Access-Token (PAT)`**                                  | >> [` CHECK CONTENT `](#regenerating-the-existing-fine_grained-tokens-)                             |
| 7 .  **`Updating` the Existing `Fine_Grained Personal-Access-Token (PAT)`**                                     | >> [` CHECK CONTENT `](#updating-the-existing-fine_grained-tokens-)                                 |
| 8 .  **Configure Git to use `Personal-Access-Tokens for Authentication in the Git_CLI`**                        | >> [` CHECK CONTENT `](#using-personal-access-tokens-pat-for-authentication-in-the-git_cli)         |
| 9 .  **Configure Git to use `Personal-Access-Tokens for Authentication in the GitHub_CLI (gh)`**                | >> [` CHECK CONTENT `](#using-personal-access-tokens-pat-for-authentication-in-the-github_cli-gh)   |
| 10.  **`Authenticate GitHub_Desktop` Using Personal-Access-Tokens**                                             | >> [` CHECK CONTENT `](#authenticate-github_desktop-using-personal-access-tokens-pat)               |
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

  - **GitHub offers Two Types of Personal-Access-Tokens:**
    - [**`Classic Personal-Access-Tokens`**](#classic-personal-access-tokens)
    - [**`Fine Grained Personal-Access-Tokens`**](#fine-grained-personal-access-tokens)
<br>

### [Classic Personal-Access-Tokens](#classic-personal-access-tokens-pat):
  - Classic Tokens provide `Account-Wide Access`.
  - Classic Tokens offer `Broad, Predefined scopes with Limited Granularity`.
  - Classic Tokens `Cannot Limit Access to Specific Repositories`.
  - Classic Tokens are `Less Secure` due to their Broad Access.
<br>

### [Fine Grained Personal-Access-Tokens](#fine_grained-personal-access-tokens-pat):
  - Fine-Grained Tokens provide `Repository-Specific Access`.
  - Fine-grained Tokens allow `Precise Control over Permissions at the Repository and Action Level`.
  - Fine-grained Tokens are `More Secure` with Tailored Access to Resources.
  - `Permissions are Easier to Audit and Adjust` using Fine-Grained Tokens as compared to Classic Tokens. 
<br>

---
<br>

## Classic Personal-Access-Tokens (PAT)
### Generating Classic-Token Using [GitHub Web-Interface](https://github.com/) :
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

### Regenerating the Existing Classic-Tokens :

<br>

### Updating the Existing Classic-Tokens :

<br>

---
<br>

## Fine_Grained Personal-Access-Tokens (PAT)
### Generating Fine_Grained-Token Using [GitHub Web-Interface](https://github.com/) :
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
  - Inside Developer Settings, Click on `Personal Access Tokens` >> Select `Fine Grained Tokens` >> Click on `Generate new token (classic)`.<br>
    ![GitHub_Settings>>Developer Settings >> Generate Token](https://github.com/user-attachments/assets/a0f12026-2e19-4eb8-a455-cfd70ef11688)
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
  - Enter an appropriate `Token Description` (Optional).<br>
    ![Generate Token>>Enter Token Description](https://github.com/user-attachments/assets/9a2bf9e3-20a0-484a-8a28-2a67d18a2915)
    <br>
  - Choose the type of `Repository Access` you wish to Grant with the Token.<br>
    ![Generate Token>>Choose Type OF Repository  Access](https://github.com/user-attachments/assets/31230dbf-11d3-4398-8c6d-31474eeb35cf)
    <br>
    `Note:` Generally, the `Only select repositories` Scope is Recommended for such Granular-Access Tokens.<br>
    Select `Only select repositories` option >> `Select the Repositories` from the Dropdown Menu that the Token will Access.<br>
    ![Generate Token>>Only select repositories](https://github.com/user-attachments/assets/93a68068-4fd1-43f1-be87-d5dc49d708a9)
    <br>
  - Select `Permissions` which you want to grant to the Token. There are two types of Permissions `Repository Permissions` and `Account Permissions`.<br>
    - **Repository Permissions [`Note:` This option is not shown for `Public Repositories` access scope.]:**
      - Repository Permissions refer to the Access_Rights and Privileges granted to a User, Collaborator, or Token for performing Specific Actions on a Repository.
      - Some `General Repository Permissions` based on Roles, for ensuring Security and Efficiency, are as follows:
        |Permission Category  |Public Users |Contributors    |Administrators  |
        |---------------------|-------------|----------------|----------------|
        |Contents             |`Read`       |`Read and Write`|`Read and Write`|
        |Issues               |`Read`       |`Read and Write`|`Read and Write`|
        |Pull Requests        |`No Access`  |`Read and Write`|`Read and Write`|
        |Discussions          |`No Access`  |`Read and Write`|`Read and Write`|
        |Administration       |`No Access`  |`No Access`     |`Read and Write`|
        |Merge Queues         |`No Access`  |`No Access`     |`Read and Write`|
        |Metadata (By Default)|`No Access`  |`Read`          |`Read`          |
      - ![Generate Token>>Repository Permissions_1](https://github.com/user-attachments/assets/5960a09b-a1ab-43f2-8f2a-9963582ca0ba)<br>
        ![Generate Token>>Repository Permissions_2](https://github.com/user-attachments/assets/bf7f0954-794e-4e21-b818-333d30eef352)<br>
    - **Account Permissions:**
      - Account Permissions in Fine-Grained Tokens define the Level of Access granted to Account-Wide Resources.  
      - Some `General Account Permissions` based on Roles, for ensuring Security and Efficiency, are as follows:
        |Permission Category  |Public Users / Contributors  |Administrators  |
        |---------------------|-----------------------------|----------------|
        |Email addresses      |`Read`                       |`Read and Write`|
        |Followers            |`Read`                       |`Read`          |
        |GPG Keys             |`No Access`                  |`Read and Write`|
        |SSH Keys             |`No Access`                  |`Read and Write`|
        |Profile              |`Read`                       |`Read and Write`|
      - ![Generate Token>>Account Permissions_1](https://github.com/user-attachments/assets/671df5af-421c-4363-baf9-9688101201ba)<br>
        ![Generate Token>>Account Permissions_2](https://github.com/user-attachments/assets/8cc0492a-a955-427e-9f45-8cd214dc6bd2)<br>
   - Click on `Generate Token` at the bottom of the page to Create your Personal-Access-Token.<br>
     ![Generate Token>>Click on Generate_Token](https://github.com/user-attachments/assets/37c24489-f2c0-431b-8258-72613e93ba47)
     <br>
   - **Congratulations! Your Personal-Access-Token has been successfully generated!!**<br>
     ![Copy the Personal-Access-Token](https://github.com/user-attachments/assets/3b34ea0d-a447-4fb9-bb52-d58520928924)
     <br>
     `Alert!:` Make sure to Copy and Securely save your Personal-Access-Token now, as you won’t be able to View it Again!
<br>

### Regenerating the Existing Fine_Grained-Tokens :

<br>

### Updating the Existing Fine_Grained-Tokens :

<br>

---
<br>

## Using Personal-Access-Tokens (PAT) for Authentication in the Git_CLI
  - To Store and Use a Personal-Access-Token (PAT) in the Git CLI, you can utilize [`Git-Credential-Manager (GCM) or Git's Credential-Helper`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git-Credential-Manager%20(GCM)%20and%20Git%20Credential-Helper.md) for Secure Management and Authentication.

<br>

---
<br>

## Using Personal-Access-Tokens (PAT) for Authentication in the GitHub_CLI (gh)
  - Open your terminal or command prompt.
  - Paste the following Command in Terminal to `Begin Authentication`.
    ```
    gh auth login
    ```
  - Click or Press Enter for **`GitHub.com`** under `Where do you use GitHub?` >> Click or Press Enter for **`HTTPS`** under `What is your preferred protocol for Git operations on this host?` >> Enter `Y` or `Yes` for `Authenticate Git with your GitHub credentials?` >> Click or Press Enter for **`Paste an authentication token`** under `How would you like to authenticate GitHub CLI?`<br>
    ![gh auth login](https://github.com/user-attachments/assets/cb0484b7-f86d-44f4-a147-ea792192a7b4)
    <br>
  - `Enter/Paste your Personal-Access-Token` >> `Press Enter`<br>
    ![gh auth login>>Paste a Token](https://github.com/user-attachments/assets/ccbc01b9-f5c0-4996-8949-81fed0947728)
    <br>
  - **Congratulations! Your account has been authenticated successfully!**<br>
    ![gh auth login>>Authentication Successful](https://github.com/user-attachments/assets/82b9b86a-346d-4db0-adbb-48785c96b2a9)
    <br>
<br>

---
<br>

## Authenticate GitHub_Desktop Using Personal-Access-Tokens (PAT)
  - Open `GitHub_Desktop`.
  - Browse `File` >> Click on `Options...` o/r Use shortcut `Ctrl + ,`.<br>
    ![GitHub_Desktop>>File>>Options....](https://github.com/user-attachments/assets/4f1f7d1e-a95a-47cf-b9fc-68ef8dded11e)
    <br>
  - Under Accounts >> Click on `Sign In`.<br>
    ![Options>>Accounts>>Sign In](https://github.com/user-attachments/assets/5fc1abba-8e75-4d08-b1d6-319170f08f77)
    <br>
  - You will be redirected to the Sign In web page after clicking on the `Continue with browser` Button.<br>
    ![Redirect_To_SignIn_Webpage](https://github.com/user-attachments/assets/892be788-c582-4f00-891f-47ee5dfeaaff)
    <br>
  - `Sign In` to Your `GitHub Account` >> Enter `Email/Username` in the `Username Field` >> Enter `Personal-Access-Token` in the `Password Field` >> Click `Sign in`.<br>
    ![Sign_In with PAT](https://github.com/user-attachments/assets/fa59c19b-579e-45c4-88d1-2200aee6007f)
    <br>
  - **Congratulations! Your account has been authenticated successfully!** >> Click `Open GithubDesktop.exe` for redirecting to GitHub_Desktop.<br>
    ![Redirecting Github_Desktop](https://github.com/user-attachments/assets/807f3edc-20e2-404b-95f1-0c01288397f3)
    <br>

<br>

---
<br>
