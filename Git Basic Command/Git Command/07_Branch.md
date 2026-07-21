# Git Branch Commands

## What is a Git branch?

A branch is a separate line of development in Git. It lets you work on new features or fixes without changing the main history until you are ready.

- The default branch is usually `main`.
- You can create new branches to try changes safely.
- You can switch between branches and merge them later.

## Branch commands and examples

1. Create a new branch:

        git branch <branch-name>

   Example:

        git branch feature-login

2. List branches in the repository:

        git branch

   The current branch is marked with `*`.

3. Switch to an existing branch:

        git switch <branch-name>

   Example:

        git switch feature-login

4. Create a new branch and switch to it immediately:

        git switch -c <branch-name>

   Example:

        git switch -c feature-login

5. Merge a branch into the current branch:

        git merge <branch-name>

   Example:

        git merge feature-login

   > This combines the changes from `feature-login` into your current branch.

6. Delete a branch after it is merged:

        git branch -d <branch-name>

   Example:

        git branch -d feature-login

## Merge conflicts

A merge conflict happens when the same part of a file is changed differently in two branches.

- Git will stop the merge and mark the conflict in the file.
- Open the file and choose which change to keep.
- After fixing conflicts, stage the file again and finish the merge with:

        git add <file>
        git commit

> Tip: Use branches for each feature or fix. Keep `main` stable and merge only when the branch is ready.
