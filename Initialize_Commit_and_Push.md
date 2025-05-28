# Initialize_Commit_&_Push
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                  |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1 .  **What are `Unstaged_Chnages`?**                                                                           | >> [` CHECK CONTENT `](#what-are-unstaged_changes-)                                           |
| 2 .  **Initializing & `Staging` the `Unstaged_Changes`**                                                        | >> [` CHECK CONTENT `](#staging-modifications)                                                |
</div>

---
<br>

## What are Unstaged_Changes ?
- `Unstaged_Changes` are **modifications** made to `Tracked_Files` in the `Working _Directory` that have **not yet been added** to the `Staging_Area` in **Git**.
- These **Changes** are detected by **Git** but will not be included in the next `COMMIT` unless **explicitly** `Staged` using the `git add` **Command**.
- You can **Check** for `Unstaged_Changes` using the following **Command**:
  ```
  git status
  ```
  ![git status >> Unstaged_Changes](https://github.com/user-attachments/assets/c21662d9-409b-4a2a-843a-67089d28343e)<br>
- The `VS_Code Source_Control` **Tool** can also be used to **Track** `Unstaged_Changes`. It indicates `Unstaged_Changes` with the letter `M`, which stands for `Modified`.
  ![VS_Code >> Source_Control >> M (Modified_Changes)](https://github.com/user-attachments/assets/6cec22fc-864f-4542-8a78-d76da921f7ce)<br>
<br>

---
<br>

## Staging Modifications:
- `Staging` refers to the process of `Adding Modified_Files` to the `Staging_Area` in **Git**, preparing them to be included in the next `COMMIT`.
- The `Staging_Area` in **Git** is an `Intermediate_Space` where changes are gathered before `COMMITing` them to the `Remote_Repository`. It allows you to **review** and **organize** which **specific modifications** you want to include in the next `COMMIT`. 
- This step is done using the `git add` **Command**, which allows you to **selectively** decide which **Modifications** should be recorded in the `Version_History`.
<br>

### Staging Specific Files
- Open your `Terminal`.
- You can `Stage` a **Specific Modified_File** using the following **Command**:
  ```
  git add FILENAME
  ```
  `Note:` Replace `FILENAME` with the `Modified File's Name`.
  ![git add FILENAME](https://github.com/user-attachments/assets/8968b76f-fede-4570-866a-c5070409e633)
<br>

### Staging All Modifications
- Open your `Terminal`.
- You can `Stage` all **Modifications** using the following **Command**:
  ```
  git add .
  ```
  ![git add .](https://github.com/user-attachments/assets/95236627-7eae-48c5-88dd-59db93b9a06b)
<br>

### Staging Modifications using VS_Code
- Navigate to the `VS_Code Source_Control` **Tool**.
- 
<div align="center"> 
 
   **OR**
</div>

---
<br>

