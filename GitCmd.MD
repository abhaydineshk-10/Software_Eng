Basic Git commands
--------------------------------------------------------------------------------------
🎯 Objectives
By completing this project, you will learn how to:

Create and clone a Git repository

Track changes using Git

Create commits

Push changes to GitHub

Pull changes from GitHub

Create and manage branches

Merge branches

View Git history and repository status

Work with remote repositories
----------------------------------------------------------------------------------------
GitHub account
A code editor such as VS Code
Verify Git installation:
git --version

Setting Up the Repository
1. Create a Repository on GitHub

-Log in to GitHub.
- Click New repository.
- Give the repository a name, for example:
  course-project-git
- Choose whether the repository should be public or private.
- Click Create repository.

2. Clone the Repository
- Clone the GitHub repository to your local computer:
- git clone <repository-url>

- Example:
  git clone https://github.com/username/course-project-git.git

- Move into the repository directory:
  cd course-project-git

3. Check Repository Status
- The git status command shows the current state of your working directory:
  git status

It tells you which files are:
- Modified
- Untracked
- Staged
- Ready to be committed

4. Add Files to the Staging Area
- Add a specific file:
git add filename

- Add all changed files:
 git add .

5. Commit Changes
- A commit saves the staged changes to the local Git repository:
 git commit -m "Add project files"

6. Push Changes
-The git push command uploads local commits to GitHub:
 git push

- For the first push of a new branch:
 git push -u origin main

7. Pull Changes
- The git pull command downloads changes from the remote repository and integrates them into your current branch:
 git pull

- This is useful when working with other team members or when changes have been made directly on GitHub.

8. Create a Branch:
 git branch feature-branch

- Create and switch to a new branch:
 git switch -c feature-branch

- Older Git versions also support:
 git checkout -b feature-branch

9. View Branches:
 git branch

- The current branch is marked with *.

10. Switch Branches:
 git switch main
Or:
 git switch feature-branch

- Merging Branches
 After completing work on a feature branch, it can be merged into the main branch.

- First, switch to the main branch:
 git switch main

- Make sure the main branch is up to date:
 git pull

- Merge the feature branch:
 git merge feature-branch

- Then push the updated main branch:
 git push

- Deleting a Branch
 After successfully merging a branch, the local branch can be deleted:
 git branch -d feature-branch


- To delete a remote branch:
 git push origin --delete feature-branch

- Viewing Git History
View the commit history:
git log

- A compact version:
git log --oneline

Comparing Changes
- View changes that have not been staged:
 git diff

- View staged changes:
 git diff --staged

- Working with Remote Repositories
 View configured remote repositories: 
 git remote -v

- Add a remote repository:
 git remote add origin <repository-url>


- Download information about remote branches:
 git fetch

 Undoing Changes
- Discard changes to a file that have not been committed:
 git restore filename


- Unstage a file:
 git restore --staged filename

 Practice Workflow
 The following workflow demonstrates a typical Git development process:

# Clone repository
git clone <repository-url>

# Enter repository
cd course-project-git

# Create a feature branch
git switch -c feature-branch

# Create or modify files
# ...

# Check changes
git status

# Stage changes
git add .

# Commit changes
git commit -m "Add feature"

# Push branch to GitHub
git push -u origin feature-branch

# Switch to main
git switch main

# Get latest changes
git pull

# Merge feature branch
git merge feature-branch

# Push merged changes
git push
