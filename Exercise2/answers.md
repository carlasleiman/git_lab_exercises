## Step 1: Check current branch
- 'git status' shows the branch you are currently on.
- By default, new repositories are on the 'master' (or 'main') branch.

## Step 2: Create a new branch
- 'git branch my_first_branch' creates a new branch.
- The branch is a pointer to the current commit and allows independent development.

## Step 3: Switch to the new branch
- 'git checkout my_first_branch' moves HEAD to the new branch.
- Now, all commits you make will be on this branch, separate from master.

## Step 4: Commits in the branch
- We added two new files and committed them.
- Each commit is only on 'my_first_branch' and does not affect master.

## Step 5: View latest commits
- 'git log --oneline' shows recent commits on the current branch.
- The two commits we just made are at the top.

## Step 6: Switch back to master
- Commits from 'my_first_branch' do not appear on master yet.
- Files also remain as they were in master.

## Step 7: View commit graph in the branch
- 'git log --graph' shows commits in a visual graph format.
- The commits on 'my_first_branch' appear as a linear branch.
- Using the fancy format gives colors, abbreviations, and relative dates for better readability.

## Step 8: Merge branch into master (fast-forward)
- Because master did not have new commits, merging is fast-forward.
- No merge commit is created.
- The commit graph remains linear.

## Step 9: More commits on branch
- Added two more commits on 'my_first_branch'.
- The branch now has additional changes not present in master.

## Step 10: Commit on master
- Added a new file in master that does not conflict with the branch.
- This ensures merge can be tested without conflicts.

## Step 11: Merge branch into master (with commits on both)
- Git automatically merges changes because there are no conflicts.
- A merge commit is created if there are commits on both master and the branch.

## Step 12: Inspect commit graph after merge
- The DAG (directed acyclic graph) shows master and branch merging.
- Merge commits show where the histories join.
- Git records the parent commits of the merge commit.

## Stretch Task Step 1: Commits on branch
- Added two commits on 'my_first_branch' for testing merge conflicts.

## Stretch Task Step 2: Commit on master
- Edited the same line as in 'my_first_branch' to force a merge conflict.

## Stretch Task Step 3: Merge conflict
- Git detected conflicting changes in file_branch1.py.
- Merge stopped, waiting for conflict resolution.

## Stretch Task Step 4: Status during conflict
- Shows files with conflicts (both staged and unstaged changes).
- Example output: "both modified: Exercise2/file_branch1.py"

## Stretch Task Step 6: Resolve and commit
- After editing and staging, 'git commit' finalizes the merge.
- Conflicts are resolved and the DAG now shows the merge commit.

## Stretch Task Step 7: Commit graph after conflict resolution
- DAG shows branch and master diverged and were joined by the merge commit.
- Conflicts are resolved and history is preserved.
