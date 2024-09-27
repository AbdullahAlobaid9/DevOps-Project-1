# Simple Task Management System Using Git

## 1. Set Up the Repository:

**a. Create a new Git repository in a dedicated directory for the project:**

```
git init task-manager
cd task-manager
```

**b. Create a text file named (tasks.txt) to serve as your simple task database:**

```
touch tasks.txt
```

## 2. Add Initial Tasks:

**a. Add some initial tasks to tasks.txt:**

```
# Added them manually.
# - Learn Git basics
# - Set up Git repository
```

**b. Stage and commit these changes:**

```
git add .
git commit -m "Initial commit with tasks"
```

## 3. Create Branches and Work on Features:

**a. Create and move to a new branch called (feature/add-tasks) to add new tasks:**

```
git checkout -b feature/add-tasks
```

**b. Add more tasks to (tasks.txt) and commit them:**

```
echo "- Practice Git branching" >> tasks.txt
git add .
git commit -m "Added a new task"
```

**c. Create and move to another branch called (feature/remove-tasks) to remove some tasks:**

```
git checkout master
git checkout -b feature/remove-tasks
```

**d. Remove a task from (tasks.txt) and commit the change:**

```
# Manually removed a task.
git add .
git commit -m "Removed first task"
```

## 4. Merge Branches and Handle Conflicts:

**a. Switch to the (master) branch and try to merge (feature/add-tasks) and (feature/remove-tasks) one by one:**

```
git checkout master
git merge feature/add-tasks
git merge feature/remove-tasks
```

**b. If a conflict occurs, resolve it by editing (tasks.txt), keeping the desired changes, then stage and commit the resolution:**

```
# Manually resolve the conflict in tasks.txt
git add .
git commit
# Got the default text of merge branch
```

## 5. Use Git Rebase:

**a. Create and move to a new branch (feature/update-tasks) to update some tasks:**

```
git checkout -b feature/update-tasks
```

**b. Make changes to (tasks.txt) and commit them:**

```
# Updated the first task to "Review Git merge and rebase".
git add .
git commit -m "Updated the first task"
```

**c. Use rebase to integrate changes from (feature/update-tasks) into the (master) branch:**

```
git checkout master
git rebase feature/update-tasks
```

## 6. Use Git Cherry Pick:

**a. Select a specific commit from another branch and add it to the (master) branch using cherry-pick:**

```
# Skipped part according to instructor
```

## 7. Reverting to Previous Commits:

**a. Make an incorrect change to (tasks.txt) and commit it:**

```
echo "- Some incorrect task" >> tasks.txt
git add .
git commit -m "Added incorrect task"
```

**b. Use (git revert) to undo the commit:**

```
git revert HEAD
```

**c. If you want to reset the project to a previous state, use reset:**

```
# Didn't have to use it, since it will remove the commits after the selected point.
```

## 8. Working with Remote Repository:

**a. Create a remote repository on GitHub and link the local repository:**

```
git remote add origin https://github.com/AbdullahAlobaid9/DevOps-Project-1.git
```

**b. Push the local repository to the remote repository:**

```
git push -u origin master
```

## 9. Final task:

- Submit the final repository with this README file explaining what Git commands were used in each part.

```
touch README.md
# Added all the details
git add .
git commit -m "Added README.md file"
```
