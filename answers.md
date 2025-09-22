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
