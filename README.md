# GIT Workflow

## Checkout remote branch locally

#### Create a local branch. Tie to remote branch and get the code from remote branch
git pull

new branches_with_new_changes

#### Make changes locally. Submit a diff.
git add *

com “Improved feature”

push branches_with_new_changes

Request a pull. Wait for comments from reviewers

### Respond to diff comments

new respond_to_comments

git branch --set-upstream-to=origin/branches_with_new_changes respond_to_comments

git pull

acom

git push origin HEAD:branches_with_new_changes

