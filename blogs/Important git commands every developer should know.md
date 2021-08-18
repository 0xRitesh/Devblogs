![1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1629298769132/JHgS7k2nq.png)
## Important git commands every developer should know
Since there are many various commands you can use, mastering Git takes time. However, certain commands are used more frequently than others. So, in this article, I will provide and explain the ten most often used Git commands that every developer should be familiar with.

Please note that you must be familiar with the fundamentals of Git in order to comprehend this article.
If you want to learn the basics of git and GitHub. I wrote an article on it in a previous [**blog**](https://wordssaysalot.hashnode.dev/introduction-to-git-and-github-beginners-guide).

This is a list of few commands that you can use frequently on GitHub(git bash) :

![2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622820605669/qOzu48wYB.png)
Everything starts from here. The first step is to initialize a new Git repo locally in your project root. 
The git init command creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository. You can do so with the command below:


```
git init 
``` 


![Frame 15.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622821028125/qMzh27zVX.png)
Git clone is a command for downloading existing source code from a remote repository (like Github, for example). In other words, Git clone basically makes an identical copy of the latest version of a project in a repository and saves it to your computer.

There are a couple of ways to download the source code, but mostly I prefer the clone with HTTPS way:

```
git clone <https://name-of-the-repository-link>
``` 

![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622821093881/sAxojbe08.png)

Branches are quite significant in the world of git. Using branches, several developers may work on the same project at the same time. We can use the git branch command for creating, listing, and deleting branches.

Creating a new branch:

```
git branch <branch-name>
``` 



This command will create a branch locally. To push the new branch into the remote repository, you need to use the following command:

```
git push -u <remote> <branch-name>
``` 

Viewing branches:

```
git branch or git branch --list
``` 


Deleting a branch:

```
git branch -d <branch-name>
``` 


![Frame 18.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622821517747/VzPTBJXD7.png)
This is also one of the most used Git commands. To work in a branch, first, you need to switch to it. We use git checkout mostly for switching from one branch to another. We can also use it for checking out files and commits.

```
git checkout <name-of-your-branch>
``` 


There are some steps you need to follow for successfully switching between branches:

The changes in your current branch must be committed or stashed before you switch
The branch you want to check out should exist in your local
There is also a shortcut command that allows you to create and switch to a branch at the same time:

```
git checkout -b <name-of-your-branch>
``` 


This command creates a new branch in your local (-b stands for the branch) and checks the branch out to new right after it has been created.



![5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622821653145/fMC3rnWeH.png)

The Git status command gives us all the necessary information about the current branch. 

```
git status
``` 

We can gather information like:
Whether the current branch is up to date
Whether there is anything to commit, push or pull
Whether there are files staged, unstaged or untracked
Whether there are files created, modified, or deleted.

![6.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622822105657/hXPn3L1FK.png)
When we create, modify or delete a file, these changes will happen in our local and won't be included in the next commit (unless we change the configurations).
We need to use the git add command to include the changes of a file(s) into our next commit. 

To add a single file:

```
git add <file>
``` 

To add everything at once:

```
git add -A
``` 

Important: The git add command doesn't change the repository and the changes are not saved until we use git commit.


![7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622822294490/CNvpsNQt-.png)
This is maybe the most-used command of Git. Once we reach a certain point in development, we want to save our changes (maybe after a specific task or issue).

Git commit is like setting a checkpoint in the development process which you can go back to later if needed.

We also need to write a short message to explain what we have developed or changed in the source code.

```
git commit -m "commit message"
``` 
Important: Git commit saves your changes only locally.

![8.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622822353319/m-r-in7Y6.png)
After committing your changes, the next thing you want to do is send your changes to the remote server. Git push uploads your commits to the remote repository.

```
git push <remote> <branch-name>
``` 


However, if your branch is newly created, then you also need to upload the branch with the following command:

```
git push --set-upstream <remote> <name-of-your-branch>
or
git push -u origin <branch_name>
``` 

Important: Git push only uploads changes that are committed.

![9.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622822415388/3vhOJpX3S.png)
The git pull command is used to get updates from the remote repo. This command is a combination of git fetch and git merge which means that, when we use git pull, it gets the updates from a remote repository (git fetch) and immediately applies the latest changes in your local (git merge).

```
git pull <remote>
``` 

This operation may cause conflicts that you need to solve manually.

![10.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622822540392/g7Sey6G-8.png)
Sometimes we need to reverse the changes we've made. There are several ways to reverse our modifications locally or remotely (depending on what we require), but we must use these commands with caution to avoid undesired removals.
We can reverse our commits in a more secure manner by using git revert. To view our commit history, we must first run git log.
Now,we just need to specify the hash code next to our commit that we would like to undo:

```
git revert  <hash code>
``` 
The advantage of using git revert is that it doesn't touch the commit history. This means that you can still see all of the commits in your history, even the reverted ones.
Another safety measure here is that everything happens in our local system unless we push them to the remote repo. That's why git revert is safer to use and is the preferred way to undo our commits.

![11.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622822943690/cM8z97sXw.png)
When you've completely finished on your branch and everything is working well, the next step is to merge it with the parent branch. The git merge command is used to do this.

Git merge merges your feature branch and all of its commits back to the master branch. It's critical to remember that you must first be on the branch that you wish to combine with your feature branch.

For example, when you want to merge your feature branch into the master branch:
First you should switch to the  master branch:

```
git checkout master
``` 

Before merging, you should update your local master branch:

```
git fetch
``` 
Finally, you can merge your feature branch into master:

```
git merge <branch-name>
``` 

Hint: Make sure your master branch has the latest version before you merge your branches, otherwise you may face conflicts or other unwanted problems.


![12.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1622823133735/JSQLSa5ZJQ.png)

If you are having trouble remembering commands or options for commands, you can use Git help.

There are a couple of different ways you can use the help command in command line:


```
git command -help :   See all the available options for the specific command
git help --all  :   See all possible commands
 ``` 


<hr>
These are the commands that I believe every developer should know in order to get things done evenly. Please let me know in the comments if you think I've missed anything important or if you think something could be done better.<br><br>
**
Thank you for reading!**
<hr>