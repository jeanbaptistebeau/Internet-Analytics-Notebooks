
# Internet Analytics Notebook - Team Incredible Abrutis

## Set up git repository on ICcluster

 - ssh into the cluster
 - Generate the key: `ssh-keygen -t rsa -b 4096`.
You will be asked to enter a name for the key. `ls` will now show two files `name` and `name.pub`.
 - Do a `cat name.pub`, copy the output and paste it in github settings.
 - Move the keys to the ssh folder: `mv name* .ssh/`
 - Start the ssh agent: `eval "$(ssh-agent -s)"`
 - Tell the agent to use the key: `ssh-add ~/.ssh/nameKey`
 - Clone the repo: `git clone git@github.com:vincenzobaz/Internet-Analytics-Notebooks.git`
 - `cd` into the repo and set up the github username: `git-config --local user.name "githubUsername"`

