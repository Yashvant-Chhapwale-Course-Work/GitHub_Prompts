# Git-Credential-Helper (CH)
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                        |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1. **An Overview `Credential-Helper (CH)`**                                                                     | >> [` CHECK CONTENT `](#what-is-a-credential_helper-ch)                                             |
| 2. **Git `Cache`**                                                                                              | >> [` CHECK CONTENT `](#git_cache)                                                                  |
| 3. **Git `Store`**                                                                                              | >> [` CHECK CONTENT `](#git_store)                                                                  |
| 4. **Git `Credential-Manager` (GCM)**                                                                           | >> [` CHECK CONTENT `](#git_credential_manager-gcm)                                                 |
</div>
<br>

---
<br>

## **What is a Credential_Helper (CH) ?**
- A `Git Credential-Helper (CH)` is a tool that remembers your Git **username** and **password** or **personal-access-token (PAT)** so you don’t have to type them every time you **push**, **pull**, or **clone** from a Remote Git Repository (like `GitHub`). 
- Git has different types of helpers. Some common ones are:
  - [`cache`](#git_cache)
  - [`store`](#git_store)
  - [`manager`](#git_credential_manager-gcm)
<br>

 ### [Git Cache:](#git_cache)
  - Git `Cache` is a temporary `Memory-Based` **Credential_Helper** for Git.
  - It stores your **Git_Credentials** in `Memory (RAM)` for a **short time**, so you don’t have to type them again during that session.
<br>

### [Git Store:](#git_store)
  - Git `Store` saves your credentials in a `Plain-Text` format.
  - It stores the **Git_Credentials** in a `Text File`, so that you don't have to type them again.
<br>

### [Git Credential Manager:](#git_credential_manager-gcm)
  - Git `Credential_Manager` (GCM) securely stores your credentials using your `System’s Secure_Storage` (like `Windows_Credential_Manager` or `macOS Keychain`).
  - It encrypts and manages your **Git_Credentials** safely, allowing you to stay logged in without manually entering them again.
<br>

---
<br>

## Git_Cache:
### What is Git_Credential_Cache or Git_Cache ?
- Git `Cache` temporarily stores your **GitHub (or other Git server) Credentials** in **Memory (RAM)** so you don’t have to re-enter them repeatedly during short sessions.
- If you push again within the `Cache_Timeout Window`, you won't be asked again for **Credentials**. After the `Cache_Timeout` expires or you close the **Terminal**, the `Cache` is cleared.
- **By Default** the **`Cache_Timeout`** is **`15 Minutes`**.
- It is also known as `credenital-cache` helper in **Git**.
- **`NOTE:`** **This method is DEPRECATED and NOT USED ANYMORE as better and secured options are available.**
<br>

### How to Use Git_Credential_Cache ? 
- Open your Terminal or Command Prompt.
- Initialize changes to your files and **COMMIT** them.<br>
  ![git add .>>git commit -m "Test Commit 1.0"](https://github.com/user-attachments/assets/a9d38e1d-f533-4cdc-9d6c-0783dc4a9901)
  <br>
- Before **PUSH**ing the changes, paste the following command in your **Terminal:**
  ```
  git config credential.helper cache
  ```
- Now, **PUSH** the **COMMITs** using the following command:
  ```
  git push -u origin main
  ```
  `Note:` Replace `main` with your `BRANCH_NAME` to avoid any errors. [`Learn more about Branches`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Branches.md)
  <br>
- <br>
    ![gh auth login](https://github.com/user-attachments/assets/6d5c76f3-c055-4756-872d-a1b5cf4bb141)
    <br>
  - Copy the **`8-Digit Alpha-Numeric CODE`** under `First copy your one-time code:` >> **`Press Enter`** to proceed to the Sign In webpage.<br>
    ![gh auth login >> Redirect_to_GitHub_SignIn](https://github.com/user-attachments/assets/4281cdcf-2c4c-4409-9be0-2a24282cf6ce)
    <br>
  - Enter your `GitHub Username` and `Password`.<br>
    ![GitHub_SignIn](https://github.com/user-attachments/assets/5b560390-fbfb-4380-b0bb-1313b72782a3)
    <br> Replace **`GITHUB USERNAME / EMAIL ID`** with **`Your Github Username`** or **`Your Github_Email Account`**.
  - Enter the `8-Digit Alpha-Numeric CODE` copied from your Terminal<br>   
    ![GitHub_SignIn>>Enter_Authentication_CODE](https://github.com/user-attachments/assets/2583347d-7fd9-4445-99bd-15e2c9cc297f)
    <br>
  - Enter `Authorize GitHub` to grant permission for the GitHub CLI to access your account.<br>
    ![GitHub_SignIn>>Authorize GitHub for GitHub_CLI](https://github.com/user-attachments/assets/96c1ae6e-5b00-4742-848e-c9facda86cdf)
    <br>
  - An `Authorization-Success-Widget` will be displayed.<br>
    ![GitHub_Auth_Success](https://github.com/user-attachments/assets/83687506-019b-46a8-97dc-910e05db4c9c)
    <br>
  - Return to Terminal.<br>
    ![gh auth login>>success](https://github.com/user-attachments/assets/a2627600-78f9-4302-953c-7bcd07bd031d)
    <br>
<br>

---
<br>

## Git_Store:
<br>

---
<br>

## Git_Credential_Manager (GCM):
<br>

---
