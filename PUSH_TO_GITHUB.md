# How to Push a Project in Visual Studio Code to GitHub using Command-Line Interface (CLI)

This markdown file explains how to upload a project from Visual Studio Code (VS Code) to a Github repository using Git commands/ CLI

## Step:
## 1. Open the Project in Visual Studio Code

Open the project folder in VS Code.

For example:
```text
C:\xampp\htdocs\document-ai-project
```
Then, open the VS Code terminal by selecting:

**Terminal -> New Terminal**

Make sure that the terminal is inside the project folder.

```powershell
PS C:\xampp\htdocs\document-ai-project>
```

## 2. Check the Git Status

Run the following command:

```bash
git status
```

This shows the current status of the project and identifies files that have been modified or are not yet tracked by Git.

## 3. Initialize the Git Repository

If Git has not been initialized in the project, run this in the terminal:

```bash
git init
```

This command creates a local Git Repository inside the project folder. (If the project is already a Git Repository, this step is not required)

## 4. Add the Project Files

Add the project files to the Git staging area:

```bash
git add .
```

The `.` means all files and folders in the current project directory will be added.

Then, check the status through this command:

```bash
git status
```

Now, the files should appear under **Changes to be committed**.

## 5. Create the First Commit

Create a commit to save the current version of the project:

```bash
git commit -m "Initial project upload"
```

Then, the commit message describes the changes being saved.

## 6. Create a Repository on GitHub

Open GitHub in browser and create a new repository.

For example:

```text
Repository name: medical-document-ai
```

>[!Note!]
> If the project already has a local Git repository and commits, it is recommended to create the GitHub repository without adding a README file, `.gitignore`, or license during the initial setup.

## 7. Connect the Local Repository to GitHub

Copy the HTTPS URL of the GitHub repository:
i) Click to the green button `<> Code` 
ii) Copy the link in section HTTPS

Example:

```text
https://github.com/njwasykri/medical-document-ai.git
```
Add the GitHub repository as the remote repository:

```bash
git remote add origin https://github.com/njwasykri/medical-document-ai.git
```
If a remote named `origin` already exists, use:

```bash
git remote set-url origin https://github.com/njwasykri/medical-document-ai.git
```

## 8. Verify the Remote Repository

Check that the project is connected to the correct GitHub repository:

```bash
git remote -v
```

The output should look similar to:

```text
origin  https://github.com/njwasykri/medical-document-ai.git (fetch)
origin  https://github.com/njwasykri/medical-document-ai.git (push)
```

## 9. Set the Main Branch

Rename the current branch to 'main':

```bash
git branch -M main
```

##10. Push the Project to GitHub

Push the local project to GitHub:

```bash
git push -u origin main
```

> [!Note]
> The first push may require GitHub authentication through a web browser.
> After a successful authentication, the project files will appear in the GitHub repository.
 



