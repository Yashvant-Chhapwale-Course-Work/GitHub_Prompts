# Initialize_Commit_&_Push
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                  |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1 .  **What are `Unstaged_Chnages`?**                                                                           | >> [` CHECK CONTENT `](#what-are-unstaged_changes-)                                           |
| 2 .  **Initializing & `Staging` the `Unstaged_Changes`**                                                        | >> [` CHECK CONTENT `](#staging-modifications)                                                |
| 3 .  **`Unstaging` the `Staged_Changes`**                                                                       | >> [` CHECK CONTENT `](#unstaging-the-staged_modifications)                                   |
| 4 .  **`Commit` the `Staged_Changes`**                                                                          | >> [` CHECK CONTENT `](#commit-the-staged_modifications)                                      |
| 5 .  **`Pushing` the `Commits`**                                                                                | >> [` CHECK CONTENT `](#pushing-commits-to-the-remote_repository)                             |
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

## Staging Modifications
- `Staging` refers to the process of `Adding Modified_Files` to the `Staging_Area` in **Git**, preparing them to be included in the next `COMMIT`.
- The `Staging_Area` in **Git** is an `Intermediate_Space` where changes are gathered before `COMMITing` them to the `Remote_Repository`. It allows you to **review** and **organize** which **specific modifications** you want to include in the next `COMMIT`. 
- This step is done using the `git add` **Command**, which allows you to **selectively** decide which **Modifications** should be recorded in the `Version_History`.
<br>

### Staging Specific Files:
- Open your `Terminal`.
- You can `Stage` a **Specific Modified_File** using the following **Command**:
  ```
  git add FILENAME
  ```
  `Note:` Replace `FILENAME` with the `Modified File's Name`.
  ![git add FILENAME](https://github.com/user-attachments/assets/8968b76f-fede-4570-866a-c5070409e633)<br>
<br>

### Staging All Modifications:
- Open your `Terminal`.
- You can `Stage` all **Modifications** using the following **Command**:
  ```
  git add .
  ```
  `Note:` The `.` refers to all `Modified_Files` in the `Current Directory` and its `SubDirectories`.
  ![git add .](https://github.com/user-attachments/assets/95236627-7eae-48c5-88dd-59db93b9a06b)<br>
<br>

### Staging Modifications Using VS_Code Source_Control Tool:
- Open the `Source_Control Tool` in `VS_Code`.
- Under the `Changes_Section`, you will see a **List of Files** that have been `Modified` but remain `Unstaged`.
- **Click** on the `+` Icon on the **Right_Side** of any `Listed Modified_File` to `Stage Changes` to that **File**.<br>
  ![VS_Code Source_Control >> Stage Changes (`+`)](https://github.com/user-attachments/assets/bf5badcd-8f6d-47a9-8713-109f6e0d7d3e)<br>
  <div align="center"> 
 
     **OR**
  </div>  

  **Click** on the `+` Icon at the **Top** of the `Changes_List` in the `Changes_Section` to `Stage all Changes`.<br>
  ![VS_Code Source_Control >> Stage all Changes (`+`)](https://github.com/user-attachments/assets/ee5db5fe-5861-4847-ac94-d38e1fbf110d)<br>
- After `Staging` the `Modified_Files` they will appear under the `Staged Changes _ Section` as follows:<br>
  ![VS_Code Source_Control >> Staged Changes _ Section](https://github.com/user-attachments/assets/7849e88d-5364-448b-a959-a950e052100a)<br>
<br>

---
<br>

## Unstaging the Staged_Modifications
- `Unstaging` the `Staged_Modifications` refers to the process of **Removing Changes** from the **Git** `Staging_Area` while keeping those changes **intact** in the `Working Directory`.
- This allows you to **Continue Editing or Selectively Stage Files** again later without Losing any Changes.
- It simply **Removes** Files from the `Staging_Area`, so they **won’t be included** in the next `COMMIT` unless `Staged` again.
<br>

### Unstaging a Specific Staged_File:
- Open your `Terminal`.
- You can `Unstage` a **Specific File** from the `Staging_Area` using the following **Command**:
  ```
  git restore --staged FILENAME
  ```
  `Note:` Replace `FILENAME` with the `Staged File's Name` which you want to `Unstage`.<br>
  The `--staged` **Flag** is used for **Targeting** Specific Files that are currently in the `Staging_Area`.
  ![git restore --staged FILENAME](https://github.com/user-attachments/assets/3c9900bc-9412-48f3-aad2-04095e4616f0)<br>
<br>

### Unstaging All Staged_Files:
- Open your `Terminal`.
- You can `Unstage` all/multiple **Files** from the `Staging_Area` using the following **Command**:
  ```
  git restore --staged .
  ```
  `Note:` The `.` refers to all `Staged_Files` in the **Git's** `Staging_Area` for `Current_Repository`.<br>
  The `--staged` **Flag** is used for **Targeting** Files that are currently in the `Staging_Area`.
  ![git restore --staged .](https://github.com/user-attachments/assets/0f8b6499-0851-42b4-93d6-c7526405e831)<br>
<br>

### Unstaging Files Using VS_Code Source_Control Tool:
- Open the `Source_Control Tool` in `VS_Code`.
- Under the `Staged Changes _ Section`, you will see a **List of Files** that have been `Staged` in the **Git's** `Staging_Area`.
- **Click** on the `-` Icon on the **Right_Side** of any `Listed Staged_File` to `Unstage` that **File**.<br>
  ![VS_Code Source_Control >> Unstage Changes (`-`)](https://github.com/user-attachments/assets/c28ceae4-f053-477f-8f1a-def99814be7c)<br>
  <div align="center"> 
 
     **OR**
  </div>  

  **Click** on the `-` Icon at the **Top** of the `Staged_List` in the `Staged Changes _ Section` to `Unstage all Staged_Files`.<br>
  ![VS_Code Source_Control >> Unstage all Changes (`-`)](https://github.com/user-attachments/assets/ffab2f7d-d4e8-46e6-a9fa-6e4ea6d0963b)<br>
- The `Unstaged_Changes` will now appear back under the `Changes_Section` as follows:<br>
  ![VS_Code Source_Control >> Changes_Section](https://github.com/user-attachments/assets/7ac6cc17-27c0-413f-93ec-77bbfea58833)<br>
<br>
  
---
<br>

## Commit the Staged_Modifications
- A `COMMIT` in **Git** is a **Snapshot** of the `Staged_Changes` at a specific point in time.
- It **Records** the `Staged_Changes` currently present in the **Git** `Staging_Area` into the `Repository’s Commit_History`.
- Note that , only `Staged_Changes` can be included in the `COMMIT`.
<br>

### Commiting the Staged_Changes:
- Open your `Terminal`.
- Use the following **Command** to `COMMIT` the **Files** in the `Staging_Area`:
  ```
  git commit -m "COMMIT_MESSAGE"
  ```
  `Note:` Replace `COMMIT_MESSAGE` with an **appropriate** `Title / Message` to identify each `COMMIT`.<br>
  ![git add hello.txt >> git commit -m "Demo Commit"](https://github.com/user-attachments/assets/5059a791-bfd6-424f-a136-ac672a28d45d)<br>
  <div align="center"> 
 
     **OR**
  </div> 

  ![git add . >> git commit -m "Demo Commit"](https://github.com/user-attachments/assets/a5ed2a7d-d7ab-4874-9cbb-3e0e0c048cb4)<br>
  <br>
<br>

### Commiting the Staged_Changes Using VS_Code Source_Control Tool:
- Open the `Source_Control Tool` in `VS_Code`.
- Enter a `"COMMIT_MESSAGE"` in the `Input Box` and Click the `✔ Commit` Button to `COMMIT` the **Files** listed under the `Staged Changes _ Section`.<br>
  ![VS_Code Source_Control >> Enter `COMMIT MESSAGE` >> Click `✔ Commit` Button](https://github.com/user-attachments/assets/54724371-c840-48e7-b791-c3df343c365e)<br>
- The `Staged_Changes` have been `Recorded / Commited` successfully!
<br>
  
---
<br>

## Pushing Commits to the Remote_Repository

- `PUSH` is a **Git_Operation** that Uploads your `Local_Commits` from your `Local_System` to a `Remote_Repository`.
- This ensures that the `Remote_version of the Project` is **up-to-date** with your **Latest Changes**.
<br>

### Pushing Local_Commits:
- Open your `Terminal`.
- **Use the following **Commands** to `PUSH` the `Local_Commits` to the `Remote_Repository`:**<br>
  Use this **Command** if the `Remote_Tracking Branch` is not Set and you need to **define** it. This **Command** is generally used for `Pushing the First Commit` from a `Local_Repository` to a `Remote_Repository`. 
  ```
  git push -u origin main
  ```
  <div align="center"> 
 
     **OR**
  </div> 

  ```
  git push -u origin main --force
  ```
  `Note:` 
  - The `-u` **Flag** is shorthand for `--set-upstream`. It is used to **Set** the `Remote_Branch` that your `LOCAL_BRANCH` is **Tracking**.<br>
  - It tells `Git`:
    - Where to `pull from` when you **Run** `git pull`.
    - Where to `push to` when you **Run** `git push`.<br>
  - The `origin` refers to the `Remote_Repository` where the `Remote_Branch` is to be **Established**.<br>
  - [**`Learn more about Git_Branches`**](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Branches.md).
  - The `--force`flag **Forces** the `PUSH`, even if it **overwrites changes** on the `Remote Branch`. Use it **Cautiously** and Only if you are **sure** about the **Content** being `PUSHed`.<br>
 ![git push -u origin main](https://github.com/user-attachments/assets/56d8424e-edcf-4d71-83b6-dea2ef50d353)<br>
   <div align="center"> 
 
     **OR**
  </div> 
  <br>
  
  Use this **Command** if the `Remote_Tracking Branch` is already **defined** for and **tracked** by the `Local_Repository` (specifically, `Current Local_Branch`).
  ```
  git push
  ```
  ![git add hello.txt >> git commit -m "Demo Commit" >> git push](https://github.com/user-attachments/assets/91ca65da-9130-4520-8b4f-ce96819eca23)<br>
  <div align="center"> 
 
     **OR**
  </div> 

  ![git add . >> git commit -m "Demo Commit" >> git push](https://github.com/user-attachments/assets/9d2f32ba-f140-4cfc-bb99-573c197f68b1)<br>
  <br>
<br>

### Pushing the Commits Using VS_Code Source_Control Tool:
- Open the `Source_Control Tool` in `VS_Code`.
- Click the `↻ Sync Changes` Button to `PUSH` the `Local_Commits` to the `Remote_Repository`.<br>
  ![VS_Code Source_Control >> Enter `COMMIT MESSAGE` >> Click `✔ Commit` Button >> Click `↻ Sync Changes` Button](https://github.com/user-attachments/assets/db250dd5-29c8-45f8-8bf3-94d06e6deb74)<br>
- You can track the `PUSHed COMMITs` through the `Graph / Commit_Tree` displayed at the **Bottom** of the `VS_Code Source_Control Tool`.
  ![VS_Code Source_Control Tool >> Graph / Commit_Tree](https://github.com/user-attachments/assets/c0bbc6a5-ba9c-4c01-ace6-8b6f1a90b879)<br>
<br>
  
---
<br>

