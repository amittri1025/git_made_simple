# A simple repository to learn git



## Renaming branches in Git

To set default name for all new branches
```sh
git config --global init.defaultBranch <name>
```

To set for current branch

```sh
git branch -m <name>
```

## Changing and creating branches
To see local branches
```sh
	git branch
```

To see remote branches

```sh
	git branch -r 
```
To see all local and remote branches
```sh
	git branch -a
```


To get a list of all branches from the remote, run this command:
```git pull```

Run this command to switch to the branch:

```sh
git checkout --track origin/my-branch-name
```


Push to a Branch

If your local branch does not exist on the remote, run either of these commands:
```sh
git push -u origin my-branch-name
git push -u origin HEAD`
```

***NOTE: HEAD is a reference to the top of the current branch.***

If your local branch already exists on the remote, run this command:

```sh 
git push
```


## Merging git branches

**Context** : Remote Repo, Local Repo(branch : main and test)
**Target** : Merging test into main.

Steps:

 1. git fetch : get latest updates from the remote(also called origin).
 2. git rebase : bring latest commits of main to your branch.

  ```sh
  git rebase origin/master
 ```

 3. Switch to main branch : ```git checkout master```
 4. Pull changes ```git pull origin main```.

 [Read difference b/w git fetch and git pull](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Git-pull-vs-fetch-Whats-the-difference#:~:text=Difference%20between%20Git%20fetch%20and,git%20pull%20command%20does%20both.)

 ![git pull vs git fetch](https://itknowledgeexchange.techtarget.com/coffee-talk/files/2023/05/git-fetch-vs-merge.gif)

5. Finally Merge , ```git merge test```.
6. Push the changes to github . ```git push origin main```