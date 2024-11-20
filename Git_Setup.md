# Git/Github_Setup [Using VsCode]
---

## Prerequisites Installation
  - [`Download VSCode`](https://code.visualstudio.com/)
  - [`Download Git`](https://git-scm.com/)
  - [`Create GitHub Account`](https://github.com/signup)

## Ensure Git is added to your System's PATH 
  - If Git is not recognized in your terminal, you need to add it to your System's PATH.

  - On `Windows`:
    - Search for `Edit the System's Environment Variables` in the `Start Menu`.
    - Under `Advanced`, click `Environment Variables`.
    - Under `User Variables`, click on the `PATH` variable, then click `Edit`.
    - Click `New` and Add the path to your `Git bin` folder (e.g., C:\Program Files\Git\bin\git.exe).
    - `Click OK` to Save.

<div align="center">
___________________________________________________
</div>

## Alternatively you can download [` GitHub_Desktop `](https://github.com/apps/desktop) 
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

## Configure Git
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
