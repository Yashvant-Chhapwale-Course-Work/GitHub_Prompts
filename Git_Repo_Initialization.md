# Git_Repository Initialization and Setup
---
<br>

## Repository Initialization Using Github_Website
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

## Repository Initialization Using Github_Desktop
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

---
<br>
