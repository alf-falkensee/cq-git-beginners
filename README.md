# cq-git-beginners

*Start using git from R-Studio and switch to an online repository*

This is a list of steps to take in order to get a local history for
source and resource files from inside R-Studio. Additionally the
history can be made available online and shared with other programmers
and readers.

## Pre-requisites

- get git running on your system for instance from
  https://git-scm.com/downloads or via a package manager like
  anaconda, apt, dpkg, chocolatey

- get git running from within R-Studio: follow https://support.rstudio.com/hc/en-us/articles/200532077?version=1.1.463&mode=desktop (Getting Started)

## Setup git for your project from within R-Studio

1) go through `Tools - Version Control - Project Setup` from within R-Studio
2) use `git add`, `git commit`, `shell` and other git functionalities of R-Studio
3) as an alternative to step 1) use `git init` from where the .Rproj file is located

## What's missing to go online?

`git` is much more than about local histories; having his code online is
for instance a rather good poor-programmer's backup.

### write/publish
1) create *a-repository-name* as signed-in github.com user *a-git-username*
	- make sure to respect copyrights and politeness already at this
      step; it is partly too late once things are online.

2) git remote add origin https://github.com/a-git-username/a-repository-name.git
    - from where the .Rproj file is located

3) git pull --allow-unrelated-histories
    - since this mini-tutorial has a working local .git repository as a
      pre-condition and the online repository is potentially created after
      the local one, one has to override corresponding git restrictions to
      the merge of unrelated histories.

4) git push -u origin master

### read
- git clone https://github.com/alf-falkensee/cq-git-beginners.git
  - or clone whatever is allowed to be cloned; if you want
    subsequently to participate to the cloned repository, learn about
    pull requests, though.
