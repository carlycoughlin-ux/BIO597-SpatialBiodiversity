# Lab01 - Intro to git and setting up a repo

## Basic git configuration

### Global git username/email
```bash
$ git config --global user.name "Isaac Overcast"
$ git config --global user.email "isaac.overcast@gmail.com"
```

### Set the default editor

```bash
$ git config --global core.editor "nano -w"
```

??? info "Setting other default editors"

    You can set many other different editors besides nano, if you
    have a preference. See the [SW Carpentries Git Setup page](https://swcarpentry.github.io/git-novice/02-setup.html)
    for detailed tips.

## Create/Install SSH Keys

Set up ssh keys to make github access easier

For this we will follow the excellent directions for
[Creating an SSH key pair](https://swcarpentry.github.io/git-novice/07-github.html#create-an-ssh-key-pair)
on the Software Carpentries lesson.

If everything in this lesson went well you should be able to type:
```
$ ssh -T git@github.com
```
Type `yes` when asked to verify the fingerprint, and if the ssh key
is set up correctly you will see the authentication verification message:
```
Hi isaacovercast! You've successfully authenticated, but GitHub does not provide shell access.
```

## Fork/clone the class repo

### Creating a fork w/ Github.com

* Insure you are logged in to GitHub
* Go to the lab site github repo: [https://github.com/isaacovercast/BIO597-SpatialBiodiversity](https://github.com/isaacovercast/BIO597-SpatialBiodiversity)
* Click the 'Fork' button in the upper right
* If you want you can change the Repository Name, but it's not required (maybe best to leave it as default)
* You will be taken to the landing page of your own forked repo
* Click the green "Code" button and under the clone section choose "SSH", then copy this URL
(it should look like this `git@github.com:<your_username>/BIO597-SpatialBiodiversity.git`

### Clone the fork locally
Copy your forked repo into your cloudbank environment
* Go to the [UMaine CloudBank Login Page](https://maine.cloudbank.2i2c.cloud/)
* Use the Launcher (the big blue plus button) to open a new Terminal
* Make sure you are in your home directory by typing `cd` and then `pwd` to verify. Your directory should be `/home/jovyan`. ('jovyan' is the default username inside a jupyterhub instance).
* Now Clone your copy of the class repo by typing `git clone ` and then pasting what we copied earlier
```
git clone git@github.com:<your_username>/BIO597-SpatialBiodiversity.git
```
* Change directory into your new forked repo and verify that this is indeed a git repo
```bash
cd BIO597-SpatialBiodiversity
git status
```
You should see:
```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

### Keeping your repo in sync
Now you have a 'forked' copy of the class repo, so you can do all the labs and
assignments in your own copy of the repository. But the class website is a
living document, so what happens when I change things and you need to get these
changes?

[Isaac makes a small change and pushes it to his repository]

Now go back to your browser tab for your own github repo and refresh. You 
should see a new info box that says "This branch is 1 commit behind...", which
indicates that your copy of the repo is missing changes that I have made.

Git remotes
```bash
git remote -v
```

```
origin  git@github.com:iao2122/BIO597-SpatialBiodiversity.git (fetch)
origin  git@github.com:iao2122/BIO597-SpatialBiodiversity.git (push)
```

```
git remote add upstream https://github.com/isaacovercast/BIO597-SpatialBiodiversity
```

Look again at the configured remotes and you should now see my repo listed as 'upstream'
```
git remote -v
```
```
origin  git@github.com:iao2122/BIO597-SpatialBiodiversity.git (fetch)
origin  git@github.com:iao2122/BIO597-SpatialBiodiversity.git (push)
upstream        https://github.com/isaacovercast/BIO597-SpatialBiodiversity (fetch)
upstream        https://github.com/isaacovercast/BIO597-SpatialBiodiversity (push)
```

Now you can pull down the changes to your local repo with:
```
git pull upstream main
```
```
From https://github.com/isaacovercast/BIO597-SpatialBiodiversity
 * branch            main       -> FETCH_HEAD
Updating 9e508b2..46e95f0
Fast-forward
 docs/labs/lab-01.2-CloneClassRepo.md | 48 ++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 48 insertions(+)
```

```
git status
```

```
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)
```

It's good practice to then synch these changes back to your own personal github
repo, and you can see in the status message that git is encouraging you to do this.

```
git push
```
```
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:iao2122/BIO597-SpatialBiodiversity.git
   550f16c..46e95f0  main -> main
```

### Reduce complexity w/ a command shortcut
Set a git alias to make pulling from upstream easier
Because there are potentially confusing consequences for running
`git pull upstream` (without specifying `main` at the end) it will
be easier for us to set a git "alias" so we can type less and have
a guaranteed outcome.

```
git config --global alias.upstream 'pull --no-edit upstream main'
```

[Isaac makes another small change and pushes to the original repository]

Now synch everything with two simple commands:
```
git upstream
git push
```

And if you go back to your github repo web page you should see it report
"This branch is up to date with `isaacovercast/BIO597-SpatialBiodiversity:main`".

