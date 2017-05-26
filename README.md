# Markdown-Editor
UWP Professional markdown editor

## Git Rules
Using git is easy, using multiple granches can be a bit tricky. There is one branch per release, when the release is complete the branch is to be merged into master. NO COMMITS must be made to master.

Any changes to gitignore, or to gitatributes must be done on the branch git, this branch can then be merged into the release branch or what ever branch in order to get the commit. This beanch should be based on master and never merge other branches than master into it.

Documentation changes should be made on the **docs** branch. This branch should always be based on master and never merge changes from other branches into it.

### Note
Changes to either git or docs should be merged in the master branch since it is safe to do so. Other branches should then be updated from master to get the latest changes to documentation and git config.

> Github's desktop application does weird stuff with merge and branches. It will merge from remote and not local, therefore if there are changes on a branch that arent pushed, they will not be merged. Sync your remote branch before merging. **The more you know!** Or you could merge using github.com as well.
