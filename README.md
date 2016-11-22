####### GIT Workflow

###### Checkout remote branch locally

## Create a local branch. Tie to remote branch and get the code from remote branch
git pull
new local_branch

### Make changes locally. Submit a diff.
git add *
com “Improved feature”
push local_branch
# Request a pull. Wait for comments from reviewers

### Respond to diff
new respond_to_comments
git branch --set-upstream-to=origin/local_branch respond_to_comments
git pull

