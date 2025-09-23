This creates a new branch feature-branch and switches to it immediately.

Equivalent to doing git branch feature-branch followed by git checkout feature-branch.

We added a new file in the feature-branch.

Committing saves the snapshot of this new file.

Switching to master branch to make changes independent of feature-branch.
New file added in master.

Its commit is separate from feature-branch.

Shows the commit history for all branches.

At this point, feature-branch and master have diverged.
Rebasing moves the feature-branch commits on top of the master branch.

The master branch becomes the new base.

Difference vs merge: Rebase rewrites history to make it linear, no merge commit is created.

We intentionally modified feature1.py on master to create a conflict for the rebase.

This simulates real-world scenarios where multiple branches edit the same file.
Now both branches have conflicting changes in the same file.