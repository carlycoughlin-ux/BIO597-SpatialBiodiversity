
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

