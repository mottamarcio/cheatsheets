## GIT

**I. Getting Started**

  * **Installation:** Download and install Git from the official website ([https://git-scm.com/](https://www.google.com/url?sa=E&source=gmail&q=https://git-scm.com/)).
  * **Configuration:**
      * `git config --global user.name "Your Name"`: Set your name.
      * `git config --global user.email "your.email@example.com"`: Set your email.

**II. Basic Workflow**

  * **Creating a Repository:**
      * `git init`: Initialize a new repository in the current directory.
      * `git clone <repository_url>`: Clone an existing repository.
  * **Tracking Changes:**
      * `git status`: Check the status of your working directory.
      * `git add <file>`: Add a file to the staging area.
      * `git add .`: Add all changes to the staging area.
  * **Committing Changes:**
      * `git commit -m "Commit message"`: Commit staged changes with a message.
  * **Working with Remotes:**
      * `git remote add origin <remote_url>`: Add a remote repository.
      * `git push -u origin <branch>`: Push changes to the remote repository.
      * `git pull origin <branch>`: Pull changes from the remote repository.

**III. Branching and Merging**

  * **Branching:**
      * `git branch`: List all branches.
      * `git branch <branch_name>`: Create a new branch.
      * `git checkout <branch_name>`: Switch to a different branch.
      * `git checkout -b <branch_name>`: Create and switch to a new branch.
  * **Merging:**
      * `git merge <branch_name>`: Merge a branch into the current branch.

**IV. Undoing Changes**

  * **Unstaging Changes:**
      * `git reset <file>`: Remove a file from the staging area.
  * **Amending Commits:**
      * `git commit --amend -m "New commit message"`: Modify the last commit.
  * **Reverting Changes:**
      * `git revert <commit_hash>`: Create a new commit that undoes the changes.

**V. Advanced Techniques**

  * **Stashing:**
      * `git stash`: Save changes temporarily without committing.
      * `git stash pop`: Apply the stashed changes.
  * **Rebasing:**
      * `git rebase <branch_name>`: Reapply commits on top of another branch.
  * **Cherry-picking:**
      * `git cherry-pick <commit_hash>`: Apply a specific commit from another branch.
  * **Ignoring Files:**
      * Create a `.gitignore` file to specify files and directories to ignore.

**VI. Viewing History**

  * `git log`: View commit history.
  * `git log --oneline`: View a concise history.
  * `git log --graph`: View history with a graphical representation of branches.

**VII. Remotes**

  * `git remote -v`: List all remote repositories.
  * `git remote show <remote_name>`: Show information about a remote.
  * `git remote rename <old_name> <new_name>`: Rename a remote.
  * `git remote remove <remote_name>`: Remove a remote.

**VIII. Collaboration**

  * **Forking:** Create a copy of a repository on your account.
  * **Pull Requests:** Propose changes to the original repository.

**IX. Resources**

  * **Git Documentation:** [https://git-scm.com/doc](https://www.google.com/url?sa=E&source=gmail&q=https://git-scm.com/doc)
  * **GitHub Help:** [https://help.github.com/](https://www.google.com/url?sa=E&source=gmail&q=https://help.github.com/)
