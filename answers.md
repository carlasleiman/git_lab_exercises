# Exercise 1 – Tracking Files (Main Task)

## Step 1: Initialize Git repository
Answer/Note: This initializes Git in the folder by creating a hidden `.git` directory.
The `.git` directory stores all Git metadata including commits, branches, staging area, and configuration.

## Step 2: Stage README.md
Answer/Note: The README.md file is now in the staging area, ready to be committed.

## Step 3: Commit README.md
Answer/Note: Committing saves a snapshot of the staged file into Git history.

## Step 4: Create src directory and Python files
Answer/Note: We create a folder called src to hold Python files. 
Two empty files, file1.py and file2.py, are created inside the src directory.

## Step 5: Stage and commit src folder
Answer/Note: Adding the directory stages all files inside it. 
Committing saves the snapshot of these files into Git history.

## Step 6: Make a change to file1.py and view diff
Answer/Note: We added a comment line to file1.py. 
The 'git diff' command shows the unstaged changes made to the file.

## Step 7: Stage and commit the change
Answer/Note: After staging, 'git diff' shows nothing because it only displays unstaged changes. 
To see staged changes, use 'git diff --staged'. 
Committing saves the staged changes into Git history.

## Step 8: Make another change to file1.py (staged vs unstaged)
Answer/Note: 
- After adding a new line to file1.py, 'git status' shows it as modified (unstaged).
- 'git diff' shows only the unstaged changes.
- After staging the change, the file moves to the staging area.
- You can have both staged and unstaged changes in a single file.
- Committing saves the staged changes into Git history.

## Step 9: View commit history
Answer/Note: 
- 'git log --oneline' displays all commits in the repository in a concise format.
- Each commit has a unique identifier (commit hash) and the commit message.

## Step 10: View a specific commit
Answer/Note:
- You can type the first 7 characters of the commit ID; Git recognizes it uniquely.
- 'git show <commit-id>' displays the details of a single commit including changes made, author, and message.

## Step 11: Make a couple more commits
Answer/Note:
- New files or updates to existing files are staged with 'git add' and committed with 'git commit'.
- Each commit represents a snapshot of the repository at that point in time.

## Step 12: Staged vs Unstaged changes
Answer/Note:
- You can have both staged and unstaged changes in a single file.
- 'git diff' shows unstaged changes.
- 'git diff --staged' shows staged changes.
- Committing saves the staged changes into Git history.

## Step 13: View commit history
Answer/Note:
- 'git log --oneline' shows all commits in short format.
- Example of commit history so far:
    - 3f0f4b0 Add print statement to file1.py
    - 2fba0e4 Update file1.py with comment
    - be97b77 Add src directory with file1.py and file2.py
    - 5de19d4 Add README file

## Step 14: View a specific commit
Answer/Note:
- You can type the first 7 characters of a commit ID to uniquely identify it.
- 'git show <commit-id>' displays all details of that commit: author, date, commit message, and changes.

## Step 15a: Add a new file
Answer/Note:
- 'touch src/file3.py' creates a new empty file.
- 'git add' stages it for commit.
- 'git commit' saves it into Git history.

## Step 15b: Update README.md
Answer/Note:
- Adding new content to an existing file creates changes.
- 'git add' stages the changes, and 'git commit' saves them.
- Each commit represents a snapshot of the repository at that moment.

Stretch Task 1:
- Using `git rm` deletes the file and stages the deletion automatically.
- After running `git status`, the file shows as deleted and ready to commit.
- Committing finalizes the deletion in the Git history.

### Stretch Task 2: Delete a file using the OS
Answer/Note:
- Deleting a file using the OS removes it from the working directory only.
- `git status` shows the file as "deleted" but it is **not staged** for commit yet.
- Unlike `git rm`, Git did not automatically stage the deletion.

### Stretch Task 3: Stage and commit an OS-deleted file
Answer/Note:
- After deleting a file via the OS, it is not staged automatically.
- Using `git add -A` or `git rm <file>` stages the deletion.
- `git commit` then records the deletion in Git history.
- Difference vs `git rm`: `git rm` deletes and stages in one step; OS delete requires a separate stage command.

### Stretch Task 4: Rename a file using git mv
Answer/Note:
- `git mv <oldname> <newname>` renames a file and stages it in one step.
- `git status` shows the file as renamed.
- `git commit` finalizes the rename in Git history.

### Stretch Task 5: Rename using OS vs git mv
Answer/Note:
- Renaming a file via the OS shows as deleted + untracked in `git status`.
- Committing now records a deletion and addition, not an explicit rename.
- Git can detect renames later in diffs using similarity, but `git status` will not show "rename".
- To have a proper rename staged, use `git mv`.

### Stretch Task 6: Show the most recent 3 commits
Answer/Note:
- Use `git log -3 --oneline` or `git log --max-count=3 --oneline` to display only the last three commits.
- This is useful to quickly see recent changes without scrolling through full history.
