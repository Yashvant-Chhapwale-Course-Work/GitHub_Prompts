# Branches
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **What do we mean by `Branches`?**                                                                         | >> [` CHECK CONTENT `](#what-are-branches-in-github-)                                         |
| 2.  **Create and Switch Branches [For Local Branches]**                                                        | >> [` CHECK CONTENT `](#create-and-switch-branches-for-local-branches)                        |
| 3.  **Create and Switch Branches [For Remote Branches]**                                                       | >> [` CHECK CONTENT `](#create-and-switch-branches-for-remote-branches)                       |
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
  - **`release`:** used to **Prepare** a **New Version** of the project before it's deployed. The `release` branch is merged into `main` (**for production**) and also into `develop` (**to keep future work in sync**).
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
- Enter the `NEW_BRANCH_NAME` and **Click** on `Create NEW_BRANCH_NAME from main`:
  ![Create NEW_BRANCH_NAME from main](https://github.com/user-attachments/assets/745925ff-9303-4f09-8fcb-e7b9cc09402f)<br>
- The **Newly Created Branch** will be displayed in the `Scrolldown_Menu for Branches` as follows:
  ![New Branch](https://github.com/user-attachments/assets/95211ee7-ae29-47c7-8131-3759b838c282)<br>  
<br>

### Switching a Remote Branch:
- **Navigate** to your `Github_Repository`.
- **Click** on the `Branch Dropdown_Menu` to **View** a `Existing Branches` in the Project:
  ![Branches Dropdown_Menu](https://github.com/user-attachments/assets/3ed22315-5d47-4e54-9db1-4465bbf5dec0)<br>
- **Click** on the `Branch` to which you want to `Switch` to.
  ![Switching the Remote Branch](https://github.com/user-attachments/assets/6cfa19db-267e-4f38-bbbf-b0043b1bb14c)<br>
- The Repository_Page now shows the **Selected** `Branch's` Files:
  ![Switched_Remote_Branch](https://github.com/user-attachments/assets/80087b3f-df2e-4f6e-ac8a-ddaf68748e21)<br>
<br>

---
<br>
