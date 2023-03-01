# Day 10 Task:

### **Git Branching:-**

A branch is a version of the repository that is separate from the main working project. It is a feature available in most modern version control systems. A Git project can have more than one branch. These branches are a pointer to a snapshot of your changes.

### Create Branch:-

You can create a new branch with the help of the **git branch** command. This command will be used as:

**Syntax:**

$ git branch  **&lt;branch** name\*\*&gt;\*\*

### List Branch

You can List all of the available branches in your repository by using the following command.

Either we can use the **git branch - list** or **git branch** command to list the available branches in the repository.

**Syntax:**

$ git branch --list

### Delete Branch

You can delete the specified branch. It is a safe operation. In this command, Git prevents you from deleting the branch if it has unmerged changes. Below is the command to do this.

**Syntax:**

git branch -d\*\*&lt;branch\*\* name\*\*&gt;\*\*

### Switch Branch

Git allows you to switch between the branches without making a commit. You can switch between two branches with the **git checkout** command. To switch between the branches, the below command is used:

$ git checkout &lt;branch name&gt;

**Switch from master Branch**

You can switch from master to any other branch available on your repository without making any commit.

### Merge Branch

Git allows you to merge the other branch with the currently active branch. You can merge two branches with the help of **git merge** command. Below command is used to merge the branches:

**Syntax:**

$ git merge **&lt;branch** name

## **Git Revert and Reset**

### Git Revert

In Git, the term revert is used to revert some changes. The git revert command is used to apply the revert operation. It is an undo-type command. However, it is not a traditional undo alternative. It does not delete any data in this process; instead, it will create a new change with the opposite effect and thereby undo the specified commit. Generally, git revert is a commit.

Two commonly used tools that git users will encounter are of git reset and git revert. The benefit of both of these commands is that you can use them to remove or edit changes you’ve made in the code in previous commits.

## **<mark>Git Rebase and Merge</mark>**

### What Is Git Rebase?

Git rebase is a command that lets users integrate changes from one branch to another, and the logs are modified once the action is complete. Git rebase was developed to overcome merging’s shortcomings, specifically regarding logs.

### What Is Git Merge?

Git merge is a command that allows developers to merge Git branches while the logs of commits on branches remain intact.

The merge wording can be confusing because we have two methods of merging branches, and one of those ways is called “merge,” even though both procedures do essentially the same thing.

### Task 1:

Add a text file called version01.txt inside the Devops/Git/ with “This is the first feature of our application” written inside. This should be in a branch coming from master, \[hint try git checkout -b dev\], switch to the dev branch ( Make sure your commit message will reflect as "Added new feature"). \[Hint use your knowledge of creating branches and Git commit command\]

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677259757651/fcd38bd2-acf6-48fd-8931-88f22d2eafd1.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677259780327/5a0fdaf1-9984-4b92-b945-a23dc7f73553.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677259801497/7d14b461-e632-4b67-b819-456e58aa4352.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677259820881/90c67c34-2dee-4b47-adb5-7493ecd1d195.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677259842877/e1e5a149-71d8-4b29-b976-31878e3492b5.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677259866349/f97fd95b-5f72-4fe1-a5e5-570d4979b8b4.png align="center")

Add a new commit in dev branch after adding the below-mentioned content in Devops/Git/version01.txt: While writing the file make sure you write these lines

1st line&gt;&gt; This is the bug fix in development branch

Commit this with message “ Added feature2 in development branch”

2nd line&gt;&gt; This is gadbad code

Commit this with message “ Added feature3 in development branch

3rd line&gt;&gt; This feature will gadbad everything from now.

Commit with message “ Added feature4 in development branch

Restore the file to a previous version where the content should be “This is the bug fix in development branch” \[Hint use git revert or reset according to your knowledge\]

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677260082840/74a280ef-733a-417e-a2ec-228d6780949d.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677260175236/a09bcd4e-3c30-4c7e-bd1d-72366f5aa165.png align="center")

### Task 2:

Demonstrate the concept of branches with 2 or more branches with screenshot. add some changes to dev branch and merge that branch in master as a practice try git rebase too, see what difference you get.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677264774976/62d621dc-1001-4202-827c-02fca52c779e.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677264796584/ba8f2082-cf18-4745-891f-05af30559a78.png align="center")

# Git Rebase:-

Rebasing is a process to reapply commits on top of another base trip. It is used to apply a sequence of commits from distinct branches into a final commit. It is an alternative of git merge command. It is a linear process of merging.

In Git, the term rebase is referred to as the process of moving or combining a sequence of commits to a new base commit. Rebasing is very beneficial and it visualized the process in the environment of a feature branching workflow.