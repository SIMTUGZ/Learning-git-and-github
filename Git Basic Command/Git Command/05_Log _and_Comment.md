# Git Log and Commit Comment Commands

## Git Log (View Commit History)

These commands help you review your commit history and see what changes were made.

1. Show the full commit history:

        git log

   This displays each commit with author, date, and message.

2. Show a brief one-line summary of each commit:

        git log --oneline

   This is useful for a compact history view.

3. Show commit history with the diff for each commit:

        git log -p

   This shows the exact changes introduced by each commit.

4. Exit the log viewer:

        q

   Use this when `git log` or `git log -p` opens in the pager.

## Commit Comment (Commit Message) Commands

These commands help you write, change, and reset commit messages.

1. Create a new commit with a message:

        git commit -m "your message"

   Use a clear message that explains what changed.

2. Change the last commit message:

        git commit --amend -m "new message"

   This updates the message of the most recent commit. Be careful if you already shared the commit with others.

3. Reset to an earlier commit using the commit ID from `git log --oneline`:

        git reset <commit-id>

   This moves your current branch back to the specified commit, effectively undoing later commits.
