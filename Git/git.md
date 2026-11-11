# Git – Distributed Version Control System

## 1. Introduction

Git is a distributed version control system used to track changes in files and manage software development projects.

It helps developers maintain project history, collaborate with others, and manage different versions of their code.

## 2. What Is Version Control?

Version control is a system that records changes to files over time.

It allows developers to:
- Track modifications.
- Restore previous versions.
- Identify who made changes.
- Compare different versions.
- Collaborate with other developers.

## 3. Types of Version Control Systems

There are three main types:

1. **Local VCS:** Manages versions on a single computer.
2. **Centralized VCS:** Stores project history on a central server. Example: SVN.
3. **Distributed VCS:** Every clone contains repository history. Example: Git.

## 4. Features of Git

- Distributed version control.
- Fast and efficient operations.
- Maintains project history.
- Supports branching and merging.
- Allows offline development.
- Supports collaboration.
- Helps recover previous versions.

## 5. Git Architecture

Git uses three main areas:

- **Working Directory:** Where files are created and modified.
- **Staging Area:** Where changes are prepared before committing.
- **Repository:** Where committed versions are stored.

Basic workflow:

Edit → Stage → Commit

## 6. Installation and Configuration

Git can be installed on Windows, Linux, and macOS.

Download Git from: https://git-scm.com/

Verify installation:

```bash
git --version
```

Configure username:

```bash
git config --global user.name "Your Name"
```

Configure email:

```bash
git config --global user.email "you@example.com"
```

View configuration:

```bash
git config --global --list
```

## 7. Creating a Git Repository

Create a project directory:

```bash
mkdir my-project
cd my-project
```

Initialize Git:

```bash
git init
```

Check repository status:

```bash
git status
```

## 8. Basic Git Commands

Git provides several commands to manage project files and changes.

| Command | Purpose |
|---|---|
| `git status` | Displays repository status |
| `git add .` | Stages all changes |
| `git commit -m "message"` | Saves staged changes |
| `git log` | Displays commit history |
| `git log --oneline` | Displays compact commit history |
| `git diff` | Shows unstaged changes |
| `git diff --staged` | Shows staged changes |
| `git ls-files` | Lists tracked files |

Example:

```bash
git add .
git commit -m "Initial commit"
```

## 9. File Management in Git

Git provides commands to rename, remove, and restore files.

Rename a file:

```bash
git mv old.py new.py
```

Remove a tracked file:

```bash
git rm old.py
```

Unstage a file:

```bash
git restore --staged main.py
```

Discard unstaged modifications:

```bash
git restore main.py
```

The `git revert` command creates a new commit that reverses an earlier commit.

```bash
git revert COMMIT_ID
```

## 10. Ignoring Files Using .gitignore

The `.gitignore` file specifies files and directories that Git should ignore.

Example:

```text
__pycache__/
*.pyc
.env
*.log
data/
```

It is useful for excluding temporary files, cache files, logs, and local configuration files.

## 11. Branching in Git

A branch is an independent line of development.

Branches allow developers to work on different features without directly modifying the main branch.

View branches:

```bash
git branch
```

Create a branch:

```bash
git branch feature-login
```

Switch branches:

```bash
git switch feature-login
```

Create and switch to a new branch:

```bash
git switch -c feature-login
```

## 12. Merging and Merge Conflicts

Merging combines changes from different branches.

Example:

```bash
git switch main
git merge feature-login
```

A merge conflict occurs when Git cannot automatically combine changes.

To resolve a conflict:

1. Open the conflicting file.
2. Identify conflicting sections.
3. Edit and save the correct content.
4. Stage the resolved file.
5. Complete the merge commit if required.

## 13. Connecting Git with GitHub

A local Git repository can be connected to a remote GitHub repository.

Add a remote:

```bash
git remote add origin REPOSITORY_URL
```

View remote repositories:

```bash
git remote -v
```

Rename the branch:

```bash
git branch -M main
```

Push changes:

```bash
git push -u origin main
```

## 14. Clone, Fetch and Pull

### Clone

Creates a local copy of a remote repository.

```bash
git clone REPOSITORY_URL
```

### Fetch

Downloads updates without integrating them into the current branch.

```bash
git fetch origin
```

### Pull

Fetches and integrates remote changes.

```bash
git pull
```

## 15. Tags and Releases

A tag identifies an important point in repository history, often representing a software version.

List tags:

```bash
git tag
```

Create an annotated tag:

```bash
git tag -a v1.0.0 -m "Version 1.0.0"
```

View tag information:

```bash
git show v1.0.0
```

Push a tag:

```bash
git push origin v1.0.0
```

## 16. Merge vs Rebase

Both commands integrate changes from different branches.

**Merge:**
- Combines branch histories.
- May create a merge commit.
- Preserves existing commits.

**Rebase:**
- Replays commits on a new base.
- Creates rewritten commit identities.
- Can produce a linear history.

Example:

```bash
git switch main
git merge feature
```

```bash
git switch feature
git rebase main
```

## 17. Git Development Workflow

A typical Git workflow includes:

1. Create or clone a repository.
2. Create a feature branch.
3. Modify and test files.
4. Stage and commit changes.
5. Push the branch to GitHub.
6. Open a pull request.
7. Review and merge approved changes.

Workflow:

Edit → Stage → Commit → Push → Review → Merge

## 18. Advantages and Limitations

### Advantages

- Free and open-source.
- Fast and efficient.
- Supports offline development.
- Maintains complete project history.
- Enables parallel development.
- Supports collaboration.

### Limitations

- Requires learning Git commands.
- Merge conflicts may require manual resolution.
- Some operations can be confusing for beginners.

## 19. Applications of Git

Git is commonly used for:

- Software development.
- Web development.
- Academic projects.
- Open-source projects.
- Collaborative programming.
- Project maintenance.
- Tracking documentation changes.

## 20. Conclusion

Git is an important distributed version control system that helps developers track changes, maintain project history, manage branches, and collaborate efficiently.

Its commands and branching features make it useful for individual developers as well as large development teams.

## 21. References

1. Git Official Documentation.
2. Git Reference Manual.
3. Git Pro Book.
4. Git and GitHub Lecture Slides.