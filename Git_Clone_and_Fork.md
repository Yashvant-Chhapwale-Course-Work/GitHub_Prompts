# Clone & Fork
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                  |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1 .  **What do we mean by `Cloning` a `Remote_Repository`?**                                                    | [` 🔗CHECK CONTENT `](#what-do-we-mean-by-cloning-a-remote_repository)                       |
| 2 .  **`Cloning` a `Remote_Repository`**                                                                        | [` 🔗CHECK CONTENT `](#cloning-a-remote_repository-to-local_system)                            |
</div>
 
---
<br>

## What do we mean by Cloning a Remote_Repository?
- `Cloning` is the process of **Creating** a `Full_Copy` of a `Remote_Repository` on your `Local_System`.
- This includes all the **Project** `Files`, `Branches`, `Commit_History`, and the `.git_Directory` that **Tracks Changes**.
- In case of a `Public_Repository`, anyone can `CLONE` the `Remote_Repository` and require **No Special Access** (Ex: `Owner`, `Collaborator`, etc).
- For `Private_Repository`, you require **Explicit Permission** to `CLONE` the `Remote_Repository` from the **Owner** or require to be added as a **Collaborator** to the `Remote_Repository`.<br>

<div align="center">

|**Access Level**  | **Can Clone?**  | **Can Push?** | **Can Manage Repo?** |
| ---------------- | --------------- | ------------- | -------------------- |
|**Read**          | ✅ Yes         | ❌ No         | ❌ No               |
| **Write**        | ✅ Yes         | ✅ Yes        | ❌ No               |
| **Admin**        | ✅ Yes         | ✅ Yes        | ✅ Yes              | 
| **Owner** (Org.) | ✅ Yes         | ✅ Yes        | ✅ Yes              |
</div>

---
<br>

## Cloning a Remote_Repository to Local_System
### Cloning a Remote_Repository through Git_CLI:
- Launch the `Terminal` in the **directory** where you want to `Clone` the `Remote_Repository`.
- Use the following **Command** to `CLONE` the `Remote_Repository` at the desired Path:
  ```
  git clone <Remote_Repository_URL> <Local_Folder_Name>
  ```
  `Note:`
  - Replace `<Remote_Repository_URL>` with the URL of the `Remote_Repository`, which you want to `CLONE`.
  - (**Optional**) Replace `<Local_Folder_Name>` with the **Name** of the **Folder** where the `Cloned Repository` will be placed. 
- Once `Cloned`, move into the `Cloned_Repository Folder` by using the **Command**:
  ```
  cd <Local_Folder_Name>
  ```
  `Note:` Replace `<Local_Folder_Name>` with the **Name** of the **Folder** where the `Cloned Repository` has been placed.
- (**Optional**) You can also **Switch** to a desired `Branch` / `Branch_Name` by using the following **Command**:
  ```
  git checkout -b <Branch_Name>
  ```
  `Note:` Replace `<Branch_Name>` with the desired Branch Name.
  ![git clone](https://github.com/user-attachments/assets/e036cd53-9c96-46cb-816e-c02d3ff75e19)<br>
<br>

### Cloning a Specific Branch from the Remote_Repository:
- Launch the `Terminal` in the **directory** where you want to `Clone` the specific `Branch` from a `Remote_Repository`.
- Use the following **Command** to `CLONE` a **Specific** `Remote_Branch` to the `Local Directory`:
  ```
  git clone -b <Remote_Branch> <Remote_Repository_URL> <Local_Folder_Name>
  ```
  `Note:`
  - `-b`: This **flag** tells `Git` to **checkout** the `develop` branch immediately after **Cloning**. So your `Current Branch` = `develop`.
  - Replace `<Remote_Branch>` with the **Specific** `Remote_Repository Branch` which you want to `CLONE`.
  - Replace `<Remote_Repository_URL>` with the URL of the `Remote_Repository`.
  - (**Optional**) Replace `<Local_Folder_Name>` with the **Name** of the **Folder** where the `Cloned Repository` will be placed.<br>
  <br>
  ![git clone -b](https://github.com/user-attachments/assets/8bee4149-435b-4fe6-b469-ad827988f1be)<br>
- Once `Cloned`, move into the `Cloned_Repository Folder` by using the **Command**:
  ```
  cd <Local_Folder_Name>
  ```
  `Note:` Replace `<Local_Folder_Name>` with the **Name** of the **Folder** where the `Cloned Repository` has been placed.
- You can verify if the Cloned Repository is tracking the desired branch from remote repository by using the following command:
  ```
  git status
  ```
  ![git clone -b >> git status](https://github.com/user-attachments/assets/ad8de09c-ff23-4998-85e7-83159794831e)<br> 
<br>

### Cloning a Remote_Repository using VS_Code:

<br>

---
<br>

