# Adding git to bash

Explained in detail on [git-scm](https://git-scm.com/book/en/v2/Appendix-A%3A-Git-in-Other-Environments-Git-in-Bash) page, in short:

1) Copy the contrib/completion/git-prompt.sh file from Git’s source repository to your home directory,

2)  Add something like this to your .bashrc or .bash_profile:

```
. ~/git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
export PS1='\w$(__git_ps1 " (%s)")\$ '
```

This will show branch information after `cd`ing into git repo, e.g.

```sh
$ (branch-name *)$
```
