# Git_Repository Initialization and Setup
---
<br>

## Repository Initialization Using **Github_Website**
  - Go To **[`Github`](https://github.com/)** .
  - `Sign In` to your Github_Account.
  - To `Create a New Repository` >> Click on `New`
    ![GitHub>>New_Repository](https://github.com/user-attachments/assets/5c88809c-97f5-421b-9b56-5a9f44146b49)
  - Set `Repository_NAME` >> Set `Repository_DESCRIPTION` (Optional) >> Set `VISIBILITY` (Either `Public` or `Private`) >> Customize `.gitignore` (Optional) >> Choose an appropriate `LICENSE` for your work (Optional).
  - After Performing above steps Click on `Create Repository` to Initialize and Create a Github_Repository .
    ![GitHub>>Create_Repository](https://github.com/user-attachments/assets/17ec6a4a-1ab1-4feb-99f3-934d2cd39e27)
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

## Repository Initialization Using **Github_Desktop**
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

## Configure Git [For a Specific  Repository]
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

## Configure Git Credentials [For Github Desktop]
  - Open GitHub_Desktop.
  - Browse `File` >> Click on `Options...` o/r Use shortcut `Ctrl + ,`.<br>
    ![GitHub_Desktop>>File>>Options....](https://github.com/user-attachments/assets/4f1f7d1e-a95a-47cf-b9fc-68ef8dded11e)
    <br>
  - Under Accounts >> Click on `Sign In`.<br>
    ![Options>>Accounts>>Sign In](https://github.com/user-attachments/assets/5fc1abba-8e75-4d08-b1d6-319170f08f77)
    <br>
    You will be redirected to the Sign In web page after clicking on the `Continue with browser` Button.<br>
    ![Redirect_To_SignIn_Webpage](https://github.com/user-attachments/assets/892be788-c582-4f00-891f-47ee5dfeaaff)
    <br>
    `Sign In` to Your `GiitHub Account`<br>
    ![SignIn_WebPage](https://github.com/user-attachments/assets/c5cd19e3-8a31-44b8-beb2-c9e620281d40)
    <br>
    Click `Open GithubDesktop.exe` for redirecting to GitHub_Desktop.<br>
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
