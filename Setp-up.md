# Configuring user information used across all local repositories
## configure email id
git config --global user.email "[valid email]"
set a name that is identifiable for credit when review version history

## configure user name
git config --global user.name "[firstname lastname]"

git config --global color.ui auto
## set automatic command line coloring for Git for easy reviewing

git config --global --list
## Check all global Git configurations

git config --show-origin --get user.name
## This shows the configuration file containing the username.

git config --show-origin --get user.email
## This shows the configuration file containing the email