# Using Forks

This is a short document on how to use forks instead of just creating things out of the branches of the master branch.

  - Go to the project that you want to fork on GitHub.
  - Click the fork button for forking at the top right hand side of the page. (It will have a the forking icon)

> You can always click the number on the fork button to go and see other people's forks displayed as a graphical interpretation.

### Clone:

  - Navigate to your local instance and create a directory that you want to put your forked version to be at.
  - Making sure you are on the on your forked version of your project within GitHub, copy the URL.
  - run: `git clone "URL of fork"` on your local instance in its directory
  - You will then have the cloned version of your fork locally
  - Check the origins by running: `git remote -v` This will display origins with their fetch and push locations.

### Set up Upstream

  - To setup the upstream we will need to run: `git remote add upstream "URL of original project"`
  - Usually you would replace the username that is in the original URL with what was there previously in the original project before your fork.
  - If you run: `git remote -v` again, you will now see the upstream and its locations

### Syncing

> Anytime you start a new fork you must sync them together so that your local, remote and fork original location are all synced.

  - Run: `git pull --rebase upstream master`

> Pull specifically from upstream master. Now we will push back to your online fork. This is important tbecause it will keep everything in sync. When you do this, your master branch will be in sync with your upstream. If you have various branches, they will not be in sync with your current local branch so then you would need to do this:

`git checkout "Your out of date branch"`

`git rebase master` 

> This will get the changes from your master branch which initially came from upstream. You will have merge conflicts, resolve them and check that the changes are resolved, then you can push up your branch.

  - Let's run: `git push origin master`

> Now everything is in sync. You should do this with every new branch and to push and pull updates. You can checkout and get other branches from folks this way. You can push and pull on each other's forks too. Here is some more information on forking by [GitHub](https://help.github.com/articles/fork-a-repo/).