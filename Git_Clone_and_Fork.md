# Clone & Fork
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                           | SECTION_LINK                                                                                  |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1 .  **What do we mean by `Cloning` a `Remote_Repository`?**                                                    | [` 🔗CHECK CONTENT `](#what-do-we-mean-by-cloning-a-remote_repository)                       |
| 2 .  **`Cloning` a `Remote_Repository` via `Git_CLI`**                                                          | [` 🔗CHECK CONTENT `](#cloning-a-remote_repository-through-git_cli)                          |
| 3 .  **`Cloning` a specific `Branch` from `Remote_Repository`**                                                 | [` 🔗CHECK CONTENT `](#cloning-a-specific-branch-from-the-remote_repository)                 |
| 4 .  **`Cloning` a `Remote_Repository` via `VS_Code Source Control`**                                           | [` 🔗CHECK CONTENT `](#cloning-a-remote_repository-using-vs_code)                            |
| 5 .  **What do we mean by `Forking` a `Remote_Repository`?**                                                    | [` 🔗CHECK CONTENT `](#what-do-we-mean-by-forking-a-remote_repository)                       |
| 6 .  **`Forking` a `Remote_Repository` into Your `Github_Account`**                                             | [` 🔗CHECK CONTENT `](#forking-a-remote_repository-into-your-github_account)                 |
</div>
 
---
<br>

## What do we mean by Cloning a Remote_Repository?
- `Cloning` is the process of **Creating** a `Full_Copy` of a `Remote_Repository` on your `Local_System` / `Local_Repository`. **[`Remote ➝ Local`]**
- This includes all the **Project** `Files`, `Branches`, `Commit_History`, and the `.git_Directory` that **Tracks Changes**.
- In case of a `Public_Repository`, anyone can `CLONE` the `Remote_Repository` and require **No Special Access** (Ex: `Owner`, `Collaborator`, etc).
- For `Private_Repository`, you require **Explicit Permission** to `CLONE` the `Remote_Repository` from the **Owner** or require to be added as a **Collaborator** to the `Remote_Repository`.<br>

<div align="center">

|**`Private_Repository` Access Level**  | **Can Clone?**  | **Can Push?** | **Can Manage Repo?** |
| ----------------------------------- | --------------- | ------------- | -------------------- |
|**Read**                             | ✅ Yes         | ❌ No         | ❌ No               |
| **Write**                           | ✅ Yes         | ✅ Yes        | ❌ No               |
| **Admin**                           | ✅ Yes         | ✅ Yes        | ✅ Yes              | 
| **Owner** (Org.)                    | ✅ Yes         | ✅ Yes        | ✅ Yes              |
</div>
<br>

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
  - (**Optional**) Replace `<Local_Folder_Name>` with the **Name** of the **Folder** where the `Cloned Repository` will be placed.
- ![git clone -b](https://github.com/user-attachments/assets/8bee4149-435b-4fe6-b469-ad827988f1be)<br>
- Once `Cloned`, move into the `Cloned_Repository Folder` by using the **Command**:
  ```
  cd <Local_Folder_Name>
  ```
  `Note:` Replace `<Local_Folder_Name>` with the **Name** of the **Folder** where the `Cloned Repository` has been placed.
- Use the following **Command** to verify whether your `Local_Clone` is **linked** to the **intended** `Remote_Branch`:
  ```
  git status
  ```
  ![git clone -b >> git status](https://github.com/user-attachments/assets/ad8de09c-ff23-4998-85e7-83159794831e)<br> 
<br>

### Cloning a Remote_Repository using VS_Code:
- **Open** your **Project** in `Visual_Studio_Code (VS_Code)`.
- From the `Navigation Bar`, **Click** `View` >> **Select** `Command Palette...`<br>
  ![`View`>>`Command Palette...`](https://github.com/user-attachments/assets/0942a48a-307e-499b-8654-e930f80fe0fc)<br>
- In the `Command Palette`, **Search** for `Git: Clone` & **Select** it.
  ![`Command Palette...`>>`Git: Clone`](https://github.com/user-attachments/assets/33a973f3-4f7d-4e44-b0a3-26eb2f09bb76)<br>
- **Copy** the `Remote_Repository URL` (`HTTPS` or `SSH`) from your **Hosting Service** (e.g., `GitHub` / `GitLab`).
  ![Remote_Repository>>`Copy URL`](https://github.com/user-attachments/assets/2f6228e1-7462-4b89-929b-1962ca267c70)<br>
- **Paste** the `Repo_URL` into the `Command Palette` >> **Choose** `Clone from URL`.
  ![`Command Palette...`>>`Git: Clone`>>Enter `Remote_Repo_URL`>>`Clone from URL`](https://github.com/user-attachments/assets/9507d4b1-3629-459e-b8c6-e0d09bd2dd40)<br>
- **Select** the `Local_Directory` where you want the `Remote_Repository` to be `Cloned` >> **Click** the `Select as Repository Destination` Button.
  ![Select `Local_Directory`>>Click on `Select as Repository Destination`](https://github.com/user-attachments/assets/3b0cf61f-31bc-4ee9-a4ee-6e231bd441b6)<br>
- Once **Cloning** is complete, **Choose** `Open` or `Open in New Window` to start working with the `Cloned_Repository` in `VS_Code`.
  ![`Open` or `Open in New Window`](https://github.com/user-attachments/assets/00207b4a-2895-486a-b064-93369ce3c1a1)<br>
<br>

---
<br>

## What do we mean by Forking a Remote_Repository? 
- `Forking` is the process of **Creating** a `Personal_Copy` of someone else’s `Remote_Repository` into Your `Own GitHub_Account` / `GitHub_Repository`. **[`Remote ➝ Remote`]**
- This allows you to **Experiment**, **Modify**, and **Add Features** to someone else's **Project** without affecting the `Original_Repository`.
- A `Forked_Repository` stays linked to the `Original_Repository`, so you can later **Submit** `Pull_Requests (PRs)` to contribute your changes back.
- `Forking` is commonly used in **Open Source Contributions** where developers **FORK** a project, **make changes** in their copy, and then **propose updates** to the Owner of the `Original_Repository`.
<br>

---
<br>

## Forking a Remote_Repository into Your GitHub_Account
- Open the `Remote_Repository` which you want to `FORK` into Your `GitHub_Account`.
- At the `Top-Right`, **Click** on the `Fork` Button.
  ![`Remote GitHub_Repository` >> `Fork`](https://github.com/user-attachments/assets/6e26ca64-4f25-45d3-9ba8-8f18db243cc3)<br>
<br>

---
<br>
