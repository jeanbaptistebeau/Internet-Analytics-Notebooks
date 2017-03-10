
# Internet Analytics Notebook - Team Incredible Abrutis

## Set up git repository on ICcluster

 - ssh into the cluster
 - Generate the key: `ssh-keygen -t rsa -b 4096`.
You will be asked to enter a name for the key. `ls` will now show two files `name` and `name.pub`.
 - Do a `cat name.pub`, copy the output and paste it in github settings.
 - Move the keys to the ssh folder: `mv name* ~/.ssh/`
 - Set up git with github information:
```
git config --global user.name "githubUsername"
git config --global user.email "emailUsedInGithub"
```
 - Modify your `.bashrc` to load the ssh key upon login using `ssh-agent`:
```
if [ -z "$SSH_AUTH_SOCK" ] ; then
        eval `ssh-agent -s`
        ssh-add ~/.ssh/name
fi
```
 - Log out and login again: you should be prompted for the key passphrase upon logging in.
 - Clone the repo: `git clone git@github.com:vincenzobaz/Internet-Analytics-Notebooks.git`
