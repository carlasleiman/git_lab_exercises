## Step 1: Create and switch to branch
- Created branch 'undoing_changes' to experiment with undoing changes.
- Using 'git checkout' switches HEAD to the new branch.

## Step 2: Commit file3.py
- file3.py is added and committed. This snapshot is now in Git history.

## Step 3: Edit and diff
- 'git diff' shows the unstaged changes in file3.py.

## Step 4: Discard changes
- 'git checkout -- file3.py' reverts the working directory file to the last committed version.
- Status shows no changes.
- The changes from step 3 are lost in the working directory.
- Alternative: 'git restore file3.py' can achieve the same effect.

## Step 5: Commit file4.py
- file4.py is added and committed. Snapshot added to branch history.

## Step 6: Revert commit
- 'git revert' creates a new commit that undoes the changes of the specified commit.
- Unlike 'checkout', it preserves history and doesn’t remove the commit.

## Step 7: New commit with multiple files
- Both files changed and committed together.

## Step 8: Soft reset
- Moves HEAD to previous commit but keeps changes staged.
- The previous commit is "undone" in terms of history but not lost; changes remain in staging.

## Step 9: Mixed reset
- Moves changes from staged to unstaged (working directory unchanged).
- Default scope is 'mixed'.
- HEAD remains the same; only the staging area is affected.

## Step 10: Hard reset
- Both working directory and staging area are reset to HEAD.
- All changes after the last commit are lost.
- Default value used: HEAD.

## Step 11: Commit history verification
- Log shows commits remaining after resets and reverts.

## Step 12: Add file5.py
- Added a new file and committed it.

## Stretch Step 1: Edit tracked file
- file5.py is modified but not staged.
- 'git status' shows it as modified.

## Stretch Step 2: Undo changes
- 'git checkout -- file5.py' discards all changes in the working directory for that file.
- The file is restored to the last committed state.
- HEAD pointer does not move; only the working directory changes.

## Stretch Step 3: Two new commits
- Each commit changes a different file and adds a snapshot to Git history.

## Stretch Step 4: Revert multiple commits
- 'git revert HEAD~2..HEAD' creates new commits that undo changes of the specified range.
- Commit history grows; the original commits remain.
- Syntax explanation: HEAD~2..HEAD means "the last two commits up to HEAD".
- Cannot use this same syntax with 'git reset'; reset handles HEAD differently.

## Stretch Step 5: Commit history check
- Log shows that revert commits were added after the original commits.
- History is preserved, unlike reset which can remove commits.

## Stretch Step 6: Anchor branch
- 'anchor' branch points to current commit to avoid losing history during testing.

## Stretch Step 7: Reset 3 commits back
- Moves HEAD three commits back.
- Working directory may keep changes (depending on reset type; default is mixed).
- Anchor branch can be used to restore previous state.

## Stretch Step 8: Test reset scopes
- Soft: moves HEAD but keeps staged changes.
- Mixed: moves HEAD and unstages changes (default).
- Hard: resets HEAD, staging area, and working directory to the anchor commit.

**Files included in this folder:**
- file3.py — created and committed as part of the Undoing Changes exercise.
- file5.py — created for the stretch task and used in reset/checkout examples.
