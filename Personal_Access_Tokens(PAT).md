# GitHub Personal_Access_Tokens (PAT)
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                        |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1 .  **An Overview on Personal-Access-Tokens (PAT)**                                                            | >> [` CHECK CONTENT `](#what-is-a-personal-access-token-or-pat)                                     |
| 2 .  **Generate A `Classic Personal-Access-Token (PAT)` using GitHub Web-Interface**                            | >> [` CHECK CONTENT `](#generating-classic-token-using-github-web-interface-)                       |
| 3 .  **`Regenrating` an Existing `Classic Personal-Access-Token (PAT)`**                                        | >> [` CHECK CONTENT `](#regenerating-an-existing-classic-token-)                                    |
| 4 .  **`Updating` an Existing `Classic Personal-Access-Token (PAT)`**                                           | >> [` CHECK CONTENT `](#updating-an-existing-classic-token-)                                        |
| 5 .  **Generate A `Fine-Grained Personal-Access-Token (PAT)` using GitHub Web-Interface**                       | >> [` CHECK CONTENT `](#generating-fine_grained-token-using-github-web-interface-)                  |
| 6 .  **`Regenrating` an Existing `Fine_Grained Personal-Access-Token (PAT)`**                                   | >> [` CHECK CONTENT `](#regenerating-an-existing-fine_grained-token-)                               |
| 7 .  **`Updating` an Existing `Fine_Grained Personal-Access-Token (PAT)`**                                      | >> [` CHECK CONTENT `](#updating-an-existing-fine_grained-token-)                                   |
| 8 .  **Configure Git to use `Personal-Access-Tokens for Authentication in the Git_CLI`**                        | >> [` CHECK CONTENT `](#using-personal-access-tokens-pat-for-authentication-in-the-git_cli)         |
| 9 .  **Configure Git to use `Personal-Access-Tokens for Authentication in the GitHub_CLI (gh)`**                | >> [` CHECK CONTENT `](#using-personal-access-tokens-pat-for-authentication-in-the-github_cli-gh)   |
| 10 . **`Refresh (Update/Remove Permissions) Personal-Access-Tokens` using GitHub_CLI (gh)**                     | >> [` CHECK CONTENT `](#refresh-personal-access-tokens-pat-using-github_cli-gh-)                    |
| 11.  **`Authenticate GitHub_Desktop` Using Personal-Access-Tokens**                                             | >> [` CHECK CONTENT `](#authenticate-github_desktop-using-personal-access-tokens-pat)               |
| 12.  **`Deleting` Personal-Access-Tokens**                                                                      | >> [` CHECK CONTENT `](#deleting-personal-access-tokens-pat)                                        |
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

### Regenerating an Existing Classic-Token :
  - Visit [`GitHub Web-Interface`](https://github.com/).
  - Click on Your `Profile-Picture` at the TOP-Right Corner >> Click on `Settings` >> Scroll Down and Click on `Developer Settings` >> Inside Developer Settings, Click on `Personal Access Tokens` >> Select `Tokens (classic)`.
  - Click on the `Name-Of-The-Token` which you want to Regenerate.<br>
    ![Classic_Token>>Click on Name-Of-The-Token](https://github.com/user-attachments/assets/101214c0-4201-4044-aa45-58bcf6dd6257)
    <br>
  - Click on `Regenrate token` to regenerate a New Token-Code for the Selected Token.<br>
    ![Classic_Token>>Regenerate_Token](https://github.com/user-attachments/assets/57317b4e-51b2-41de-b05f-72b6302a89f6)
    <br>
  - Set `New Expiration-Date` (Optional) >> Click on `Regenrate token`.<br>
    ![Classic_Token>>Set Expiration>>Regenerate_Token](https://github.com/user-attachments/assets/448ffd51-ecc6-4979-ad3d-b00ecc58f179)
    <br>
  - Copy and Securely save your **Regenerated Personal-Access-Token** now, as you won’t be able to View it Again!<br>
    ![Classic_Token>>Token Regenerated](https://github.com/user-attachments/assets/67dab367-aa5c-475d-8339-6ce96330c738)
    <br>

<br>

### Updating an Existing Classic-Token :
  - Visit [`GitHub Web-Interface`](https://github.com/).
  - Click on Your `Profile-Picture` at the TOP-Right Corner >> Click on `Settings` >> Scroll Down and Click on `Developer Settings` >> Inside Developer Settings, Click on `Personal Access Tokens` >> Select `Tokens (classic)`.
  - Click on the `Name-Of-The-Token` for which you want to Update Permissions and Details.<br>
    ![Classic_Token>>Click on Name-Of-The-Token](https://github.com/user-attachments/assets/101214c0-4201-4044-aa45-58bcf6dd6257)
    <br>
  - `Change Token-Name` by replacing the Existing-Name in the `Note` Field. (Optional)<br>
    ![Classic_Token>>Update_Token_Name/Note](https://github.com/user-attachments/assets/435287c4-83a9-434d-8d91-b5d4f6c79a63)
    <br>
  - `Update / Add / Remove Permissions or Scope` of the Token.<br>
    ![Classic_Token>>Update_Token_Permissions/Scope](https://github.com/user-attachments/assets/8be793ac-c3cd-4bba-b443-50a03ca8b18f)
    <br>
  - Scroll Down >> Click `Update token`.<br>
    ![Classic_Token>>Click on Update_Token](https://github.com/user-attachments/assets/ba8814f1-ea6c-4a63-8f31-9c3e7f1b5ccc)
    <br>

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

### Regenerating an Existing Fine_Grained-Token :
- Visit [`GitHub Web-Interface`](https://github.com/).
  - Click on Your `Profile-Picture` at the TOP-Right Corner >> Click on `Settings` >> Scroll Down and Click on `Developer Settings` >> Inside Developer Settings, Click on `Personal Access Tokens` >> Select `Fine-grained tokens`.
  - Click on the `Name-Of-The-Token` which you want to Regenerate.<br>
    ![Fine-Grained_Token>>Click on Name-Of-The-Token](https://github.com/user-attachments/assets/3732a23c-36a2-44f2-941b-65e7e755cd7d)
    <br>
  - Click on `Regenrate token` to regenerate a New Token-Code for the Selected Token.<br>
    ![Fine-Grained_Token>>Regenerate_Token](https://github.com/user-attachments/assets/5c118ba8-3f0d-4a4a-8553-813fb6ee2238)
    <br>
  - Set `New Expiration-Date` (Optional) >> Click on `Regenrate token`.<br>
    ![Fine-Grained_Token>>Set Expiration>>Regenerate_Token](https://github.com/user-attachments/assets/5f94faba-7a73-4e4d-b427-a6bd55fbeddb)
    <br>
  - Copy and Securely save your **Regenerated Personal-Access-Token** now, as you won’t be able to View it Again!<br>
    ![Fine-Grained_Token>>Token Regenerated](https://github.com/user-attachments/assets/4e2f2afb-e8fd-482b-909a-be42b48c2d85)
    <br>
    
<br>

### Updating an Existing Fine_Grained-Token :
  - Visit [`GitHub Web-Interface`](https://github.com/).
  - Click on Your `Profile-Picture` at the TOP-Right Corner >> Click on `Settings` >> Scroll Down and Click on `Developer Settings` >> Inside Developer Settings, Click on `Personal Access Tokens` >> Select `Fine-grained tokens`.
  - Click on the `Name-Of-The-Token` for which you want to Update Permissions and Details.<br>
    ![Fine-Grained_Token>>Click on Name-Of-The-Token](https://github.com/user-attachments/assets/3732a23c-36a2-44f2-941b-65e7e755cd7d)
    <br>
  - To Change/Update Token-Name and Token-Description, Click on the `Edit` Button besides the Token-Name at the Top. (Optional)<br>
    ![Fine-Grained_Token>>Edit_Token-Name>>Update Token-Description](https://github.com/user-attachments/assets/59103578-11f5-4b21-813a-e3a3aa8a039c)
    <br>
  - Enter `New Token-Name` and Update `Token-Description` below it >> Click `Save`. (Optional)<br>
    ![Fine-Grained_Token>>Edit_Token-Name>>Update Token-Description>>Save](https://github.com/user-attachments/assets/3c7e4527-9845-4355-9a46-b373c7403a57)
    <br>
  - Scroll Down >> Click `Edit` besides `Access on <Username>` Heading.<br>
    ![Fine-Grained_Token>>Edit Acess/Permissions](https://github.com/user-attachments/assets/91bd312b-759a-4c9c-abca-6b4c1c546203)
    <br>
  - `Update / Add / Remove Permissions` for the Token.<br>
    ![Fine-Grained_Token>>Update_Token_Permissions](https://github.com/user-attachments/assets/c56fa20b-93e5-4f81-92f2-d140d7e24979)
    <br>
  - Scroll Down >> Click `Update`.<br>
    ![Fine-Grained_Token>>Click on Update](https://github.com/user-attachments/assets/a4ffda40-c804-4bba-80eb-d9b93abc9b84)
    <br>
    
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

### Refresh Personal-Access-Tokens (PAT) using GitHub_CLI (gh) :
  - The `gh auth refresh` command in the GitHub CLI is used to `Update or Refresh your Authentication Credentials`.
  - It can `Add New Scopes`, `Revalidate Tokens`, or `Synchronize Token Permissions` for GitHub or GitHub Enterprise accounts.

<br>
<div align="center">
______________________________________________________
</div>
<br>

  - **`To Synchronize or Revalidate Tokens :`**
    - Open `Command-Prompt` or `Git-Bash` Terminal.
    - Paste the `gh auth refresh` command to `Revalidate Tokens or Synchronize Permissions`.<br>
      ```
      gh auth refresh
      ```
      <br>
    - Copy the `8-Digit Aplha Numeric Code` >> Press `Enter` to redirect to GitHub Sign_In Page.<br>
      ![gh auth refresh>>Copy-the-Code>>Press Enter](https://github.com/user-attachments/assets/ede5e6bf-03fd-4d13-becb-c800325fcfd0)
      <br>
    - Continue With an Exisiting Account to `Synchronize Permissions` >> Click `Continue` besides the Account with which you want to Continue.<br>
      ![Continue with Existing_Account>>Synchronize_Permissions](https://github.com/user-attachments/assets/1b2c6be1-866e-4958-8060-f33932d6cd5f)
      <br>
      <div align="center">
       
      **OR**
      </div>

      Click `Use a different account` to `Revalidate Tokens` >> Enter `Username` in the `Username Field` and `Personal-Access-Token` in the `Password Field` >> Click `Sign in`.<br>
      ![Use a different account>>Revalidate_Tokens](https://github.com/user-attachments/assets/c5fdcdcd-13bb-4f55-a78d-e63ba937ce8d)
      <br>
    - Enter the `8-Digit Alpha-Numeric CODE` copied from your Terminal >> Click `Continue`.<br>   
      ![GitHub_SignIn>>Enter_Authentication_CODE](https://github.com/user-attachments/assets/2583347d-7fd9-4445-99bd-15e2c9cc297f)
      <br>
    - Click `Authorize GitHub` to `Synchronize or Revalidate Tokens`.<br>
      ![Authorize-GitHub](https://github.com/user-attachments/assets/f7fb521b-acf6-4454-93e8-9502697e38a0)
      <br>
    - An `Authorization-Success-Widget` will be displayed.<br>
      ![Revalidation/Synchronization Successful](https://github.com/user-attachments/assets/a252645a-be07-4040-9d94-bacecf19f190)
      <br>
    - Return back to the Terminal.<br>
      ![Authentication_Successful](https://github.com/user-attachments/assets/99cb204f-c8ff-480a-9128-bc18abe2e2d0)
      <br>

  - **`To Verify Authorization Status`**
    - Paste the following command to `Verify Authorization Status`.<br>
      ```
      gh auth status
      ```
      <br>
    - Verify whether the `GitHub_Account` and `Token_Scopes` have been Synchronized / Revalidated Successfully.<br>
      ![Screenshot 2024-12-10 074419](https://github.com/user-attachments/assets/bdce09bc-3515-401c-ad0e-efc202b6e2a9)
      <br>

<br>      
<div align="center">
______________________________________________________
</div>
<br>

  - **`To Add or Remove Permissions/Scope :`**
    - Open `Command-Prompt` or `Git-Bash` Terminal.
    - Paste the Following Command to `Add Scopes/Permissions` to the Token.<br>
      ```
      gh auth refresh -h HOSTNAME -s "SCOPES TO BE ADDED"
      ```
      `Note:` Replace `HOSTNAME` with your preferred host (`github.com`, `github.enterprise.com`) >> Replace `"SCOPES TO BE ADDED"` with the required `"Scopes/Permissions"`.
      <br>
      <div align="center">
       
      **OR**
      </div>

      Paste the Following Command to `Remove Scopes/Permissions` from the Token.<br>
      ```
      gh auth refresh -h HOSTNAME -r "SCOPES TO BE REMOVED"
      ```
      `Note:` Replace `HOSTNAME` with your preferred host (`github.com`, `github.enterprise.com`) >> Replace `"SCOPES TO BE REMOVED"` with the `"Scopes/Permissions"` which are to be removed.
      <br>
    - Copy the `8-Digit Aplha Numeric Code` >> Press `Enter` to redirect to GitHub Sign_In Page.<br>
      ![Add Scopes>>Copy Code>>Press Enter](https://github.com/user-attachments/assets/5b00bfc5-3a0c-4b22-be39-da68d4cb86d9)
      <br>
      <div align="center">
       
      **OR**
      </div>
      
      ![Remove Scopes>>Copy Code>>Press Enter](https://github.com/user-attachments/assets/a710c108-f47d-47b7-b7d1-703d26616421)
      <br>
    - Click `Continue` besides the Account for which you want to Add or Remove Scopes/Permissions.<br>
      ![Continue with Existing_Account](https://github.com/user-attachments/assets/1b2c6be1-866e-4958-8060-f33932d6cd5f)
      <br>
    - Enter the `8-Digit Alpha-Numeric CODE` copied from your Terminal >> Click `Continue`.<br>   
      ![GitHub_SignIn>>Enter_Authentication_CODE](https://github.com/user-attachments/assets/2583347d-7fd9-4445-99bd-15e2c9cc297f)
      <br>
    - Click `Authorize GitHub` to `Synchronize or Revalidate Tokens`.<br>
      ![Authorize-GitHub](https://github.com/user-attachments/assets/f7fb521b-acf6-4454-93e8-9502697e38a0)
      <br>
    - An `Authorization-Success-Widget` will be displayed.<br>
      ![Scopes Addition/Removal Successful](https://github.com/user-attachments/assets/a252645a-be07-4040-9d94-bacecf19f190)
      <br>
    - Return back to the Terminal.<br>
      ![Scopes Added>>Authentication Successful](https://github.com/user-attachments/assets/83e9a991-b5c1-4181-8e3b-96895fca9cbb)
      <br>
      <div align="center">
       
      **OR**
      </div>
      
      ![Scopes Removed>>Authentication Successful](https://github.com/user-attachments/assets/8b518fee-e8c3-4d49-9d84-34ce3918c119)
      <br>

  - **`To Verify Authorization Status`**
    - Paste the following command to `Verify Authorization Status`.<br>
      ```
      gh auth status
      ```
      <br>
    - Verify whether the `Token_Scopes` have been Updated Successfully.<br>
      ![Verify Scopes_Addition](https://github.com/user-attachments/assets/c8cb46e6-3cfc-444a-b70d-e3d264a53ec4)
      <br>
      <div align="center">
       
      **OR**
      </div>
      
      ![Verify Scopes_Removal](https://github.com/user-attachments/assets/d6299c76-2851-48c9-b1bd-47355b3a8ebb)
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

## Deleting Personal-Access-Tokens (PAT)
  - Visit [`GitHub Web-Interface`](https://github.com/).
  - Click on Your `Profile-Picture` at the TOP-Right Corner >> Click on `Settings` >> Scroll Down and Click on `Developer Settings` >> Inside Developer Settings, Click on `Personal Access Tokens` >> Select the `Category` under which you want to Delete Tokens (`Tokens (classic)` or `Fine-grained tokens`).<br>
    ![GitHub>>Settings>>Developer_Settings>>Personal-Access-Tokens>>Select the Category](https://github.com/user-attachments/assets/b9acd947-2001-497e-9f1b-77dbc82b8cc2) 
    <br>
  - Click `Delete` Button corresponding to **Name-Of-The-Token** which you want to Remove.<br>
    ![Fine-Grained_Token>>Delete_Token](https://github.com/user-attachments/assets/00dd1e28-432d-4221-b9de-c645315ea581)<br>
    <div align="center">
     
     **OR**
    </div>
    
    ![Classic_Token>>Delete_Token](https://github.com/user-attachments/assets/f948453c-d775-45d6-abda-3a25361ea4d8)<br>
  - A Pop-Up Window will appear >> Click the `I understand, delete this token` Button in the Pop-Up.<br>
    ![Delete_Token>>Click on I-understand-delete-this-token](https://github.com/user-attachments/assets/f637b773-4d5d-4770-8c51-22e6ede0b5a8)
    <br>

<br>

---
<br>
