## Repo

`repo init`

error:

    "/usr/bin/env 'python' no such file or directory"

Fix:

    sudo ln -s /usr/bin/python3 /usr/bin/python

~sudo apt install python-is-python2~

~sudo apt install python-all~

<sub>[source](https://source.android.com/setup/build/downloading#initializing-a-repo-client)</sub>

## Git

`git remote add`

    "fatal: remote origin already exists." - [Solution](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories)


`git pull`

> You have divergent branches and need to specify how to reconcile them. \
You can do so by running one of the following commands sometime before \
your next pull: \
 \
  git config pull.rebase false  # merge (the default strategy) \
  git config pull.rebase true   # rebase \
  git config pull.ff only       # fast-forward only \
 \
You can replace "git config" with "git config --global" to set a default \
preference for all repositories. You can also pass --rebase, --no-rebase, \
or --ff-only on the command line to override the configured default per \
invocation.
