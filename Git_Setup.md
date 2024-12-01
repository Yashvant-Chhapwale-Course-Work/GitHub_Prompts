# Git/Github_Setup
---
<br>
<div align="center">
 
### TABLE OF CONTENT
 
| TITLE                                                                                                          | SECTION_LINK                                                                                  |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| 1.  **Pre_requisites**                                                                                         | >> [` CHECK CONTENT `](#prerequisites-installation)                                           |
| 2.  **Git Version Verificaton**                                                                                | >> [` CHECK CONTENT `](#version-verification)                                                 |
| 3.  **Configure Git Credentials Using CLI**                                                                    | >> [` CHECK CONTENT `](#configure-git-using-cli)                                              |
| 4.  **Configure Git Credentials Using CLI [For a Specific Repository / Project]**                              | >> [` CHECK CONTENT `](#configure-git-for-a-specific-repositoryproject-using-cli)             |
| 5.  **Configure Git Credentials [For GitHub Desktop]**                                                         | >> [` CHECK CONTENT `](#configure-git-credentials-for-github-desktop)                         |
| 6.  **Configure Git Credentials [For VSCode with `GitHub Pull Requests Extension`]**                           | >> [` CHECK CONTENT `](#if-github-pull-requests-extension-is-enabled)                         |
| 7.  **Configure Git Credentials [For VSCode without `GitHub Pull Requests Extension`]**                        | >> [` CHECK CONTENT `](#if-github-pull-requests-extension-is-not-enabled)                     |
| 8.  **GitHub Extensions For VSCode**                                                                           | >> [` CHECK CONTENT `](#vscode-extensions)                                                    |
</div>

---
<br>

## Prerequisites Installation
  - [`Download VSCode`](https://code.visualstudio.com/)
  - [`Download Git`](https://git-scm.com/)
  - [`Create GitHub Account`](https://github.com/signup)

## Ensure Git is added to your System's PATH 
  - If Git is not recognized in your terminal, you need to add it to your System's PATH.

  - On `Windows`:
    - Search for `Edit the System's Environment Variables` in the `Start Menu`.<br>
      ![Edit_The_System_Environment_Variables](https://github.com/user-attachments/assets/14c2c514-887c-49b5-8f40-b17064d4f976)
      <br>
    - Under `Advanced` >> click `Environment Variables`.<br>
      ![System_Properties>>Advanced_TAB>>Environment Variables](https://github.com/user-attachments/assets/d86361a7-cd10-4e8b-af90-cdd894be1fad)
      <br>
    - Under `User Variables` >> click on the `PATH` variable >> click `Edit`.<br>
      ![Environment Variables>>User_Variables>>PATH>>Edit](https://github.com/user-attachments/assets/f445bae0-49cd-4174-9715-e7de4c22fe43)
      <br>
    - Click `New` >> Add the path to your `Git bin` folder (e.g., C:\Program Files\Git\bin\git.exe).
    - `Click OK` to Save.<br>
      ![Edit_Environment_Variable>>New>>OK](https://github.com/user-attachments/assets/15fe7218-fb0f-48d9-981a-b88021c12b77)
      <br>
      
<div align="center">
___________________________________________________
</div>
<br>

## Alternatively you can download [` GitHub_Desktop `](https://github.com/apps/desktop) (Recommended)
  - Download [` GitHub_Desktop `](https://github.com/apps/desktop) instead of downloading and setting up `Git_CLI` separately.
  - **`Advantages`** Of GitHub Desktop:
    - `User-Friendly Interface`: Easy to navigate GUI, suitable for beginners.
    - Displays line-by-line changes for `easier code review`.
    - `Streamlines frequent Git actions` like commits, pushes, and pulls.
    - `Simplified Branch Management`: Easy creation, switching, and merging of branches.
    - `Integrated GitHub Features`: Direct support for pull requests, issue tracking, and repository publishing.
    - `Built-In Conflict Resolution`: User-friendly tools for resolving merge conflicts.
    - `Multi-Repository Management`: Seamlessly manage and switch between multiple repositories.
    - `Quick Authentication`: Simplifies login and authentication with GitHub accounts.
    - `No Separate Git Installation Required`:
      - GitHub Desktop includes pre-configured Git installation, reducing setup complexity.
      - Users can start using Git features through Command_Prompt / Powershell immediately after installing GitHub Desktop.
<br>

---
<br>

## Version Verification
  - You can verify the `Installed_Version of Git`, using the following command in the Shell:
    ```
    git --version
    ```
  - To Determine the `Directory where Git is Installed` on your System, use the following command in the Shell:
    ```
    where git
    ```
<br>

---
<br>

# Using Git_CLI [Command Line Interface]
### Configure Git [Using CLI]:
  - Open your terminal or command prompt and configure Git with your GitHub credentials.
  - ```
    git config --global user.name "GITHUB_USERNAME"
    git config --global user.email "EMAIL_ID@gmail.com"
    ```
    Replace **`GITHUB_USERNAME`** with **`Your Github Username`** and **`EMAIL_ID@gmail.com`** with **`Your Github_Email Account`**.
  - Verify the Changes:
    ```
    git config --list --global
    ```
  - Alternatively you can Inspect Specific Configurations:
    ```
    git config user.name
    ```
    
    ```
    git config user.email
    ```
<br>

### Configure Git For a Specific Repository/Project [Using CLI]:
  - Open your terminal or command prompt and configure Git with your GitHub credentials.
  - Navigate to the Local Repository using the `cd (Change Directory)` Command:
    ```
    cd C:\My_Workspace\<path_to_local_repository>
    ```
  - Configure Your Github Credentials for the local repository:
    ```
    git config user.name "GITHUB_USERNAME"
    git config user.email "EMAIL_ID@gmail.com"
    ```
    Replace **`GITHUB_USERNAME`** with **`Your Github Username`** and **`EMAIL_ID@gmail.com`** with **`Your Github_Email Account`**.
  - Verify the Changes:
    ```
    git config --list --local
    ```
  - Alternatively you can Inspect Specific Configurations:
    ```
    git config user.name
    ```
    
    ```
    git config user.email
    ```
<br>

---
<br>

# Using GitHub_Desktop
### Configure Git Credentials [For GitHub Desktop]:
  - Open `GitHub_Desktop`.
  - Browse `File` >> Click on `Options...` o/r Use shortcut `Ctrl + ,`.<br>
    ![GitHub_Desktop>>File>>Options....](https://github.com/user-attachments/assets/4f1f7d1e-a95a-47cf-b9fc-68ef8dded11e)
    <br>
  - Under Accounts >> Click on `Sign In`.<br>
    ![Options>>Accounts>>Sign In](https://github.com/user-attachments/assets/5fc1abba-8e75-4d08-b1d6-319170f08f77)
    <br>
  - You will be redirected to the Sign In web page after clicking on the `Continue with browser` Button.<br>
    ![Redirect_To_SignIn_Webpage](https://github.com/user-attachments/assets/892be788-c582-4f00-891f-47ee5dfeaaff)
    <br>
  - `Sign In` to Your `GitHub Account`<br>
    ![SignIn_WebPage](https://github.com/user-attachments/assets/c5cd19e3-8a31-44b8-beb2-c9e620281d40)
    <br>
  - Click `Open GithubDesktop.exe` for redirecting to GitHub_Desktop.<br>
    ![Redirecting Github_Desktop](https://github.com/user-attachments/assets/807f3edc-20e2-404b-95f1-0c01288397f3)
    <br>
  - Again, Go To `File` >> Click on `Git`>> Set Your `Git_Credentials(Username and Email)` For Git.<br>
    `NOTE`:Generally This Step Is Configured Automatically With Account Sign In.<br>
    ![GitHub_Desktop>>File>>Git>>Set Name_and_Email](https://github.com/user-attachments/assets/f7a33cae-fe2f-4770-bd56-b04492550f6f)
    <br>
  - Click on `Save` to Save Credentials.
<br>

---
<br>

# Using VSCode
  ### If "GitHub Pull Requests" Extension is Enabled:
  - Open `VSCode`.
  - Click on `Accounts_Icon` at the `Bottom-Left Corner of VSCode` >> Click on `Sign in with GitHub to use GitHub Pull Requests.`<br>
    ![VSCode>>Accounts](https://github.com/user-attachments/assets/c3f41205-5505-4373-820e-df066325d95f)
    <br>
  - `Sign In` to Your `GitHub Account`<br>
    ![VSCode>>GitHub_SignIn](https://github.com/user-attachments/assets/95c8cd1b-afda-483f-8066-d169ebecf162)
    <br>
  - `To Change GitHub Account:` Click on `Accounts_Icon` >> Click `>` on Account with `(GitHub)` Tag >> Click `Sign Out` >> Follow the above steps to `Sign_In to the desired GitHub_Account`.<br>
    ![VSCode>>Sign_Out](https://github.com/user-attachments/assets/63815e4b-1f28-44ec-8310-4943d4056145)
    <br>
    
<div align="center">
___________________________________________________
</div>
<br>

 ### If "GitHub Pull Requests" Extension is Not Enabled:
 - Open `VSCode`.
 - Browse `File` >> Click on `Open Folder...` or Use Shortcut `Ctrl + O` >> `Select the folder which you want to upload to GitHub` or `Select Any Random Folder, If you just want to Sign_In to GitHub Account`.
 - Browse `View` >> Click on `Command Palette...`<br>
   ![VSCode>>View>>Command Palette](https://github.com/user-attachments/assets/7a34e476-b179-4e2a-943f-d9331bd170f7)
   <br>
 - Paste the Command ` Publish to GitHub ` in the Command Palette >> Press `Enter`<br>
   ![VSCode>>View>>Command Palette>>Publish to GitHub](https://github.com/user-attachments/assets/26436dcb-5cd5-4c3e-aa07-f313c97d36cd)
   <br>
 - Click `Allow` to give permission for Signing_In to your GitHub Account<br>
   ![Publish to GitHub>>Click Allow](https://github.com/user-attachments/assets/ada7073b-c0cb-4180-8e38-c27fdeb17191)
   <br>
 - `Sign In` to Your `GitHub Account`<br>
   ![VSCode>>GitHub_SignIn](https://github.com/user-attachments/assets/95c8cd1b-afda-483f-8066-d169ebecf162)
   <br>
    You Have Successfully Signed_In to VSCode with your GitHub Account!
 - `To Change GitHub Account:` Click on `Accounts_Icon` >> Click `>` on Account with `(GitHub)` Tag >> Click `Sign Out` >> Follow the above steps to `Sign_In to the desired GitHub_Account`.<br>
   ![VSCode>>Sign_Out](https://github.com/user-attachments/assets/63815e4b-1f28-44ec-8310-4943d4056145)
   <br>
   
<br> 

---
<br>

# VSCode Extensions:
You can enhance Git operations in VS Code by downloading the following extensions:
  - `GitHub Pull Requests`:
    - Publisher: **GitHub**
    - Description: This extension allows you to manage pull requests and issues directly in VS Code.
    - Functions:
        - Create, review, and merge pull requests.
        - Browse and comment on issues.
        - View repository details.
    - ![GitHub_Pull_Requests](https://github.com/user-attachments/assets/f9f0b338-3d8a-4e18-af54-c848304a9677)
    <br>
  - `GitLens -- Git supercharged`:
    - Publisher: **GitKraken**
    - Description:Enhances the built-in Git capabilities of VS Code by providing advanced features:
    - Functions:
      - See who made changes and why.
      - Explore commits and branches in detail.
      - GitHub integration for quick access to repositories.
    - ![Git_Lens](https://github.com/user-attachments/assets/23130a4a-e505-46c3-ab04-72ab9d6f1e68)
<br>

---
<br>

**`NOTE:`** It is recommended to configure each platform and tool mentioned above to prevent Collaboration Issues and ensure proper Git_Account Identification.
<br>

---
<br>
