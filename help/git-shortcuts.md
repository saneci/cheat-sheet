# Git commonly used commands

## Table of content

1. [Updating Git](#updating-git)
2. [Clone repository via ssh](#clone-repository-via-ssh)
3. [Managing remote repositories](#managing-remote-repositories)
4. [Pull changes](#pull-changes)
5. [Show changes](#show-changes)
6. [Commit changes](#commit-changes)
7. [Delete commit](#delete-commit)
8. [Delete branch](#delete-branch)
9. [Push changes](#push-changes)
10. [Rebase](#rebase)
11. [Tags](#tags)
12. [Resolve problems](#resolve-problems)

## Updating Git

- `git --version` - check Git version
- `git update` - in versions between 2.14.2 and 2.16.1
- `git update-git-for-windows` - since Git 2.16.1

## Clone repository via ssh

- `ssh-keyscan -t rsa github.com`
- `git clone git@github.com:{company_or_username}/{repository}.git` - before that you should add your rsa public key
  into Git server account

## Managing remote repositories

- `git remote add origin {repository_url}` - set a new remote
- `git remote set-url origin {repository_url}` - update the remote URL, for example after the repository was renamed
  or moved, or to switch from `https` to `ssh`
- `git remote -v` - verify new remote
- `git branch --set-upstream-to origin/{branch_name}`

## Pull changes

- `git fetch origin` - pull all changes and new branches from origin, but not merge
- `git fetch origin --prune` - prune remote-tracking branches no longer on remote

## Show changes

- `git status`
- `git log --all --decorate --oneline --graph` - show git branch graph

## Commit changes

- `git add {file_name}` - stage changes of a file
- `git add .` - stage all changes
- `git commit -m "{commit_message}"` - commit staged changes
- `git commit -am "{commit_message}"` - stage tracked files and commit in one command

## Delete commit

- `git reset --hard HEAD~1` - delete ALL changes, the HEAD~1 means the one commit before head
- `git reset --hard {commit_id}` - delete ALL changes by commit ID
- `git reset --soft HEAD~1` - delete just the commit, that approach keeps your work and changes will be restored,
  the HEAD~1 means the one commit before head
- `git push origin HEAD --force` - if you already pushed it, you will need to do a force push to get rid of it

## Delete branch

- `git branch -d {branch_name}` - delete already merged branch
- `git branch -D {branch_name}` - delete branch force
- `git push origin -d {branch_name}` - delete remote branch

## Push changes

- `git push --set-upstream origin {branch_name}` - push to a new branch

## Rebase

- `git rebase --onto {branch_name}` - rebase current branch onto specified branch
- `git rebase {branch_name}` - rebase current branch onto specified branch

## Tags

- `git tag` - show tag list
- `git tag -a v1.0.0 -m "{tag_message}"` - create annotated tag
- `git show v1.0.0` - show expanded info about annotated tag
- `git tag v1.0.0` - create lightweight tag
- `git tag -d v1.0.0` - delete tag if it is not already pushed
- `git push origin --delete v1.0.0` - delete tag from remote server
- `git push origin tag {tag_name}` - push tag to a remote server

## Resolve problems

- `git commit --amend -m "an updated commit message"` - change commit message
- `git commit --amend --no-edit` - the `--no-edit` flag will allow you to make changes to a commit without changing its
  comment
