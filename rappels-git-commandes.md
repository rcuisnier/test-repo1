# Commandes Git utiles
==========

# Travailler sur un projet Github existant 
## Créer son propre repo à partir d’un projet Github (Fork)
To fork this project, click the "Fork" button in the GitHub.com repository
Unwatch the main repository
When you fork a particularly popular repository, you may find yourself with a lot of unwanted updates about it. To unsubscribe from updates to the main repository, click the "Unwatch" button on the main repository and select "Not Watching".
Delete your fork
At some point you may decide that you want to delete your fork. To delete a fork, just follow the same steps as you would to delete a regular repository.

### Initialiser le repo 
	git clone https://github.com/user-me/repo.git

### Référencer le projet original (upstream)
> Changes the active directory in the prompt to the newly cloned "project" directory

	cd projectdir/

> Assigns the original repository to a remote called "upstream"

	git remote add upstream https://github.com/user-original/project.git

> Pulls in changes not present in your local repository, without modifying your files

	git fetch upstream

### Créer une branche de travail 
#### Create your feature branch (my-new-feature) and switch to the branch 
	git checkout -b my-new-feature

Test your changes to the best of your ability.
Update the documentation to reflect your changes if they add or changes current functionality.
Déployer sur le repo local

#### Commit your changes 
> Equivalent for : git add files + git commit

	git commit -am 'Added some feature'

#### Déployer sur le repo distant
##### Push to the branch 
	git push origin my-new-feature).
##### ou Push the master :
	git push origin master 
(# Pushes commits to your remote repository stored on GitHub)

##### Importer les modifications du projet original // Fetches any new changes from the original repository
	git fetch upstream

##### Merges any changes fetched into your working files

	git merge upstream/master

Remarque : Pull VS Merge
Pull
git pull upstream master
# Pulls commits from 'upstream' and stores them in the local repository

When you use git pull, git tries to automatically do your work for you. It is context sensitive, so git will merge any pulled commits into the branch you are currently working in. One thing to keep in mind is that git pull automatically merges the commits without letting you review them first. If you don't closely manage your branches you may run into frequent conflicts.
Fetch & Merge
git fetch upstream
# Fetches any new commits from the original repository
git merge upstream/master
# Merges any fetched commits into your working files

When you git fetch, git retrieves any commits from the target remote that you do not have and stores them in your local repository. However, it does not merge them with your current branch. This is particularly useful if you need to keep your repository up to date but are working on something that might break if you update your files. To integrate the commits into your local branch, you use git merge. This combines the specified branches and prompts you if there are any conflicts.



### Remarque branches

#### Create branches
Branching allows you to build new features or test out ideas without putting your main project at risk. In git, branch is a sort of bookmark that references the last commit made in the branch. This makes branches very small and easy to work with.
How do I use branches?
Branches are pretty easy to work with and will save you a lot of headaches, especially when working with multiple people. To create a branch and begin working in it, run these commands:
git branch mybranch
##### Creates a new branch called "mybranch"
git checkout mybranch
##### Makes "mybranch" the active branch

Alternatively, you can use the shortcut:
git checkout -b mybranch
#### Creates a new branch called "mybranch" and makes it the active branch

To switch between branches, use git checkout.
git checkout master
# Makes "master" the active branch
git checkout mybranch
# Makes "mybranch" the active branch

Once you're finished working on your branch and are ready to combine it back into the masterbranch, use merge.
git checkout master
# Makes "master" the active branch
git merge mybranch
# Merges the commits from "mybranch" into "master"
git branch -d mybranch
# Deletes the "mybranch" branch

Branches locales
"git branch" should show all the local branches of your repo. 
> The starred branch is your current branch.

Tip
When you switch between branches, the files that you work on (the "working copy") are updated to reflect the changes in the new branch. If you have changes you have not committed, git will ensure you do not lose them. Git is also very careful during merges and pulls to ensure you don't lose any changes. When in doubt, commit early and commit often.



Git external submodule
Recapitulatif :
You have a project -- call it MyWebApp that already has a github repo
You want to use the jquery repository in your project
You want to pull the jquery repo into your project as a submodule.
Submodules are really, really easy to reference and use. Assuming you already have MyWebApp set up as a repo, from terminal issue these commands:
cd MyWebApp git submodule add git://github.com/jquery/jquery.git externals/jquery
This will create a directory named externals/jquery* and link it to the github jquery repository. Now we just need to init the submodule and clone the code to it:
git submodule update --init --recursive
You should now have all the latest code cloned into the submodule. If the jquery repo changes and you want to pull the latest code down, just issue the submodule update command again.

Github Pull Request
Create a new pull request.
https://help.github.com/articles/using-pull-requests

Tips 
Revert File to specific Version
Version of a file : git checkout commit_point_A -- <filename>

Git rebase
# Rewrite your master branch so that any commits of yours that aren't already in upstream/master are replayed on top of that other branch: 
git rebase upstream/master
If you don't want to rewrite the history of your master branch, (for example because other people may have cloned it) then you should replace the last command with 
git merge upstream/master 
However, for making further pull requests that are as clean as possible, it's probably better to rebase.

Update: If you've rebased your branch onto upstream/master you may need to force the push in order to push it to your own forked repository on GitHub. You'd do that with:
git push -f origin master


# Serious Game et tutos
http://pcottle.github.io/learnGitBranching/
http://marklodato.github.io/visual-git-guide/index-en.html
https://help.github.com/articles/fork-a-repo
http://mac.github.com/help
https://gun.io/blog/how-to-github-fork-branch-and-pull-request/


