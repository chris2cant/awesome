# Git

I created this guide to help everyone to execute git command step by step.
This guide follows the oneflow method. Everything in this guide merge my experience, articles and feedbacks. 

## Table of Contents
- [:wrench: Config](#config)
	- [User](#config-user)
	- [Git log](#config-git-log)
	- [Generate an SSH keys](#config-ssh-key)
- [:hammer_and_wrench: Tools](#tools)
- [:floppy_disk: Versioning](#versioning)
	- [Example](#versioning-example)
- [:rocket: Commands](#commands)
	- [:building_construction: Feature](#feature)
		- [Start feature](#start-feature)
		- [Finish feature](#finish-feature)
	- [:gem: Release](#release)
		- [Start release](#start-release)
		- [Finish release](#finish-release)
	- [:fire: Hotfix](#hotfix)
		- [Start hotfix](#start-hotfix)
		- [Finish hotfix](#finish-hotfix)
	- [:scissors: Squash commit](#squash-commit)
	- [Show commit timestamp](#commit-timestamp)
	- [Pull with auto stash](#pull-autostash)
- [✨Remove deleted branches](#remove-deleted-branches)
- [:pushpin: Pinned articles](#pinned-article)


<a name="config"/>

## :wrench: Config

<a name="config-user"/>

### User

Configure your user

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

Display your config

```sh
git config --list
```

<a name="config-git-log"/>

### Git log

```sh
# Alias for a pretty git log
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
# Execute the alias of the pretty git log
git lg
```

### Generate an SSH keys

Generate an SSH key with passphrase. **Set a Passphrase is strongly recommended !**

```sh
# -t : Type [dsa | ecdsa | ed25519 | rsa]
# -b : Bits
# -C : Comment (at the end of id_rsa.pub)
# PLEASE ! Replace "johndoe@example.com" with your email address
ssh-keygen -t rsa -b 4096 -C "johndoe@example.com"
```

<a name="tools"/>

## :hammer_and_wrench: Tools

A list of git tools :
- [Gitkraken](https://www.gitkraken.com/)
- [Sourcetree](https://www.sourcetreeapp.com/)
- [Ungit](https://github.com/FredrikNoren/ungit)
- [Gitflow](https://danielkummer.github.io/git-flow-cheatsheet/index.fr_FR.html)
- [Oneflow CLI](https://github.com/Workable/oneflow)
- [Gitmoji](https://gitmoji.carloscuesta.me/)

<a name="versioning"/>

## :floppy_disk: Versioning (X.Y.Z)


`SemVer` is the versioning method I follow for my projects.

```txt
X (major release) : MAJOR version when you make incompatible API changes.
Y (feature)       : MINOR version when you add functionality in a backwards-compatible manner.
Z (hotfix)        : PATCH version when you make backwards-compatible bug fixes.
```

On a git project 

```txt
X : Major release
Y : A new feature
Z : A hotfix
```

[Go to semver.org for more informations](https://semver.org/)

<a name="versioning-example"/>

### Example

This is an example from a bike to an electric motorbike.

```sh
# MAJOR - ("incompatible API changes")
[1.0.0]  - A Bike

# MINOR - "Backwards-compatible"
[1.1.0]  - Add front light

# MINOR - "Backwards-compatible"
[1.2.0]  - Add back light

# PATCH - "Backwards-compatible bug fixes"
[1.2.1]  - Fix the back light

... 21 features later ...

# MAJOR - New law for electric bike. ("incompatible API changes")
[2.0.0]  - Add electric motor : Electric Bike

... 43 features later ...

# PATCH - "Backwards-compatible bug fixes"
[2.43.23] - Fix the battery issue 

# MAJOR - New law for electric bike with acceleration handle  ("incompatible API changes")
[3.0.0]  - Remove pedals - Add acceleration handle - Electric motorbike
```

<a name="commands"/>

## :rocket: Commands

### Init

```sh
# Init a git repository
git init
```

<a name="feature"/>

### :building_construction: Feature

<a name="start-feature"/>

#### Start feature 

```sh
# Create a feature branch
# -b : New branch
git checkout -b feature/my-feature
# Publishing this local branch on the remote server
# After having set upstream you can use only "git push" instead "git push origin feature/my-feature"
# -u : Set upstream [-u | --set-upstream]
git push -u origin feature/my-feature
```

<a name="finish-feature"/>

#### Finish feature 

```sh
# Start to pull master to be up to date
git checkout master
git pull
# Go to the feature branch
git chekout feature/my-feature
# Pull to be up to date (To be sure)
git pull
# Rebase with master and resolve conflicts
git rebase master
# During conflic add your files with `git add yourfile`
# Use git rebase --continue after file conflict
# Push force (-f) because you rewrite your feature origin 
git push -f origin feature/my-feature

# Create a merge request or merge in command line
```

##### Case 1 : Rebase

```sh
# Switch to master
git checkout master
# Rebase the feature in master
git rebase feature/my-feature
git push
# Remove the branch locally
git branch -d feature/my-feature
# Remove the branch remotely
git push origin :feature/my-feature
```

<a name="release"/>

### :gem: Release

<a name="start-release"/>

#### Start release 

```sh
# Create a release branch
git checkout -b release/1.0.0
# Publishing this local branch on the remote server
git push -u origin release/1.0.0
```

<a name="finish-release"/>

#### Finish release 

```sh
git checkout release/1.0.0
# New version for a major feature X(+1).Y.Z (Example : 1.0.0 -> 2.0.0)
# New version for a minor feature X.Y(+1).Z (Example : 1.0.0 -> 1.1.0)
git tag 1.0.0
git checkout master
git merge release/1.0.0
# Important : --tags push the tag
git push --tags origin master
# Remove the branch locally
git branch -d release/1.0.0
# Remove the branch remotely
git push origin :release/1.0.0
```

<a name="hotfix"/>

### :fire: Hotfix

<a name="start-hotfix"/>

#### Start hotfix 

```sh
git checkout master
# Create a branch hotfix from the tag 1.0.0
git checkout -b hotfix/1.0.1 1.0.0
# Publishing this local branch on the remote server
git push -u origin hotfix/1.0.1
```

<a name="finish-hotfix"/>

#### Finish hotfix 

Hotfix version should increase the z part (Version x.y.z)

```sh
git checkout hotfix/1.0.1
# New version for a hotfix X.Y.Z(+1) (Example : 1.0.0 -> 1.0.1)
git tag 1.0.1
git checkout master
# Merge the hotfix in master
git merge hotfix/1.0.1
# Important : --tags push the tag
git push --tags origin master
# Remove the branch locally
git branch -d hotfix/1.0.1
# Remove the branch remotely
git push origin :hotfix/1.0.1
```

<a name="squash-commit"/>

### :scissors: Squash commit

Squash commit is a good practice to keep a clean git log 

```sh
# Display logs
git lg
```

In this example we have two commits for the same feature. If we want to keep only one commit message we can squash it in one !

```sh
* 4c23828 - (HEAD -> master, origin/master) [mySecondFeature] - Add the second method (3 minutes ago) <Chris>
* efd6cee - [mySecondFeature] - Add the first method (4 minutes ago) <Chris>
* 6987662 - [myFirstFeature] - Add the first feature(12 minutes ago) <Chris>
* 092b49f - Initial commit (22 hours ago) <Chris>
```

Go to the commit just before "mySecondFeature"

```sh
# Rebase 
# -i : Interactive
# Commit hash
git rebase -i 6987662
```

Your terminal will show you `vim` with this content

```txt
pick efd6cee [mySecondFeature] - Add the first method 
pick 4c23828 [mySecondFeature] - Add the second method
```

Change `pick` by `squash` for the last commit you wand to squash. When you are done, save it !

```
pick efd6cee [mySecondFeature] - Add the first method 
squash 4c23828 [mySecondFeature] - Add the second method
```

Your terminal will show you `vim` with this new content.

```
# This is a combination of 2 commits.
# This is the 1st commit message:

[mySecondFeature] - Add the first method 

# This is the commit message #1:

[mySecondFeature] - Add the second method
```

Now you can comment with `#` the last commit and rename the commit message you want to keep. When you are done, save it !

```
# This is a combination of 2 commits.
# This is the 1st commit message:

[mySecondFeature] - Add the second feature

# This is the commit message #1:

#[mySecondFeature] - Add the second method
```

Push your changes

```sh
# Push with force because you made a rebase
git push -f origin master
```

Verification 

```sh
# Display logs
git lg
```

Now you have one commit per feature. It's cleaned !

```txt
* 4c23828 - (HEAD -> master, origin/master) [mySecondFeature] - Add the second feature (3 minutes ago) <Chris>
* 6987662 - [myFirstFeature] - Add the first feature(12 minutes ago) <Chris>
* 092b49f - Initial commit (22 hours ago) <Chris>
```

That's it !

<a name="pull-autostash"/>

### Pull with auto stash

```sh
# Pull your branch without commit your changes
# 1. Stash your code
# 2. Pull your code
# 3. Stash pop your code
git pull --autostash
```

<a name="commit-timestamp"/>

### Show commit timestamp

```sh
# -s : Suppresses the diffs from showing
# %ct : committer date, UNIX timestamp
git show -s --format=%ct
# Result :
# 1577785324
```

<a name="remove-deleted-branches"/>

### Remove deleted branches

```sh
# git branch -vv : list local branches and information about remote branches ("gone” if it's deleted)
# grep ': gone]' : Keep only "gone" branches
# grep -v "\*" : Avoid current branch (contain an asterisk)
# awk '{print $1}' : Print only the branch name
# xargs git branch -D : Force to delete each branch
git branch -vv | grep ': gone]' | grep -v "\*" | awk '{print $1}' | xargs git branch -D
```

<a name="pinned-article"/>

## :pushpin: Pinned articles

- [OneFlow - a Git branching model and workflow](https://www.endoflineblog.com/oneflow-a-git-branching-model-and-workflow)
- [Show Emoji in Git Log!](https://ahmadawais.com/show-emoji-git-log/)

## Sources

- [OneFlow - a Git branching model and workflow] - https://www.endoflineblog.com/oneflow-a-git-branching-model-and-workflow
- [SemVer](https://semver.org/)
- [Delete local Git branches that where deleted on remote repository](https://medium.com/@kcmueller/delete-local-git-branches-that-were-deleted-on-remote-repository-b596b71b530c)
