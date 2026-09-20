# Git & GitHub CLI Commands

## Git Local SetUp

* Check git version

`git -v`

* If git is not installed

`sudo apt update`

`sudo apt install git`

* Setup git configuration

`git config --global user.name "your_username"`

`git config --global user.email "name@example.com"`

* Show git configuration

`git config -l`

* Show global git configuration

`git config --global --list`

* Check configured username

`git config user.name`

* Check configured email

`git config user.email`

* Initialize git repository

`git init`

* Checkout branch

`git checkout -b <branchname>`

* Switch to existing branch

`git checkout <branchname>`

* Pull the changes

`git pull`

## Git Commands

| Command | Usage | Example |
|-------|-----------|---------|
| `git init` | initialize a repo inside directory | `git init` |
| `git clone <url>` | clone an existing repo | `git clone https://github.com/NishantBhangale/90DaysOfDevOps.git` |
| `git add file` | add a file to staging | `git add demo.txt` |
| `git add .` | add all changes to staging | `git add .` |
| `git add -A` | add all changes including deleted files | `git add -A` |
| `git commit` | make a commit | `git commit -m "added demo.txt"` |
| `git reset file` | remove a file from staging | `git reset demo.txt` |
| `git status` | check if anything to commit/add | `git status` |
| `git log` | check commit history | `git log` |
| `git log --oneline` | show compact commit history | `git log --oneline` |
| `git log --oneline --graph --all` | show commit graph for all branches | `git log --oneline --graph --all` |
| `git show <commit-id>` | show details of a commit | `git show 4ae73` |
| `git revert <commit-id>` | creates a new commit that undoes changes made by given commit | `git revert 4ae73` |
| `git reset <commit-id>` | reset HEAD back to given commit | `git reset 2sd3i` |
| `git reset --soft <commit-id>` | reset commit but keep changes staged | `git reset --soft 4ae73` |
| `git reset --mixed <commit-id>` | reset commit and unstage changes | `git reset --mixed 4ae73` |
| `git reset --hard <commit-id>` | reset commit and remove local changes | `git reset --hard 4ae73` |
| `git clean -n` | show untracked files that can be removed | `git clean -n` |
| `git clean -f` | remove untracked files | `git clean -f` |
| `git diff` | show unstaged changes | `git diff` |
| `git diff --staged` | show staged changes | `git diff --staged` |

## Git Branch Commands

| Command | Usage | Example |
|-------|-----------|---------|
| `git branch` | show local branches | `git branch` |
| `git branch -a` | show local and remote branches | `git branch -a` |
| `git branch -r` | show remote branches | `git branch -r` |
| `git branch <branchname>` | create a new branch | `git branch feature-login` |
| `git checkout <branchname>` | switch to a branch | `git checkout feature-login` |
| `git checkout -b <branchname>` | create and switch to a new branch | `git checkout -b feature-login` |
| `git switch <branchname>` | switch to an existing branch | `git switch feature-login` |
| `git switch -c <branchname>` | create and switch to a new branch | `git switch -c feature-login` |
| `git branch -d <branchname>` | delete a merged local branch | `git branch -d feature-login` |
| `git branch -D <branchname>` | force delete a local branch | `git branch -D feature-login` |
| `git branch -M main` | rename current branch to main | `git branch -M main` |

## Git Remote Commands

| Command | Usage | Example |
|-------|-----------|---------|
| `git remote -v` | show remote repositories | `git remote -v` |
| `git remote add origin <url>` | add a remote repository | `git remote add origin git@github.com:NishantBhangale/demo.git` |
| `git remote set-url origin <url>` | change remote repository URL | `git remote set-url origin git@github.com:NishantBhangale/demo.git` |
| `git remote remove origin` | remove a remote | `git remote remove origin` |
| `git remote show origin` | show remote information | `git remote show origin` |

## Git Fetch / Pull / Push

| Command | Usage | Example |
|-------|-----------|---------|
| `git fetch` | download remote changes without merging | `git fetch` |
| `git fetch origin` | fetch changes from origin | `git fetch origin` |
| `git fetch --all` | fetch from all remotes | `git fetch --all` |
| `git fetch --prune` | remove deleted remote-tracking branches | `git fetch --prune` |
| `git pull` | fetch and merge remote changes | `git pull` |
| `git pull origin main` | pull main branch | `git pull origin main` |
| `git pull --rebase origin main` | pull and rebase local commits | `git pull --rebase origin main` |
| `git push` | push current branch | `git push` |
| `git push -u origin main` | push main and set upstream | `git push -u origin main` |
| `git push origin <branchname>` | push a specific branch | `git push origin feature-login` |
| `git push --all origin` | push all local branches | `git push --all origin` |
| `git push origin --delete <branchname>` | delete a remote branch | `git push origin --delete feature-login` |
| `git push --force` | force push changes | `git push --force` |
| `git push --force-with-lease` | safer force push | `git push --force-with-lease` |

## Git Merge Commands

| Command | Usage | Example |
|-------|-----------|---------|
| `git merge <branchname>` | merge another branch into current branch | `git merge feature-login` |
| `git merge --no-ff <branchname>` | create a merge commit even when fast-forward is possible | `git merge --no-ff feature-login` |
| `git merge --squash <branchname>` | combine changes without creating the source branch's commits | `git merge --squash feature-login` |
| `git merge --abort` | abort an active merge | `git merge --abort` |

## Git Rebase Commands

| Command | Usage | Example |
|-------|-----------|---------|
| `git rebase main` | rebase current branch onto main | `git rebase main` |
| `git rebase <branchname>` | rebase onto another branch | `git rebase feature-login` |
| `git rebase -i HEAD~3` | interactively edit last 3 commits | `git rebase -i HEAD~3` |
| `git rebase --continue` | continue after resolving a conflict | `git rebase --continue` |
| `git rebase --skip` | skip the current commit | `git rebase --skip` |
| `git rebase --abort` | abort an active rebase | `git rebase --abort` |

## Git Stash Commands

| Command | Usage | Example |
|-------|-----------|---------|
| `git stash` | temporarily save local changes | `git stash` |
| `git stash push -m "message"` | save changes with a message | `git stash push -m "work in progress"` |
| `git stash list` | show all stashes | `git stash list` |
| `git stash show` | show latest stash summary | `git stash show` |
| `git stash show -p` | show stash changes | `git stash show -p` |
| `git stash apply` | restore stash and keep it | `git stash apply` |
| `git stash pop` | restore stash and remove it | `git stash pop` |
| `git stash drop` | remove latest stash | `git stash drop` |
| `git stash clear` | remove all stashes | `git stash clear` |

## Git Tags

| Command | Usage | Example |
|-------|-----------|---------|
| `git tag` | show tags | `git tag` |
| `git tag <tagname>` | create a tag | `git tag v1.0.0` |
| `git tag -a <tagname> -m "message"` | create an annotated tag | `git tag -a v1.0.0 -m "Release v1.0.0"` |
| `git show <tagname>` | show tag details | `git show v1.0.0` |
| `git push origin <tagname>` | push a tag | `git push origin v1.0.0` |
| `git push origin --tags` | push all tags | `git push origin --tags` |
| `git tag -d <tagname>` | delete local tag | `git tag -d v1.0.0` |
| `git push origin --delete <tagname>` | delete remote tag | `git push origin --delete v1.0.0` |

## Git Cherry-pick

| Command | Usage | Example |
|-------|-----------|---------|
| `git cherry-pick <commit-id>` | apply a specific commit to current branch | `git cherry-pick 4ae73` |
| `git cherry-pick --continue` | continue after resolving conflict | `git cherry-pick --continue` |
| `git cherry-pick --abort` | abort cherry-pick | `git cherry-pick --abort` |

## Git Worktree

| Command | Usage | Example |
|-------|-----------|---------|
| `git worktree list` | show worktrees | `git worktree list` |
| `git worktree add <path> <branch>` | create a worktree | `git worktree add ../feature feature-login` |
| `git worktree remove <path>` | remove a worktree | `git worktree remove ../feature` |

## Git Reflog

| Command | Usage | Example |
|-------|-----------|---------|
| `git reflog` | show previous HEAD positions | `git reflog` |
| `git reflog --all` | show reflog for all refs | `git reflog --all` |

Useful for finding commits or branch positions that appear to have been lost.

## GitHub Remote Names

| Remote | Common Meaning |
|-------|----------------|
| `origin` | Your main remote repository |
| `upstream` | Original repository when working with a fork |

### Add upstream

`git remote add upstream <original-repository-url>`

### Show all remotes

`git remote -v`

### Fetch upstream

`git fetch upstream`

### Merge upstream changes

`git checkout main`

`git merge upstream/main`

### Push updated main

`git push origin main`

## Fork Workflow

```text
Original Repository
        |
        | Fork
        v
Your GitHub Repository
        |
        | Clone
        v
Local Repository
```

### Add original repository as upstream

`git remote add upstream <original-repository-url>`

### Fetch upstream

`git fetch upstream`

### Update local main

`git checkout main`

`git merge upstream/main`

### Push changes to your fork

`git push origin main`

---

# Git Authentication

## HTTPS Remote

`git remote set-url origin https://github.com/username/repository.git`

GitHub HTTPS authentication requires a Personal Access Token instead of a GitHub account password.

## SSH Remote

`git remote set-url origin git@github.com:username/repository.git`

### Test SSH connection

`ssh -T git@github.com`

### Generate SSH key

`ssh-keygen -t ed25519 -C "your_email@example.com"`

### Start SSH agent

`eval "$(ssh-agent -s)"`

### Add SSH key

`ssh-add ~/.ssh/id_ed25519`

---

# GitHub CLI

GitHub CLI command is:

`gh`

## Check GitHub CLI version

`gh --version`

## Check GitHub CLI status

`gh auth status`

## Login to GitHub

`gh auth login`

## Logout

`gh auth logout`

## Login with SSH Git protocol

`gh auth login --git-protocol ssh`

## Setup Git to use GitHub CLI authentication

`gh auth setup-git`

---

# GitHub Repository Commands

## Create a GitHub repository

`gh repo create`

## Create a public repository

`gh repo create <repo-name> --public`

Example:

`gh repo create my-project --public`

## Create a private repository

`gh repo create <repo-name> --private`

## Create repository and clone it

`gh repo create <repo-name> --public --clone`

## Create repository from current directory

`gh repo create <repo-name> --public --source=.`

## Create repository from current directory and push

`gh repo create <repo-name> --public --source=. --push`

## View repository

`gh repo view`

## View repository in browser

`gh repo view --web`

## Clone a repository

`gh repo clone <owner>/<repo>`

Example:

`gh repo clone NishantBhangale/MERN-task-manager`

## Fork a repository

`gh repo fork <owner>/<repo>`

## Fork and clone

`gh repo fork <owner>/<repo> --clone`

## Archive a repository

`gh repo archive <owner>/<repo>`

## Rename a repository

`gh repo rename <new-name>`

## Delete a repository

`gh repo delete <owner>/<repo>`

---

# GitHub Issue Commands

## List issues

`gh issue list`

## Create an issue

`gh issue create`

## Create issue with title

`gh issue create --title "Bug in login"`

## Create issue with title and body

`gh issue create --title "Bug in login" --body "Login is not working"`

## View an issue

`gh issue view <issue-number>`

Example:

`gh issue view 10`

## View issue in browser

`gh issue view 10 --web`

## Close an issue

`gh issue close <issue-number>`

Example:

`gh issue close 10`

## Reopen an issue

`gh issue reopen <issue-number>`

---

# GitHub Pull Request Commands

## List pull requests

`gh pr list`

## Create pull request

`gh pr create`

## Create pull request with title

`gh pr create --title "Add login feature"`

## Create pull request with title and body

`gh pr create --title "Add login feature" --body "Added login functionality"`

## Create pull request and select base branch

`gh pr create --base main`

## View pull request

`gh pr view <pr-number>`

Example:

`gh pr view 15`

## View pull request in browser

`gh pr view 15 --web`

## Checkout pull request

`gh pr checkout <pr-number>`

## Review pull request

`gh pr review <pr-number>`

## Approve pull request

`gh pr review <pr-number> --approve`

## Request changes

`gh pr review <pr-number> --request-changes --body "Please update the validation"`

## Add review comment

`gh pr review <pr-number> --comment --body "Looks good"`

## Merge pull request

`gh pr merge <pr-number>`

## Merge using squash

`gh pr merge <pr-number> --squash`

## Merge using rebase

`gh pr merge <pr-number> --rebase`

## Merge using merge commit

`gh pr merge <pr-number> --merge`

## Close pull request

`gh pr close <pr-number>`

## Reopen pull request

`gh pr reopen <pr-number>`

---

# GitHub Actions

## List workflow runs

`gh run list`

## View a workflow run

`gh run view <run-id>`

## Watch a workflow run

`gh run watch <run-id>`

## Rerun a workflow

`gh run rerun <run-id>`

## Cancel a workflow run

`gh run cancel <run-id>`

## List workflows

`gh workflow list`

## View workflow

`gh workflow view <workflow-name>`

## Run workflow manually

`gh workflow run <workflow-name>`

---

# GitHub Releases

## List releases

`gh release list`

## View release

`gh release view <tag>`

## Create release

`gh release create <tag>`

Example:

`gh release create v1.0.0`

## Create release with title

`gh release create v1.0.0 --title "Version 1.0.0"`

## Create release with notes

`gh release create v1.0.0 --generate-notes`

## Delete release

`gh release delete <tag>`

---

# GitHub Gists

## Create a gist

`gh gist create file.txt`

## Create public gist

`gh gist create file.txt --public`

## List gists

`gh gist list`

## View gist

`gh gist view <gist-id>`

## Delete gist

`gh gist delete <gist-id>`

---

# GitHub Codespaces

## List Codespaces

`gh codespace list`

## Create Codespace

`gh codespace create`

## Connect to Codespace using SSH

`gh codespace ssh`

## Stop Codespace

`gh codespace stop`

## Delete Codespace

`gh codespace delete`

---

# GitHub API

## Get authenticated user

`gh api user`

## Get repository information

`gh api repos/<owner>/<repo>`

Example:

`gh api repos/NishantBhangale/MERN-task-manager`

## List repository issues

`gh api repos/<owner>/<repo>/issues`

## List pull requests

`gh api repos/<owner>/<repo>/pulls`

## List repository branches

`gh api repos/<owner>/<repo>/branches`

---

# Common Git Workflows

## First Push to GitHub

```text
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <repository-url>
git push -u origin main
```

## Daily Git Workflow

```text
git status
git pull
git checkout -b feature-name
```

Make changes.

```text
git add .
git commit -m "Add feature"
git push -u origin feature-name
```

Then create a Pull Request.

```text
gh pr create
```

## Update Feature Branch

```text
git checkout main
git pull origin main
git checkout feature-name
git rebase main
```

If there is a conflict:

```text
git status
```

Resolve the conflict, then:

```text
git add <file>
git rebase --continue
```

If required:

```text
git rebase --abort
```

---

# Git Conflict Workflow

When Git reports a conflict:

```text
git status
```

Open the conflicted file.

Look for:

```text
<<<<<<< HEAD
Your changes
=======
Other branch changes
>>>>>>> branch-name
```

Keep the required changes and remove the conflict markers.

Then:

```text
git add <file>
```

For merge:

```text
git commit
```

For rebase:

```text
git rebase --continue
```

---

# Useful Git Commands

| Command | Usage | Example |
|-------|-----------|---------|
| `git status` | check repository status | `git status` |
| `git branch` | show branches | `git branch` |
| `git remote -v` | show remote URLs | `git remote -v` |
| `git fetch --all` | fetch all remotes | `git fetch --all` |
| `git branch -a` | show all branches | `git branch -a` |
| `git log --oneline --graph --all` | visualize history | `git log --oneline --graph --all` |
| `git reflog` | find previous HEAD positions | `git reflog` |
| `git stash` | temporarily save changes | `git stash` |
| `git cherry-pick <commit>` | apply one commit | `git cherry-pick 4ae73` |
| `git clean -n` | preview untracked files to remove | `git clean -n` |
| `git clean -f` | remove untracked files | `git clean -f` |

---

# Git vs GitHub CLI

| Tool | Purpose |
|-------|---------|
| `git` | Manage local Git repositories and Git history |
| `gh` | Manage GitHub repositories, issues, pull requests, Actions, releases, and more |

Examples:

```text
git commit
```

Creates a local Git commit.

```text
git push
```

Pushes commits to a remote repository.

```text
gh pr create
```

Creates a GitHub Pull Request.

```text
gh issue create
```

Creates a GitHub Issue.

```text
gh run list
```

Shows GitHub Actions workflow runs.

---

# Quick Reference

```text
git init
git clone <url>
git status
git add .
git commit -m "message"
git branch
git checkout <branch>
git checkout -b <branch>
git switch <branch>
git switch -c <branch>
git pull
git fetch
git push
git merge <branch>
git rebase <branch>
git stash
git stash pop
git cherry-pick <commit>
git log --oneline
git diff
git remote -v
git tag
```

## GitHub CLI Quick Reference

```text
gh auth login
gh auth status

gh repo create
gh repo clone <owner>/<repo>
gh repo fork <owner>/<repo>
gh repo view
gh repo view --web

gh issue list
gh issue create
gh issue view <number>
gh issue close <number>

gh pr list
gh pr create
gh pr view <number>
gh pr checkout <number>
gh pr review <number>
gh pr merge <number>

gh run list
gh run view <run-id>
gh run watch <run-id>
gh workflow list
gh workflow run <workflow>

gh release list
gh release create <tag>

gh api user
```
