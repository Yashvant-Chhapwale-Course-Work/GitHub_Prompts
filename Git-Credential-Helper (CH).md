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
| 5. **Git `Credential-Manager-Core` (GCM Core or GCMC)**                                                         | >> [` CHECK CONTENT `](#git_credential_manager_core-gcm-core-or-gcmc)                               |

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

### [Git Cache:](#git_cache) [NOT RECOMMENDED FOR WINDOWS]
- Git `Cache` is a temporary `Memory-Based` **Credential_Helper** for Git.
- It stores your **Git_Credentials** in `Memory (RAM)` for a **short time**, so you don’t have to type them again during that session.
<br>

### [Git Store:](#git_store)
- Git `Store` saves your credentials in a `Plain-Text` format.
- It stores the **Git_Credentials** in a `Text File`, so that you don't have to type them again.
<br>

### [Git Credential Manager:](#git_credential_manager-gcm) [RECOMMENDED FOR WINDOWS]
- `Git_Credential_Manager (GCM)` was introduced around `2015` for `Windows` to support **Token-Based (OAuth, PAT) Login Flows** instead of just basic Username/Password.
- Git `Credential_Manager` (GCM) securely stores your credentials using your `System’s Secure_Storage` (like `Windows_Credential_Manager`).
- It encrypts and manages your **Git_Credentials** safely, allowing you to stay logged in without manually entering them again.
<br>

### [Git Credential Manager Core:](#git_credential_manager_core-gcm-core-or-gcmc) [RECOMMENDED FOR WINDOWS]
- `Git_Credential_Manager_Core (GCMC)` was introduced in `2020` with **Cross-Platform Support**(like `Windows`, `macOS`, `Linux`, etc).
- It is similar to `Git_Credential_Manager`, but `Git_Credential_Manager_Core` is a **faster, more secure, and actively maintained** with support for modern authentication methods like `OAuth` and `Browser-Based` Login.
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
  ![Test Commit 1.0](https://github.com/user-attachments/assets/a9d38e1d-f533-4cdc-9d6c-0783dc4a9901)
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
- Enter your `GitHub_USERNAME` and `Repository Personal_Access_Token (PAT)` or `PASSWORD` as shown:
  ![Enter USERNAME](https://github.com/user-attachments/assets/85d57f5e-3df9-490b-a356-cf54f1fc98eb)<br>
  ![Enter PAT](https://github.com/user-attachments/assets/42780948-ae0d-4c57-aa47-6e7be53b4f03)<br>
  <div align="center">
   
   **OR**</div>
  A Dialogbox will appear asking permission for authenticating GitHub. Click `Allow` to **Sign In** using GitHub:
  ![Click Allow>>GitHub_Sign In](https://github.com/user-attachments/assets/e7ee6e0f-2123-48a7-b943-4c5c92319952)<br>
  Enter your `GitHub Username` and `PASSWORD` OR `Personal_Access_Token (PAT)`.<br>
  ![GitHub_SignIn](https://github.com/user-attachments/assets/5b560390-fbfb-4380-b0bb-1313b72782a3)<br>
  Replace **`GitHub_USERNAME / EMAIL ID`** with **`Your Github Username`** or **`Your Github_Email Account`**.<br>
- Once the **Authentication** is completed, `Git_Cache` stores the credentials and completes the `PUSH` Operation.    
  ![Test Commit 1.0>>git push -u origin main](https://github.com/user-attachments/assets/7daa9aa9-9e7a-4849-adc3-5c018fed5ee8)
  <br>
  <br>
- To **Verify** whether `Git_Cache` is working, **Logout** of your **GitHub Account** from `gh_CLI` as well as `VS_Code` (If Signed_In) and **PUSH** a Demo_Commit as follows:  
  ![VS_Code>>GitHub>>Sign Out](https://github.com/user-attachments/assets/33af3792-0f3f-4a47-8ad7-77341fba9497)<br>
  ![Test Commit 1.1>>git push -u origin main](https://github.com/user-attachments/assets/d8de196c-31c8-4ad7-9c74-5e224fc966ce)
- As Observed, the `PUSH` Operation is carried out successfully even when GitHub was not Authenticated, also it did not ask for the Credentials again.
  <br>
  
  **Hence, we have successfully implemented `Git_Credential_Cache`!**
<br>

### How to Specify (Increase or Decrease) Timeouts for Git_Cache ?
- **By Default** the **`Cache_Timeout`** is **`15 Minutes`**.
- We can use the following **Command** to **Configure** the `Timeout_Period` for `Git_Credential_Cache`**:** 
  ```
  git config --global credential.helper 'cache --timeout=3600'
  ```
  `NOTE:` This command sets the `Timeout` to `1hr i.e, 3600sec`. Similarly, the `Timeout` can be adjusted to `15min i.e, 90sec`, `2hr i.e, 7200sec`, etc.
<br>

### Advantages:
- Credentials are stored in **RAM** only, not on disk making it **Safer** than `Plain-Text` Storage (i.e `Git_Credential_Store`).
- Useful for **Short-Lived** Tasks as you can **Specify** how long the credentials stay in Memory(i.e, Specify `Timeouts`).
- During the `Timeout_Window`, repeated **Git_Commands** (e.g., `PUSH`, `Fetch`, `Pull`) won't ask for your Credentials again.
- Git cache works **natively** and **reliably** on `Unix`/`Linux`/`macOS` because it uses `Unix Domain Sockets` and spawns a **Local Daemon** automatically.
<br>

### Disadvantages:
- The cache helper was built for `Unix-like Systems`. It **does not Work Properly** on `Windows`, as the `Native_Cache_Daemon` is **Absent** for **Windows**.
- The `Cache_Daemon` stores Credentials only in **RAM**, therefore, once the **`Timeout` Expires, System Reboots, or the Daemon Stops**, you'll be **Prompted** again.
- Unlike `manager-core` or `store`, **Git** will forget credentials after you restart your computer.
<br>

---
<br>

## Git_Store:
### What is Git_Credential_Store or Git_Store ?
- Git `Store` is a **Credential_Helper** that saves your **Git Credentials** in `Plain_Text` on your **Local Disk**, so you don’t need to re-enter them for Future Git_Operations.
- Credentials are **Saved Permanently** and remain available across **sessions** and **reboots**, unlike the Temporary `Credential_Cache` Helper.
- **By Default** the **`Credentials`** are stored at `C:\Users\USERNAME\.git-credentials` or `~/.git-credentials` .
- It is also known as `credenital-store` helper in **Git**.
- **`NOTE:`** **It is mandatory to use a `Personal Access Token (PAT)` instead of your account password for `Git_Store`, as GitHub no longer supports password-based authentication.**
- **`NOTE:`** **This method is DEPRECATED and NOT USED ANYMORE as better and secured options are available.**
<br>

### How to Use Git_Credential_Store ? 
- Open your Terminal or Command Prompt.
- Initialize changes to your files and **COMMIT** them.<br>
- Before **PUSH**ing the changes, paste the following command in your **Terminal** to enable `Git_Credential_Store`:
  ```
  git config credential.helper store
  ```
- Now, **PUSH** the **COMMITs** using the following command:
  ```
  git push -u origin main
  ```
  `Note:` Replace `main` with your `BRANCH_NAME` to avoid any errors. [`Learn more about Branches`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Branches.md)
  ![Test Commit 2.0](https://github.com/user-attachments/assets/47bdc2f0-b03b-4fa1-a06d-3f5df2385c73)<br>
- Enter your `GitHub_USERNAME` and `Repository Personal_Access_Token (PAT)` as shown:
  ![Enter USERNAME](https://github.com/user-attachments/assets/85d57f5e-3df9-490b-a356-cf54f1fc98eb)<br>
  ![Enter PAT](https://github.com/user-attachments/assets/42780948-ae0d-4c57-aa47-6e7be53b4f03)<br>
  `Note:` It is mandatory to use a `Personal Access Token (PAT)` instead of your **account password** for `Git_Store`, as GitHub no longer supports **password-based authentication**.
  <div align="center">
   
   **OR**</div>
  A Dialogbox will appear asking permission for authenticating GitHub. Click `Allow` to **Sign In** using GitHub:
  ![Click Allow>>GitHub_Sign In](https://github.com/user-attachments/assets/e7ee6e0f-2123-48a7-b943-4c5c92319952)<br>
  Enter your `GitHub Username` and `Personal_Access_Token (PAT)`.<br>
  ![GitHub_SignIn](https://github.com/user-attachments/assets/f18fff08-2bc5-425f-9a3a-e16d2f2bf99a)<br>
  Replace **`GitHub_USERNAME / EMAIL ID`** with **`Your Github Username`** or **`Your Github_Email Account`**.<br>
  `Note:` It is mandatory to use a `Personal Access Token (PAT)` instead of your **account password** for `Git_Store`, as GitHub no longer supports **password-based authentication**.
- Once the **Authentication** is completed, `Git_Store` stores the credentials in `.git-credentials` File and completes the `PUSH` Operation.    
  ![Test_Commit_2.0>>git push -u origin main](https://github.com/user-attachments/assets/3af01a4b-9bab-4afd-ba90-461cf6e9f0b1)<br>
  `Git_Store` saves the **Credentials** at `C:\Users\USERNAME\.git-credentials`
  ![~\.git-credentials](https://github.com/user-attachments/assets/e480a6be-61d8-4461-97b2-cd98d67f3185)<br>
- To **Verify** whether `Git_Cache` is working, **Logout** of your **GitHub Account** from `gh_CLI` as well as `VS_Code` (If Signed_In) and **PUSH** a Demo_Commit as follows:  
  ![VS_Code>>GitHub>>Sign Out](https://github.com/user-attachments/assets/33af3792-0f3f-4a47-8ad7-77341fba9497)<br>
  ![Test Commit 2.1>>git push -u origin main](https://github.com/user-attachments/assets/39a28051-be22-4a4d-b90c-88949172e8bf)<br>
- As Observed, the `PUSH` Operation is carried out successfully even when GitHub was not Authenticated, also it  
  did not ask for the Credentials again.
  <br>
  
  **Hence, we have successfully implemented `Git_Credential_Store`!**
<br>

### How to Specify (Increase or Decrease) Timeouts for Git_Cache ?
- **By Default** the **`Cache_Timeout`** is **`15 Minutes`**.
- We can use the following **Command** to **Configure** the `Timeout_Period` for `Git_Credential_Cache`**:** 
  ```
  git config --global credential.helper 'cache --timeout=3600'
  ```
  `NOTE:` This command sets the `Timeout` to `1hr i.e, 3600sec`. Similarly, the `Timeout` can be adjusted to `15min i.e, 90sec`, `2hr i.e, 7200sec`, etc.
<br>

### Advantages:
- Credentials are stored in **RAM** only, not on disk making it **Safer** than `Plain-Text` Storage (i.e `Git_Credential_Store`).
- Useful for **Short-Lived** Tasks as you can **Specify** how long the credentials stay in Memory(i.e, Specify `Timeouts`).
- During the `Timeout_Window`, repeated **Git_Commands** (e.g., `PUSH`, `Fetch`, `Pull`) won't ask for your Credentials again.
- Git cache works **natively** and **reliably** on `Unix`/`Linux`/`macOS` because it uses `Unix Domain Sockets` and spawns a **Local Daemon** automatically.
<br>

### Disadvantages:
- The cache helper was built for `Unix-like Systems`. It **does not Work Properly** on `Windows`, as the `Native_Cache_Daemon` is **Absent** for **Windows**.
- The `Cache_Daemon` stores Credentials only in **RAM**, therefore, once the **`Timeout` Expires, System Reboots, or the Daemon Stops**, you'll be **Prompted** again.
- Unlike `manager-core` or `store`, **Git** will forget credentials after you restart your computer.
<br>


---
<br>

## Git_Credential_Manager (GCM):
<br>

---
<br>

## Git_Credential_Manager_Core (GCM Core or GCMC):
<br>

---
