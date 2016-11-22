# GIT Workflow

## Create a new branch
-git pull
-new branches_with_new_changes

## Make changes locally. Submit a diff.
-git add *
-com “Improved feature”
-push branches_with_new_changes
-Request a pull. Wait for comments from reviewers

## Update the diff with the same branch
-git add *
-acom
-push branches_with_new_changes

## Respond to diff comments
-new respond_to_comments
-git branch --set-upstream-to=origin/branches_with_new_changes respond_to_comments
-git pull
-acom
-git push origin HEAD:branches_with_new_changes

