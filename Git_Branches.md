# Branches
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **What do we mean by `Branches`?**                                                                         | >> [` CHECK CONTENT `](#what-are-branches-in-github-)                                         |
| 2.  **Create and Switch Branches [For `Local_Branches`]**                                                      | >> [` CHECK CONTENT `](#create-and-switch-branches-for-local-branches)                        |
| 3.  **Create and Switch Branches [For `Remote_Branches`]**                                                     | >> [` CHECK CONTENT `](#create-and-switch-branches-for-remote-branches)                       |
| 4.  **Fetch `Branches` for a `GitHub_Repository`**                                                             | >> [` CHECK CONTENT `](#fetching-branches)                                                    |
| 5.  **Linking `Local_Branches` to `Remote_Branches`**                                                          | >> [` CHECK CONTENT `](#linking-local-and-remote-branches)                                    |
</div>

---
<br>

## What are Branches in GitHub ?
- `Branches` are **Individual Lines of Development** within a `GitHub_repository`.
- They allow you to work on `changes`, `new_features` or `bug_fixes` separately from the **Main_Codebase**.
- **Multiple** `Branches` can exist at the same time, supporting **Collaborative** and **Parallel Development**.
- **Types of Branches:**
  - **`main` (or `master`):** It is the **Main Branch** of your project. Contains the **final**, **stable** Code.
  - **`develop`:** It is used to **Combine** all **New Work** (`features`, `fixes`). **Acts** like a `Testing_Area` before updating the `main` branch.
  - **`feature`:** It is used to **Build** a **New Feature**. It is created from `develop` and merged back when done.
  - **`release`:** It is used to **Prepare** a **New Version** of the project before it's deployed. The `release` branch is merged into `main` (**for production**) and also into `develop` (**to keep future work in sync**).
  - **`hotfix`:** It is used for quickly **Fixing Urgent Issues** in the project.
<br>

---
<br>

## Create and Switch Branches [For Local Branches]
### Create a Branch:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Create a New Branch:**
  ```
  git branch BRANCH_NAME
  ```
  `Note:` Switch `BRANCH_NAME` with your desired **Branch-Name** (Ex: `main`, `develop`,etc or Other)
<br>

### Switch to a Branch:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Switch to an Existing Branch:**
  ```
  git checkout BRANCH_NAME
  ```
  `Note:` Switch `BRANCH_NAME` with your **existing Branch-Name** (Ex: `main`, `develop`,etc or Other)
<br>

###  Create and Switch to a Branch Simultaneously:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Create and Switch to a Branch Simultanoeusly:**
  ```
  git checkout -b BRANCH_NAME
  ```
  The **`-b` Flag** indicates `Git` to **Create a New Branch**.<br>
  `Note:` Switch `BRANCH_NAME` with your desired **Branch-Name** (Ex: `main`, `develop`,etc or Other)  
<br>

---
<br>

## Create and Switch Branches [For Remote Branches]
### Create a Remote Branch:
- **Navigate** to your `Github_Repository`.
- **Click** on the `Branch Dropdown_Menu` to **Create** a `New Branch` in the Project:
  ![Branch Dropdown_Menu](https://github.com/user-attachments/assets/7910d3ca-1aa1-4a80-aa0d-c9aab3212865)<br>
- **Select** the `Branch` (`SELECTED_BRANCH`) from which you want to **Create** a `NEW_BRANCH`.<br>
  Basically, this will `Clone` the contents of `SELECTED_BRANCH` and **Create** a `NEW_BRANCH` with them.<br> 
- Enter the `NEW_BRANCH_NAME` and **Click** on `Create NEW_BRANCH_NAME from SELECTED_BRANCH`:
  ![Create NEW_BRANCH from SELECTED_BRANCH](https://github.com/user-attachments/assets/430db745-f33f-4495-b1e6-2cb4d2289bd5)<br>
- The **Newly Created Branch** will be displayed in the `Branch Dropdown_Menu` as follows:
  ![New Branch](https://github.com/user-attachments/assets/95211ee7-ae29-47c7-8131-3759b838c282)<br>  
<br>

### Switching a Remote Branch:
- **Navigate** to your `Github_Repository`.
- **Click** on the `Branch Dropdown_Menu` to **View** the `Existing Branches` in the Project:
  ![Branches Dropdown_Menu](https://github.com/user-attachments/assets/3ed22315-5d47-4e54-9db1-4465bbf5dec0)<br>
- **Select** the `Branch` which you want to `Switch` to.
  ![Switching the Remote Branch](https://github.com/user-attachments/assets/6cfa19db-267e-4f38-bbbf-b0043b1bb14c)<br>
- The Repository_Page now display the **Files** from the `Selected_Remote_Branch`:
  ![Selected_Remote_Branch](https://github.com/user-attachments/assets/80087b3f-df2e-4f6e-ac8a-ddaf68748e21)<br>
<br>

---
<br>

## Fetching Branches
### Fetch Branches from Remote_Repository:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Fetch** all the `Branches` from a `Remote_Repository`:
  ```
  git fetch
  git branch -r
  ```
  `fetch:` This **Command** is used to **Download** the latest `commits`, `branches`, and `tags` from the `Remote_Repository` without merging or modifying your working directory.<br>
  `-r:` This **Flag** is used to **List** all `remote-tracking branches` (from `Remote_Repository`) that your `Local_Repository` knows about.
- The **Command** will display the `Remote_Branches` in the format: `origin/branch-name`
  ![git fetch>>git branch -r](https://github.com/user-attachments/assets/86f100ff-ffbc-41d4-9091-7b625f554f6f)<br>
  `Note:` The `fetch` **Command** fetches Updates from the `Remote_Repository`, but it doesn’t automatically `prune (remove)` **References** to **Branches** that **no longer exist** on the `Remote_Repository`, from your `Local_Repository`. Hence, you may also see **References** of **Deleted** `Remote_Branches` being displayed.
<br>

### Fetch Branches from Local_Repository:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Fetch** all the `Branches` on your `Local_Repository`:
  ```
  git branch 
  ```
- The **Command** will display the `Local_Branches` from your `Local_Repository`:
  ![git branch](https://github.com/user-attachments/assets/a9c760f3-ae7d-44df-9033-6d722f65ff7b)<br>
<br>

### Fetch All Branches:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Fetch** all the `Local_Branches` as well as `Remote_Branches`:
  ```
  git fetch
  git branch -a
  ```
  `Note:` The `fetch` **Command** is required to return the **Latest** List of `Remote_Branches`.
- The **Command** will display the `Local & Remote Branches` known to your `Local Repository`:
  ![git fetch>>git branch -a](https://github.com/user-attachments/assets/fb92eddc-dc07-4983-be65-71a60e106790)<br>
<br>

---
<br>

## Linking Local and Remote Branches
### Linking Existing Local and Remote Branches:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` for **Linking** the **Existing **`Local and Remote Branches`:
  ```
  git branch --set-upstream-to=origin/REMOTE_BRANCH LOCAL_BRANCH
  ```
  `Note:`
  - The `--set-upstream-to` sets the `Remote_Branch` that your `Local_Branch` is **Tracking**.<br>
    It tells `Git`:<br>
    - Where to `pull from` when you **Run** `git pull`
    - Where to `push to` when you **Run** `git push`
  - Also, Replace the `LOCAL_BRANCH` with your desired `Local-Branch-Name` and `REMOTE_BRANCH` with the `Remote-Branch-Name` to which you want to **Link** with. 
- Use the following **Command** to **Switch** to the **Respective** `Local Branch`:
  ```
  git checkout LOCAL_BRANCH
  ```
- Finally, Use this **Command** to Confirm the `Linking_Status`:
  ```
  git status
  ```
  ![Linking **Existing** `Local and Remote Branches`](https://github.com/user-attachments/assets/6c5caf1f-ee77-4945-bef7-e78b1b403ab9)<br>
<br>

### Create a Local_Branch and Link it to an Existing or New Remote_Branch:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` for **Creating & Linking** `Local_Branch` to **New or Exisitng** `Remote_Branch`:
  ```
  git checkout -b LOCAL_BRANCH origin/REMOTE_BRANCH
  ```
- The above **Command** performs the following **Tasks:**
  - Automatically **Creates** a **New** `Local_Branch` instance.
  - Switches to the **Newly Created** `Local_Branch`.
  - **Establishes** an `Upstream-Link` for the `Local_Branch` to track the `Remote_Branch`.<br>
- ![**Create and Link** `Local Branch` to an **Existing or New** `Remote Branch`](https://github.com/user-attachments/assets/a7c1b2ff-1c40-4e6c-bd85-7e99c2a3683b)<br>
- `Note:` If the **Command** finds the `REMOTE_BRANCH` on the `origin` (i.e, `Remote_Repository`), then it **Links** it to the `LOCAL_BRANCH`. Otherwise, it **Creates** the **Specified** `REMOTE_BRAMCH` on the `Remote_Repository` and **Links** it to the `LOCAL_BRANCH`.
<br>

### Pushing an Existing Local_Branch to the Origin (i.e, New Remote_Branch on a Remote_Repository):
- Open your `Terminal`.
- Use the following **Command** to `Initialize` and `COMMIT` **Demo_Commits** on the `Local_Repository`:
  ```
  git add .
  git commit -m "COMMIT MESSAGE"
  ```
  ![`Demo_Commit` Changes](https://github.com/user-attachments/assets/8c0e2e10-ffd8-47ff-99d4-8a50ed030a92)<br>
  ![git add . >> git commit -m "Demo Commit"](https://github.com/user-attachments/assets/ea22b4a7-67ef-43aa-9a4c-9a202a87d2a4)<br>
- Paste the following **Command** in your `Terminal` for **Linking** an **Exisitng** `Local_Branch` to a **Newly_Created** `Remote_Branch` (i.e, `PUSH` the `Local_Branch Commits` to the `Remote_Branch` on the `Remote_Repository`):
  ```
  git push -u origin LOCAL_BRANCH
  ```
  `Note:`
  - The `-u` **Flag** is shorthand for `--set-upstream`. It is used to **Set** the `Remote_Branch` that your `LOCAL_BRANCH` is **Tracking**.<br>
    It tells `Git`:
    - Where to `pull from` when you **Run** `git pull`.
    - Where to `push to` when you **Run** `git push`.<br>
  - The `origin` refers to the `Remote_Repository` where the `Remote_Branch` is to be **Established**.
  - Basically, it `PUSHes` your existing `Local_Branch` to the `Remote (Origin)` and **Creates** a New `Remote_Branch` **(if it Doesn't Already Exist)**.
- ![git push -u origin develop](https://github.com/user-attachments/assets/c7f5b832-d797-48b6-a156-63c88a61076e)
<br>

---
<br>

