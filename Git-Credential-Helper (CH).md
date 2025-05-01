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
- Before **PUSH**ing the changes, paste the following command in your **Terminal** to enable `Git_Credential_Cache`:
  ```
  git config credential.helper cache
  ```
- Now, **PUSH** the **COMMITs** using the following command:
  ```
  git push -u origin main
  ```
  `Note:` Replace `main` with your `BRANCH_NAME` to avoid any errors. [`Learn more about Branches`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Branches.md)
  <br>
- A Dialogbox will appear asking permission for authenticating GitHub. Click `Allow` to **Sign In** using GitHub.
  ![Click Allow>>GitHub_Sign In](https://github.com/user-attachments/assets/e7ee6e0f-2123-48a7-b943-4c5c92319952)
- Enter your `GitHub Username` and `Password`.<br>
  ![GitHub_SignIn](https://github.com/user-attachments/assets/5b560390-fbfb-4380-b0bb-1313b72782a3)
  <br> Replace **`GITHUB USERNAME / EMAIL ID`** with **`Your Github Username`** or **`Your Github_Email Account`**.
- Once the **Authentication** is completed, `Git_Cache` stores the credentials and completes the `PUSH` Operation.    
  ![git push -u origin main](https://github.com/user-attachments/assets/7daa9aa9-9e7a-4849-adc3-5c018fed5ee8)
  <br>
  <br>
- To **Verify** whether `Git_Cache` is wotking, **Logout** of your **GitHub Account** from `gh_CLI` as well as `VS_Code` and **PUSH** a Demo_Commit as follows:  
  ![VS_Code>>GitHub Sign Out](https://github.com/user-attachments/assets/9642abf4-4d76-4492-bb7e-8949ecb065ae)<br>
  ![gh auth logout>>git push -u origin main](https://github.com/user-attachments/assets/d8de196c-31c8-4ad7-9c74-5e224fc966ce)
- As Observed, the `PUSH` Operation is carried out successfully even when GitHub was not Authenticated, also it did not ask for the Credentials again.
  <br>
  **Hence, we have successfully implemented `Git_Credential_Cache`!**
<br>

### How to Specify (Increase or Decrease) Timeouts for Git_Cache ?
- 
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
