# Git File Modification Commands

This lesson explains how to modify commits using an interactive rebase from the root of the repository.

## Modify commit history with interactive rebase

1. Start an interactive rebase from the first commit:

        git rebase -i --root

   This opens an editor with the list of all commits from the very first commit to the current one.

2. In the editor, you can change how each commit is applied:

   - `pick` keeps the commit as-is.
   - `reword` lets you change the commit message.
   - `edit` lets you pause at that commit to change the files.
   - `squash` combines this commit into the previous commit.
   - `fixup` combines this commit into the previous commit and discards this commit message.

3. Example: change a commit message

   - Run `git rebase -i --root`
   - Find the commit you want to change and replace `pick` with `reword`.
   - Save and close the editor.
   - Git opens a new editor window for you to write the new commit message.

4. Example: combine two commits into one

   - Run `git rebase -i --root`
   - For the second commit, replace `pick` with `squash`.
   - Save and close the editor.
   - Git merges the changes and lets you edit the combined commit message.

## When to use this

Use interactive rebase when you want to clean up commit history before sharing it:

- fix typo or improve commit messages
- combine small commits into a single, cleaner commit
- remove or rearrange commits

> Warning: avoid rewriting published history. Only use `git rebase -i --root` on local branches that are not shared with others.
