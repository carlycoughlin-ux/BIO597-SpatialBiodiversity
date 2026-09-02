
## Basic git configuration

```bash
$ git config --global user.name "Isaac Overcast"
$ git config --global user.email "isaac.overcast@gmail.com"
```

### Setting git default editor

```bash
$ git config --global core.editor "nano -w"
```

## Set up ssh keys to make github access easier

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
