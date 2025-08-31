# Git_Repository Initialization and Setup
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **Create A Repository Using Git_CLI Commands**                                                             | >> [` CHECK CONTENT `](#local-repository-initialization--using-git_cli--recommended)                |
| 2.  **Create A Repository Using GitHub_CLI (gh) Commands**                                                     | >> [` CHECK CONTENT `](#repository-initialization--using-github_cli-gh--recommended)          |
| 3.  **Create A Repository Using GitHub_Web_Interface / Initialize a Remote_GitHub_Repository**                 | >> [` CHECK CONTENT `](#repository-initialization--using-github_website--recommended)         |
| 4.  **Create A Repository Using GitHub_Desktop**                                                               | >> [` CHECK CONTENT `](#repository-initialization--using-github_desktop-)                     |
| 5.  **Create A Repository Using VSCode Source_Control Tool**                                                   | >> [` CHECK CONTENT `](#repository-initialization--using-vscode-source-control-)              |
</div>

---
<br>

## Local Repository Initialization [ Using Git_CLI ] (Recommended)
  - Open a `Command_Prompt` or `Git_Bash` Terminal.
  - Set the Folder's `Path` where you want to Initialize the Git repository.
    ```
    cd C:/My_Workspace/path_to_folder
    ```
  - Use the `init` command in the Terminal to `Initialize` a Git repository.
    ```
    git init
    ```
    ![git init](https://github.com/user-attachments/assets/8842b3bd-c3b8-43d5-9a50-c437d24150f0)<br>
    <br>
  - Create a `Demo Commit File` in the Local Repository Folder to make the `First Commit`, so that the repository can be published to GitHub.<br>
    ![VSCode>>Demo Commit File](https://github.com/user-attachments/assets/0f7f0742-fd4d-451a-9e67-0c0185ffae24)<br>
    <br>
  - Create a `Remote GitHub Repository` By Following the Steps for [`Repository Initialization Using Github_Web-Interface`](#repository-initialization--using-github_website--recommended).
  - Copy the `URL` for this `GitHub Repository`:<br>
    ![Copy_URL_from_Address_Bar](https://github.com/user-attachments/assets/c7453c89-51af-4bfe-bd31-76d62add8563)<br>
    <br> <div align="center">**OR**</div> <br>
    ![GitHub_Website>>Code<>>>Local>>Copy URL](https://github.com/user-attachments/assets/6484b66b-f33a-404e-b4c2-9b7b2c6d1015)<br>
    <br>
  - Use the following Command in the Terminal to `Link` the `Remote Repository` to your `Local Repository`.
    ```
    git remote add origin https://github.com/USERNAME/REPOSITORY-NAME
    ```
    `Note:` Substitute **'USERNAME'** with your **'GitHub_Username'** and **'REPOSITORY-NAME'** with your **'Remote Repository_Name'** `OR` **PASTE** your `Repository_URL` instead.<br>
    [`Learn more about Managing Remote_Repositories`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Remote_Repositories.md)<br>
  - Now, if you have `Not Signed_In` with your `GitHub_Account`, `Signed_In` with a `Different GitHub_Account` than the **Account** on which the `Remote_Reposiotry` **Lies** or other such reasons causing an `Account or Ownership Mismatch`, then on executing the above **Command** **Git** might throw an error as follows:<br>
    ![`dubious_ownership` Error](https://github.com/user-attachments/assets/c11a934a-0eb5-4a6f-8b82-aec61df23343)<br>
    The above `Error` simply states that, **Git** cannot verify **Ownership** of the `Local_Repository / Directory` as you might be working on an `External Drive`, a `Shared Folder` or a `Different User_Account`.<br>
    Use the following **Command** in your `Terminal` to **Resolve** this `Error`:
    ```
    git config --global --add safe.directory "Path/To/Local_Repository"
    ```
    This **Command** flags the `Local_Repository` to be **Safe** and **Trustworthy** to work in.
  - Use the `add` Command to `Stage` any Unstaged (New) Changes >> Use the `commit` Command to `Save` the Staged Changes to the Repository.
    ```
    git add .
    git commit -m "Initial Message"
    ```
  - Take an initial **PULL** from the `Remote Repository` to sync your `Local Branch` with it.
    ```
    git pull --rebase origin master
    ```
    `Note:`
    - Replace `master` with your `BRANCH_NAME` to avoid any errors. [`Learn more about Branches`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Branches.md)<br>
    - Also, make sure to **PULL** before **PUSHing** to keep branches `conflict-free`.
  - Use the `push` Command to `Upload` the Changes to the Remote_GitHub_Repository.
    ```
    git push -u origin master
    ```
    `Note:`
    - The `-u` **Flag** is shorthand for `--set-upstream`. It is used to **Set** the `Remote_Branch` that your `Local_Branch (master)` is **Tracking**.<br>
      It tells `Git`:
      - Where to `pull from` when you **Run** `git pull`.
      - Where to `push to` when you **Run** `git push`.<br>
    - The `origin` refers to the `Remote_Repository` where the `Remote_Branch` is to be **Established**.
    - Also, Replace `master` with your `BRANCH_NAME` to avoid any errors. [`Learn more about Branches`](https://github.com/Yashvant-Chhapwale-Course-Work/GitHub_Prompts/blob/main/Git_Branches.md)<br> 
    ![git push -u origin](https://github.com/user-attachments/assets/296259f7-fae7-452e-b9d8-edeba8748d98)<br>
  <br>

  
  **Congratulations! You have successfully `Initialized a Local Repository` and `Linked it with a Remote Repository` using Git_CLI!!**
<br>

---
<br>

## Repository Initialization [ Using GitHub_CLI (gh) ] (Recommended)
  - Open a `Command_Prompt` or `Git_Bash` Terminal.
  - Paste the following Command in the Terminal to `Create a Remote Git Repository`.
    ```
    gh repo create DEMO-GITHUB-REPOSITORY --public
    ```
    `Note:` Substitute **'DEMO-GITHUB-REPOSITORY'** with your `Repository-Name` and **'--public'** with your `Preferred Visibility Flag (--private / --public)`.
  - Now, follow the **Steps** for [`Initializing a Local Repository and Linking it with the Above Remote_Repository`](#repository-initialization--using-git_cli--recommended).
<br>

---
<br>

## Repository Initialization [ Using Github_Website ] (Recommended)
  - Go To **[`Github`](https://github.com/)** .
  - `Sign In` to your Github_Account.
  - To `Create a New Repository` >> Click on `New`<br>
    ![GitHub>>New_Repository](https://github.com/user-attachments/assets/5c88809c-97f5-421b-9b56-5a9f44146b49)
    <br>
  - Set `Repository_NAME` >> Set `Repository_DESCRIPTION` (Optional) >> Set `VISIBILITY` (Either `Public` or `Private`) >> Customize `.gitignore` (Optional) >> Choose an appropriate `LICENSE` for your work (Optional).
  - After Performing above steps Click on `Create Repository` to Initialize and Create a Github_Repository.<br>
    ![GitHub>>Create_Repository](https://github.com/user-attachments/assets/17ec6a4a-1ab1-4feb-99f3-934d2cd39e27)
    <br>
  - **`Public Repository`:**
    - **Description:** `Visible to everyone on GitHub.` Anyone can view the repository contents, including code, issues, and pull requests.
    - **Access Control:** Only collaborators or contributors with appropriate permissions can make changes.
    - **Use Cases:** Open-source projects, publicly shared resources, community contributions.
  - **`Private Repository`:**
    - **Description:** `Restricted to specific users or teams.` Only authorized users can view or access the contents.
    - **Access Control:** Collaborators or organization members with explicit access can contribute.
    - **Use Cases:** Proprietary projects, sensitive work, internal collaboration.
<br>

---
<br>

## Repository Initialization [ Using Github_Desktop ]
  - Open `Github_Desktop`.
  - Browse `File` >> Click on `New repository...` o/r Use Shortcut ` Ctrl + N `.<br>
    ![GitHub_Desktop>>New_Repository](https://github.com/user-attachments/assets/0bae54da-c3de-400d-8901-b0440684e2bf)
    <br>
  - Set `Repository_NAME` >> Set `Repository_DESCRIPTION` (Optional) >> Select a `Path` on your Local Machine where the Git_Repository should be created >> Customize `.gitignore` (Optional) >> Choose an appropriate `LICENSE` for your work (Optional).
  - After Performing above steps Click on `Create Repository` to Initialize and Create a Github_Repository.<br>
    ![GitHub_Desktop>>Create_Repository](https://github.com/user-attachments/assets/6bf01418-cf4c-4ddb-b14d-5cf48b8f2475)
    <br>
  - This Repository is currently only available on your Local Machine. Click on `Publish repository` to make it available on your GitHub _Account.<br>
    ![Github_Desktop>>Publish_Repository](https://github.com/user-attachments/assets/44b52764-c714-433a-8d81-3cad977ee14e)
    <br>
  - Provide the `REPOSITORY_NAME` and a `REPOSITORY_DESCRIPTION (Optional)` >> Click on `Publish Repository` to publish the Repository on your GitHub_Account.<br>
    ![Github_Desktop>>Publish_Repostiory>>Enter_Name_And_Description](https://github.com/user-attachments/assets/8a91e346-562d-49d5-8320-2d631f3f6b79)<br>
    [`Note`: Uncheck the `Keep this code private` Option to make the Repository Public. `By Default, GitHub_Desktop sets the Repository to Private` when publishing from your Local Machine.]
<br>

---
<br>

## Repository Initialization [ Using VSCode Source-Control ]
  - Open `VSCode`.
  - For `Initialising a New Project`, Go To `File` >> Click on `Open Folder` or Use shortcut `Ctrl + O` >> Create/Open a New Folder in your Local Machine for the Project.
  - [`Note`: For `Uploading an Existing Project`, Navigate To and Open the folder where the Project is Stored.]<br>
    ![VSCode>>File>>Open Folder](https://github.com/user-attachments/assets/2b2ac1c6-4dda-4384-a205-fc05fb96bb6e)
    <br>
  - Go To `Source Control` by Clicking on the `Fork` icon >> Click on `Initialize Repository`.<br>
    ![GitHub>>Source Control>>Initialize Repository](https://github.com/user-attachments/assets/6abdcb44-6d06-44c6-b779-214503bc3f25)
    <br>
  - Create a `Demo Commit File` in the Local Repository Folder to make the `First Commit`, so that the repository can be published to GitHub.<br>
    ![VSCode>>Demo Commit File](https://github.com/user-attachments/assets/0f7f0742-fd4d-451a-9e67-0c0185ffae24)
    <br>
  - Go To `Source-Control` >> Replace 'ENTER-COMMIT-TEXT' with a `Commit Message` >> Click on `Commit` to commit changes to local repository.<br>
    ![VSCode>>Demo Commit File>>Commit](https://github.com/user-attachments/assets/4748d8ec-fb03-482b-b5b4-cb4cfb82d113)
    <br>
  - Click on `Yes` to `Stage All Changes and Commit them directly`<br>
    ![VSCode>>Demo Commit File>>Commit>>Stage and Commit ? 'Yes'](https://github.com/user-attachments/assets/e9cc609f-6974-49ed-8413-2815293baf52)
    <br>
  - Click on `Publish Branch` to upload/create the Project as a Remote Repository.<br>
    ![VSCode>>Source Control>>Publish Branch](https://github.com/user-attachments/assets/3a489239-db4c-4682-9369-669ffd0013e2)<br>
    `Note`:
    - If VSCode is not connected to the GitHub Account where you want to create a Repository, then it will prompt you for permission to Sign In to your GitHub Account.
    - Click on `Allow` and `Sign_In` to your GitHub Account.
    - **To `Change GitHub_Account` where the repository is being published:** Go To  [`Git_Setup`](Git_Setup.md) >> Click on `CHECK CONTENT` for `Configure Git Credentials [For VSCode with GitHub Pull Requests Extension]` or for `Configure Git Credentials [For VSCode without GitHub Pull Requests Extension]` >> Follow the steps shown in the Section to change your GitHub Account for VSCode.
  - Replace `Demo-GitHub-Repository` with your intended `Repository-Name` >> Select `Publish to GitHub Private Repository` or `Publish to GitHub Public Repository` based on the type of `Access Control` you want for the repository.<br>
    ![VSCode>>Publish Branch>>Public Or Private](https://github.com/user-attachments/assets/a6406ffa-74f4-4770-8c70-39a246462fef)
    <br>
  - Once the Repository is Initialized and Published to GitHub Remote a Pop-Up Window will appear at Bottom-Right Corner in VSCode >> Click `Open on GitHub` to view the Published Remote Repository.
    ![VSCode>>Publish Repository>>Open on GitHub](https://github.com/user-attachments/assets/2dfd78cf-7b3d-4fd4-bfe2-33a8d983324a)
<br>

---
