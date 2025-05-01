# Managing Remote_GitHub_Repositories
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **What do we mean by a `Remote_Repository`?**                                                              | >> [` CHECK CONTENT `](#what-do-we-mean-by-a-remote_repository)                               |
| 2.  **Link `Local_Repository` To `Remote_Repository`**                                                         | >> [` CHECK CONTENT `](#link-local_repository-to-remote_repository)                           |
| 3.  **Verify the `Linked` Remote_Repository**                                                                  | >> [` CHECK CONTENT `](#verify-the-linked-remote_repository)                                  |
| 3.  **Create A Repository Using GitHub_Web_Interface**                                                         | >> [` CHECK CONTENT `](#repository-initialization--using-github_website--recommended)         |
| 4.  **Create A Repository Using GitHub_Desktop**                                                               | >> [` CHECK CONTENT `](#repository-initialization--using-github_desktop-)                     |
| 5.  **Create A Repository Using VSCode Source_Control Tool**                                                   | >> [` CHECK CONTENT `](#repository-initialization--using-vscode-source-control-)              |
| 6.  **Remove / Unlink Remote Repository From Local Repository**                                                | >> [` CHECK CONTENT `](#unlink-remote-repository-from-local-repository)                       |
| 6.  **Remove / Unlink `Remote Repository` From `Local Repository`**                                            | >> [` CHECK CONTENT `](#unlink-remote-repository-from-local-repository)                       |
</div>

---
<br>

## What do we mean by a Remote_Repository?
  - A `Remote_Repository` in **Git** is a version of your project that's hosted on the Internet or another Network, typically on a platform like **GitHub**,**GitLab**,etc.
  - Unlike the `Local_Repository` which is on your **Own Device** (ex: **Computer**), the `Remote_Repository` is stored somewhere else — usually on the **Cloud**.
  - Learn how to **Initialize** a `Remote_Repository` from [**`Here`**](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Repo_Initialization.md#repository-initialization--using-github_website--recommended).
<br>

---
<br>

## Link Local_Repository To Remote_Repository
  - Open your **Terminal** or **Command Prompt**.
  - Ensure that the **Terminal** is pointed to the **Correct** `Local_Repository` **Directory**.<br>
    ![Local_Repository_Directory](https://github.com/user-attachments/assets/c8a96d54-ca05-4760-8f5d-3e200f4f4c3d)
  - Copy the `URL` for your `Remote_GitHub_Repository`:<br>
    ![Copy_URL_from_Address_Bar](https://github.com/user-attachments/assets/c7453c89-51af-4bfe-bd31-76d62add8563)
    <br> <div align="center">**OR**</div> <br>
    ![GitHub_Website>>Code<>>>Local>>Copy URL](https://github.com/user-attachments/assets/6484b66b-f33a-404e-b4c2-9b7b2c6d1015)
    <br>
  - Use the following Command in the Terminal to `Link` the `Remote Repository` to your `Local Repository`.
    ```
    git remote add origin https://github.com/USERNAME/REPOSITORY-NAME
    ```
    `Note:` Substitute **'USERNAME'** with your **'GitHub_Username'** and **'REPOSITORY-NAME'** with your **'Remote Repository_Name'** `OR` **PASTE** your `Repository_URL` instead.<br>
  - Verify the **Linked** `Remote_Repository` by following the Steps enlisted [**`Here`**](#verify-the-linked-remote_repository).
<br>

---
<br>

## Verify the Linked Remote_Repository
  - Open your **Terminal** or **Command Prompt**.
  - Use the following Command in the Terminal to **Verify** the `Linked Remote_Repository`.
    ```
    git remote -v
    ```
    ![git remote -v](https://github.com/user-attachments/assets/d8166b6a-b4fb-4e9a-94cd-e08b653d0d9b)
<br>

---
<br>

## Unlink Remote Repository from Local Repository
  - Open your **Terminal** or **Command Prompt**.
  - Paste the following **Command** in the **Terminal:**
    ```
    git remote remove origin
    ```
---
