
## Setting up GitHub fork of Class repo

* Insure you are logged in to GitHub
* Go to the lab site github repo: [https://github.com/isaacovercast/BIO597-SpatialBiodiversity](https://github.com/isaacovercast/BIO597-SpatialBiodiversity)
* Click the 'Fork' button in the upper right
* If you want you can change the Repository Name, but it's not required (maybe best to leave it as default)
* You will be taken to the landing page of your own forked repo
* Click the green "Code" button and under the clone section choose "SSH", then copy this URL
(it should look like this `git@github.com:<your_username>/BIO597-SpatialBiodiversity.git`

### Copy your forked repo into your cloudbank environment
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


