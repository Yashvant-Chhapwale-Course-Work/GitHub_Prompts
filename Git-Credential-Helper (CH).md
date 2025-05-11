# Git-Credential-Helper (CH)
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                        |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1. **An Overview `Credential-Helper (CH)`**                                                                     | >> [` CHECK CONTENT `](#what-is-a-credential_helper-ch)                                             |
| 2. **Set / Switch_Between `Credential-Helpers (CHs)`**                                                          | >> [` CHECK CONTENT `](#set--switch_between-credential_helpers-chs)                                 |
| 3. **Unset / Remove `Credential-Helpers (CHs)`**                                                                | >> [` CHECK CONTENT `](#unset--remove-credential_helpers-chs)                                       |
| 4. **Git `Cache`**                                                                                              | >> [` CHECK CONTENT `](#git_cache)                                                                  |
| 5. **Git `Store`**                                                                                              | >> [` CHECK CONTENT `](#git_store)                                                                  |
| 6. **Git `Credential-Manager` (GCM)**                                                                           | >> [` CHECK CONTENT `](#git_credential_manager-gcm)                                                 |
| 7. **Git `Credential-Manager-Core` (GCM Core or GCMC)**                                                         | >> [` CHECK CONTENT `](#git_credential_manager_core-gcm-core-or-gcmc)                               |

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
  - [`manager-core`](#git_credential_manager_core-gcm-core-or-gcmc)
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

## Set / Switch_Between Credential_Helpers (CHs):
###  Credential Helper Scope:
- Git `Credential_Helper (CH)` mainly supports two **Configuration_Scopes**:
  - **Global (`--global`)**
  - **Local (` no flag, --global ❌`)**
  - **System-Level**
<br>

- **`Global (--global):`**
  - This **Scope** is used with git config to **Set**, **View**, or **Unset** the `Credential_Helper (CH)` for all **Git_Repositories** under your **User_Account**.
  - `Global Settings` are stored in `~/.gitconfig` or `C:/Users/USERNAME/.gitconfig` file.<br>
    ![~/.gitconfig](https://github.com/user-attachments/assets/dfd1af82-fd40-48ad-8700-bfb156954c45)<br>
<br>

- **`Local (no flag, --global ❌):`**
  - This **Scope** is used to **Set**, **View**, or **Unset** the `Credential_Helper (CH)` for the **Current Git_Repository** only.
  - `Local Settings` are stored in the **Repository's** `.git/config` file.<br>
    ![.git/config](https://github.com/user-attachments/assets/cb2b571e-3a54-46b9-bad6-2aac95c48a4b)<br>
  - The `.git` folder is **usually** `Hidden`. To **View** or **Access** it, follow these **Steps**:<br>
    ➤ 
    You can use the following **Command** in your `Terminal` to **Verify** the `Hidden` Files for a `Specific_Repository`:
    ```
    ls -hidden
    ```
    ![ls -hidden](https://github.com/user-attachments/assets/9386d27e-7029-4338-872a-d90aa5ccede7)<br>
    Then, use the following **Commands** in your `Terminal` to access the **hidden** `.git` Folder:
    ```
    cd .git
    ls
    ```
    ➤ Then `Hold Ctrl + Left_Click` on the `config` file **listed** by the `ls` **Command**.<br>
    ![cd .git >> ls](https://github.com/user-attachments/assets/dc14ddbd-2c4b-466c-b4d9-93e7d90a62ac)<br>
    ➤ This **action** opens the `config` file, where you can view the `Current_Repository's` **Settings**, including its **Configuration** for **Remotes, Branches, and other Git-Specific options**.<br>
    ![`config` file](https://github.com/user-attachments/assets/147850fb-915f-4a5f-87f9-d7e2dd1b48fc)<br>
<br>

- **`System-Level:`**
  - This **Scope** refers to **Configurations** that apply to **All Users** in a **System**, unlike the `--global` **Scope** which applies only to the `Current User_Account` across all their **Git_Repositories**.
  - `System Git_Configurations` are typically stored  in `C:\Program Files\Git\etc\gitconfig` file.<br>
    ![etc\gitconfig](https://github.com/user-attachments/assets/03c2ca4f-6452-48e7-b6d3-c09f8cf0c579)<br>
<br>


### How to Set / Switch_Between Credential_Helpers ?
- Use the following **Command** in your `Terminal` to `Set` / `Switch_Between` different `Credential_Helpers (CHs)`:<br>
  ➤ For **Specific Repository**:
  ```
  git config credential.helper <HELPER-NAME>
  ```
  **`NOTE:`** **Switch** the `HELPER-NAME` with one of the **available** `Credential_Helper Options` (`cache`, `store`, `manager`, `manager-core`)<br>
  ![git config credential.helper manager](https://github.com/user-attachments/assets/4977872e-df25-4135-a4b1-f9cbeaa8403e)<br>
  <br>
  
  ➤ To **Configure** a `Credential_Helper` for all your **Git_Repositories** (`--global`):
  ```
  git config --global credential.helper <HELPER-NAME>
  ```
  **`NOTE:`** **Switch** the `HELPER-NAME` with one of the **available** `Credential_Helper Options` (`cache`, `store`, `manager`, `manager-core`)<br>
  ![git config --global credential.helper manager-core](https://github.com/user-attachments/assets/f4908aab-3436-4540-863f-56929ff43f0f)<br>
  <br>
  
  ➤ To **Configure** a `Credential_Helper` for **All Users** in a **System**:<br>
  ```
  git config --system credential.helper <HELPER-NAME>
  ```
  **`NOTE:`** **Switch** the `HELPER-NAME` with one of the **available** `Credential_Helper Options` (`cache`, `store`, `manager`, `manager-core`)<br>
  ![git config --system credential.helper manager](https://github.com/user-attachments/assets/afb5d82c-0f00-4fd4-9b99-d963815f2ac2)<br>
  **`NOTE:`** To execute this command, **Right-Click on `Command_Prompt (cmd) / Terminal`** and **Select `Run as administrator`** before running it as you require `Administrative Privileges` for `System-Level` **Scope**.<br>
  ![CMD >> Run as administrator](https://github.com/user-attachments/assets/6330e372-c422-4b71-976e-6b60c8327b10)<br>
<br>


### How to View Configured Git Credential_Helpers (CHs) ?
- Use the following **Command** to **View** the `Local Credential_Helper` i.e, `Credential_Helper` for **Current_Repository**:
  ```
  git config credential.helper
  ```
  ![git config credential.helper](https://github.com/user-attachments/assets/db5106df-a21a-4571-9a7a-c01aa8e2f179)<br>
- Use the following **Command** to **View** the `Global Credential_Helper`:
  ```
  git config --global credential.helper
  ```
  ![git config --global credential.helper](https://github.com/user-attachments/assets/232f9b2a-be19-4e83-9b1d-fa797bf113cf)<br>
- Use the following **Command** to **View** the `System-Level Credential_Helper` **(For Windows)**:
  ```
  git config --system credential.helper
  ```
  `Note:` This **Command** reads from the `System Git_Configuration (.gitconfig)` File, typically under `C:/Program Files/Git/etc/gitconfig`.<br>
  ![git config --system credential.helper](https://github.com/user-attachments/assets/754ce668-c649-46b6-9ca9-76e45de27597)<br>
- Use the following **Command** to **View** the `Credential_Helper Configuration at all Levels (Scopes)` **(For Windows)**:
  ```
  git config --list --show-origin | findstr credential.helper
  ```
  `Note:` The `--show-origin` Flag in `Git` is used with `git config . . .` to display where each **Configuration Value** is **defined** i.e., the **File** in which the **Configuration** is **stored**.<br>
  ![git config --list --show-origin | findstr credential.helper](https://github.com/user-attachments/assets/7c71157a-9a60-4308-b3cf-5746b6cf3e96)<br>
<br>

---
<br>

## Unset / Remove Credential_Helpers (CHs):
### How to Unset Credential_Helpers at various Levels of Scope ?
- To **Delete** a **previously configured** `Credential_Helper (CH)` from the specified **Git_Configuration Scope**, we use the `--unset` Flag. 
- Use the following **Command** in your `Terminal` to `Unset` the `Local Credential_Helper (CH)`:
  ```
  git config --unset credential.helper
  ```
- Use the following **Command** in your `Terminal` to `Unset` the `Global Credential_Helper (CH)`:
  ```
  git config --global --unset credential.helper
  ```
- Use the following **Command** in your `Terminal` to `Unset` the `System-Level Credential_Helper (CH)`:
  ```
  git config --system --unset credential.helper
  ```
  `Note:` The `--system` Flag modifies the `System-Level Git_Configuration`, which requires **Administrative Privileges**.<br>
  To execute this command, **Right-Click on `Command_Prompt (cmd) / Terminal`** and **Select `Run as administrator`** before running it.<br>
  ![CMD >> Run as administrator](https://github.com/user-attachments/assets/6330e372-c422-4b71-976e-6b60c8327b10)<br>
  Without **Administrative Privileges** the **Command** returns **`Error`** as follows:<br>
  ![`--system --unset` Error](https://github.com/user-attachments/assets/4f027592-b347-4767-9434-260e5a18475c)<br>
- To **Confirm** whether the `Credential_Helpers (CHs)` have been successfully removed, run the following **Command** in your `Terminal`:
  ```
  git config --list --show-origin | findstr credential.helper
  ```
  ![git config --unset](https://github.com/user-attachments/assets/4e469630-3304-4d6f-b05e-f1d1cc2ace49)<br>
  If this **Command** gives **No Output**, as shown above, it means the `Credential_Helper (CH)` is not **Set** at any **Level** (`local`, `global`, or `system`) — so it has been successfully **Unset**.
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
  git config credential.helper 'cache --timeout=3600'
  ```
  `NOTE:` This command sets the `Timeout` to `1hr i.e, 3600sec`. Similarly, the `Timeout` can be adjusted to `15min i.e, 90sec`, `2hr i.e, 7200sec`, etc.
<br>

### How to Update or Reset Credentials in Git_Cache ?
- There is **no direct** `Git_Command` to **clear** the `Cache`, but the `Cache` **expires automatically** after the `Timeout`.
- You can either **Wait** for `Git_Cache` to `Timeout` or Use the following Command to manually `Timeout` the `Cache`:
  ```
  git config --global credential.helper 'cache --timeout=30'
  ```
- This will **reset** the `Timeout` to `30sec`, after which the `Cache` will forget the credentials, then repeat the Steps for [**Setting Credentials in `Git_Cache`**](#how-to-use-git_credential_cache-).
- Don't Forget to reset the `Timeout` from `30sec` or the **Updated Credentials** will also **expire** after **30 seconds** pass.<br>
  Use the following Command to **Reset** the `Timeout` to **Default**:
  ```
  git config --global credential.helper 'cache --timeout=90'
  ```
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
- **By Default** the **`Credentials`** are stored at `C:/Users/USERNAME/.git-credentials` or `~/.git-credentials`.
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
  `Git_Store` saves the **Credentials** at `C:\Users\USERNAME\.git-credentials`. You can also **Save** your **Credentials** in a [`Custom Directory`](#how-to-set-a-custom-directory-for-git_credential_store-) of your choice.
  ![~\.git-credentials](https://github.com/user-attachments/assets/e480a6be-61d8-4461-97b2-cd98d67f3185)<br>
  **`FORMAT`** for **Credentials** stored in `.git-credentials` file:
  ```
  https://USERNAME:PAT@github.com
  ```
- To **Verify** whether `Git_Store` is working, **Logout** of your **GitHub Account** from `gh_CLI` as well as `VS_Code` (If Signed_In) and **PUSH** a Demo_Commit as follows:  
  ![VS_Code>>GitHub>>Sign Out](https://github.com/user-attachments/assets/33af3792-0f3f-4a47-8ad7-77341fba9497)<br>
  ![gh auth logout](https://github.com/user-attachments/assets/f8489fd9-4831-4771-85b2-6f3492d471e8)<br>
  ![Test Commit 2.1>>git push -u origin main](https://github.com/user-attachments/assets/39a28051-be22-4a4d-b90c-88949172e8bf)<br>
- As Observed, the `PUSH` Operation is carried out successfully even when GitHub was not Authenticated, also it  
  did not ask for the Credentials again.
  <br>
  
  **Hence, we have successfully implemented `Git_Credential_Store`!**
<br>


### How to Set a Custom Directory for Git_Credential_Store ?
- **By Default** the **`Credentials`** are stored at `C:/Users/USERNAME/.git-credentials` or `~/.git-credentials`.
- We can use the following **Command** to **Specify** the `Location` for `Git_Credential_Store File`**:** 
  ```
  git config credential.helper "store --file=PATH:/TO/CUSTOM/GIT-STORE_CREDENTIAL_FILE"
  ```
- Again, **STAGE** a **Demo_COMMIT** and **PUSH** them to the Remote_Repository.
- As the **PATH** for `Git_Store_File` was **Updated** you will be asked to,
  Enter your `GitHub_USERNAME` and `Repository Personal_Access_Token (PAT)` as shown:
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
- Once the **Authentication** is completed, `Git_Store` stores the credentials at the `New_Custom_File_Path` and completes the `PUSH` Operation.    
  ![Test Commit 2.2>>git push -u origin main](https://github.com/user-attachments/assets/36656527-358b-43ee-b0e7-6a6d8813c479)<br>
  ![~/.my-git-credentials](https://github.com/user-attachments/assets/66821fb3-a4d5-443a-bbe7-f71fea827069)<br>
- To **Verify** whether `Git_Store` is working, **Logout** of your **GitHub Account** from `gh_CLI` as well as `VS_Code` (If Signed_In).
  ![VS_Code>>GitHub>>Sign Out](https://github.com/user-attachments/assets/33af3792-0f3f-4a47-8ad7-77341fba9497)<br>
  ![gh auth logout](https://github.com/user-attachments/assets/f8489fd9-4831-4771-85b2-6f3492d471e8)<br>
  Also, **Remove** the Older `Credential_Store_Files` (like `.git-credentials`) by using the following **Command:**
  ```
  rm C:/Users/USERNAME/.git-credentials
  ```
  `Note:` Use **Caution** with this Step, as Older `Credential_Store_Files` (such as `.git-credentials`) may be Configured as `--global` and **shared** across **Multiple Repositories**.
  <div align="center">
   
   **OR**</div>
  ```
  rm ~/.git-credentials
  ```
  `Note:` Use **Caution** with this Step, as Older `Credential_Store_Files` (such as `.git-credentials`) may be Configured as `--global` and **shared** across **Multiple Repositories**.<br>
  After performing the above Step, **PUSH** a **Demo_COMMIT** and Observe:
  ![Test Commit 2.3>>git push -u origin main](https://github.com/user-attachments/assets/b409ed8c-3a58-4e38-9497-82fa3c91d648)
- If the `PUSH` Operation is performed successfully without asking for **Credentials** again, then we can assume that `Git_Store` has successfully recognised the `New_Custom_File_Path`. 
<br>

### How to Update Credentials Stored in Git_Credential_Store:
- First, **Remove** the Credentials stored by `Git_Store` at the specified **PATH** using the following Command:
  ```
  rm PATH:/TO/.credential-file
  ```
  By **Default**, `Git_Store` saves Credentials at `C:/Users/USERNAME/.git-credentials` or `~/.git-credentials`. In this case use the following Command:
  ```
  rm ~/.git-credentials
  ```
- Once the `Credential_File` has been removed, repeat the steps for [**Setting Credentials in `Git_Store`**](#how-to-use-git_credential_store-). 
<br>

### Advantages:
- `Credentials` are stored **Locally**, requiring **No Network Authentication** each time.
- `Git_Store` provides `Cross-Platform Support` i.e, it works **consistently** across `Windows`, `macOS`, and `Linux`.
- It supports specifying a `Custom_Path` for `Credential_Storage`.
<br>

### Disadvantages:
- `Credentials` are saved in `Plain_Text` & `Unencrypted` Format, posing a **Security Risk**.
- Once `Personal Access Tokens` expire, they must be updated manually or the `Authentication` might **Fail**.
<br>

---
<br>

## Git_Credential_Manager (GCM):
### What is Git_Credential_Manager or GCM ?
- `Git_Credential_Manager (GCM)` is the **Older Version** of the `Git_Credential_Manager_Core` **Helper** designed specifically for `Windows`.
- It integrates with the `System's Secure_Storage` i.e, `Windows_Credential_Manager` in `Windows` for storing your **Credentials**.
- It is also simply called as the `manager` **Helper**.
- Now-a-days, the `manager` helper is no longer maintained as it is being replaced by `Git_Credential_Manager_Core (i.e, manager-core)` which provides **Cross_Platform Support** and is **Compatible with Modern Authentication Methods**.
- If you stay on `manager`, it will still work, but you may hit **compatibility issues** with **Modern Authentication** in the **Future**.
<br>

### How to Use Git_Credential_Manager or GCM ? 
- Open your Terminal or Command Prompt.
- Initialize changes to your files and **COMMIT** them.<br>
- Before **PUSH**ing the changes, paste the following command in your **Terminal** to enable `Git_Credential_Manager`:
  ```
  git config credential.helper manager
  ```
- Now, **PUSH** the **COMMITs** using the following command:
  ```
  git push -u origin main
  ```
  `Note:` Replace `main` with your `BRANCH_NAME` to avoid any errors. [`Learn more about Branches`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Branches.md)
- A `Git_Prompt` will appear, asking you to **Choose** an **Authentication Method** (Using `Browser/Device` or `Token (i.e, PAT)`):
  ![Git Prompt >> Browser/Device](https://github.com/user-attachments/assets/12dfb7aa-2723-4e83-8a3d-cb09ba701cc2)<br>
  ![Git Prompt >> Token (PAT)](https://github.com/user-attachments/assets/3e857c74-39e7-4035-9dae-8e02c0350b8d)<br>
- 
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
  `Git_Store` saves the **Credentials** at `C:\Users\USERNAME\.git-credentials`. You can also **Save** your **Credentials** in a [`Custom Directory`](#how-to-set-a-custom-directory-for-git_credential_store-) of your choice.
  ![~\.git-credentials](https://github.com/user-attachments/assets/e480a6be-61d8-4461-97b2-cd98d67f3185)<br>
  **`FORMAT`** for **Credentials** stored in `.git-credentials` file:
  ```
  https://USERNAME:PAT@github.com
  ```
- To **Verify** whether `Git_Manager` is working, **Logout** of your **GitHub Account** from `gh_CLI` as well as `VS_Code` (If Signed_In) and **PUSH** a Demo_Commit as follows:  
  ![VS_Code>>GitHub>>Sign Out](https://github.com/user-attachments/assets/33af3792-0f3f-4a47-8ad7-77341fba9497)<br>
  ![gh auth logout](https://github.com/user-attachments/assets/f8489fd9-4831-4771-85b2-6f3492d471e8)<br>
  ![Test Commit 2.1>>git push -u origin main](https://github.com/user-attachments/assets/39a28051-be22-4a4d-b90c-88949172e8bf)<br>
- As Observed, the `PUSH` Operation is carried out successfully even when GitHub was not Authenticated, also it  
  did not ask for the Credentials again.
  <br>
  
  **Hence, we have successfully implemented `Git_Credential_Store`!**
<br>

---
<br>

## Git_Credential_Manager_Core (GCM Core or GCMC):
<br>

---
