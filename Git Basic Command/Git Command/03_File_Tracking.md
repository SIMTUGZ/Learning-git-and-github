# Git File Tracking Commands

These commands help you track file changes, stage work, commit updates, and remove files from staging.

1. Check the status of your repository:

        git status

2. Stage files for commit:

   - Stage a specific file:

         git add <file>

   - Stage new and modified files in the current directory:

         git add .

   - Stage all changes, including deletions:

         git add --all

     or:

         git add -A

3. Stop tracking a file but keep it locally:

        git rm --cached <file>

6. Use a `.gitignore` file to exclude files and folders from tracking, such as `node_modules/`, `*.log`, or `.env`.

7. Commit staged changes:

        git commit -m "message"

8. Commit modified and deleted tracked files without staging new files:

        git commit -a -m "message"

9. Show changes that are not yet staged:

        git diff

10. Show changes that are staged and ready to commit:

        git diff --staged

11. Remove a file from the staging area while keeping its changes in the working directory:

        git restore --staged <file>
