## What is git?

- Git is a way of keeping track of your code
- Every time you make an important change in your code, you can store a snapshot of it as a commit. The commits are identified by hashes, so no two different commits will be mistaken as the same.
- Projects are kept in repositories, or repos, which are a bundle of commits. 
- Commits are linked to each other, so it is possible to "travel back in time" if needed. You can simply jump to a point in time where your code was in a specific way.
- The most recent commit is called the "head" of the repository
- Keeping the idea of time traveling, it is possible to have multiple timelines in git. They are called branches. While there is a main or master branch in which the production code is kept, there can also be other branches, which are initially copies of the main one, and are often used for trying out new code. If it works, you can merge it with the main. If not, it can just discard it without having to worry about your main application being changed. 

- While git is a way of keeping track of your code, there are many providers that offer storage for your code and your commits. One of the most used ones is Github. The benefits of using such services is that you can easily share and build different parts of your code with your team and other developers.

---------------------------------------------------------------------------------

## Main git commands ([Source](https://zepel.io/blog/13-git-commands/)):

`$ git init`
- This will transform the current directory into a Git repository

`$ git clone <https://url-of-the-repository>`
- The git clone command is used to download the source code from a remote repository. As a convenience, the downloaded version is linked to the origin (the repository from where you downloaded).

`$ git remote rm origin`
- This will disassociate the downloaded current repository from the origin.

`$ git branch <branch-name>`
- This command will create a new branch only in your local system. If you want this to be visible to all the members in the repo, you’ll still have to push the branch.

`$git push -u <remote> <branch-name>`
- Push a newly created branch into the repository

`$ git branch`
`$ git branch --list`
- Commands to view all branches

`$ git branch -d <branch-name>`
- Command to delete a branch

`$ git checkout <branch-name>`
- This will automatically switch you to the branch name you mentioned in the command.

`$ git checkout -b <branch-name>`
- Command that will both create a new branch and automatically switch to it.

`$ git add <file-name>`
- This command will add only a single file to your next commit.

`$ git add -A`
`git add .`
- Add all the files to which changes were made.

`$ git commit -a`
- This will commit all the changes in the directory you’re working in. Once this command is run, you’ll be prompted to enter a commit message.

`$ git commit -am “<commit-message>”`
- You can enter the commit message in the command itself and skip the additional step where you’ll be prompted to enter the commit message.

`$ git push <remote> <branch-name>`
- Push the commits to the remote origin.

`$ git pull <remote>`
- The git pull command allows you to fetch all the changes that your teammates pushed and automatically merge them into your local repo.

`$ git diff`
- This will show you any uncommitted changes in your local repo.

`$ git diff branch1..branch2`
- This will show all the file differences between the two branches.

`$ git diff branch1 branch2 ./path/to/file.txt`
- This command will show a comparison of the changes made to file file.txt across the branches branch1 and branch2.

`$ git stash save “<stash-message>”`
- Git Stash temporarily shelves your work, so you can switch to another 
branch, work on something else, and then come back to this at a later time. This will stash your tracked changes with the message you entered.

`$ git stash save -u`
- If you want to include the untracked files as well.

`$ git stash list`
-  View all the stashed code.

`$ git stash apply`
- This will automatically restore and apply the topmost stash in the stack.

`git stash apply stash@{n}`
- If you want to restore a specific stash "n".

`$ git status`
 - Will tell you:  your current branch, whether your current branch is up to date, if there's anything in the branch that needs to be committed, pushed, or pulled, if you have any files that are either staged or not staged and if you have any files that are created, modified, or deleted.

`$ git log`
- This displays the entire commit history.

- Merge:
`$ git checkout main`
- Switch to the main branch.

`$ git pull`
- Make sure that you update your local main branch. This is important because your teammates might've merged into the main branch while you were working on your feature.

`$ git merge branch`
- If there are no conflicts while pulling the updates, you can finally merge your branch into the main one.
