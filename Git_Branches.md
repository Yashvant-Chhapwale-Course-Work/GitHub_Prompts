# Branches
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **What do we mean by `Branches`?**                                                                         | >> [` CHECK CONTENT `](#what-are-branches-in-github-)                                         |
| 2.  **Create and Switch Branches**                                                                             | >> [` CHECK CONTENT `](#create-and-switch-branches)                                           |
| 3.  **Configure Git Credentials Using Git_CLI**                                                                | >> [` CHECK CONTENT `](#configure-git-using-git_cli)                                          |
| 4.  **Configure Git Credentials Using Git_CLI [For a Specific Repository / Project]**                          | >> [` CHECK CONTENT `](#configure-git-for-a-specific-repositoryproject-using-git_cli)         |
| 5.  **Configure Git Credentials Using GitHub_CLI (gh)**                                                        | >> [` CHECK CONTENT `](#configure-git-using-github_cli-gh)                                    |
| 6.  **Configure Git Credentials [For GitHub Desktop]**                                                         | >> [` CHECK CONTENT `](#configure-git-credentials-for-github-desktop)                         |
| 7.  **Configure Git Credentials [For VSCode with `GitHub Pull Requests Extension`]**                           | >> [` CHECK CONTENT `](#if-github-pull-requests-extension-is-enabled)                         |
| 8.  **Configure Git Credentials [For VSCode without `GitHub Pull Requests Extension`]**                        | >> [` CHECK CONTENT `](#if-github-pull-requests-extension-is-not-enabled)                     |
| 9.  **GitHub Extensions For VSCode**                                                                           | >> [` CHECK CONTENT `](#vscode-extensions)                                                    |
| 10. **Update Git & GitHub_CLI (gh) [For Windows]**                                                             | >> [` CHECK CONTENT `](#update-git--github_cli-gh-for-windows)                                |
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

## Create and Switch Branches
### Create a Branch:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Create a New Branch:**
  ```
  git branch BRANCH_NAME
  ```
  or
  ```
  git -b BRANCH_NAME
  ```
  The **`-b` Flag** indicates `Git` to **Create a New Branch**.<br>
  `Note:` Switch `BRANCH_NAME` with your desired **Branch-Name** (Ex: `main`, `develop`,etc or Other)

### Switch to a Branch:
- Open your `Terminal`.
- Paste the following **Command** in your `Terminal` to **Switch to an Existing Branch:**
  ```
  git checkout BRANCH_NAME
  ```
  `Note:` Switch `BRANCH_NAME` with your **existing Branch-Name** (Ex: `main`, `develop`,etc or Other)

###  Create anf Switch to a Branch Simultaneously:
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
