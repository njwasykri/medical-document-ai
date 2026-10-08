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

## 4. 
