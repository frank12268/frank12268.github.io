---
layout: post
title:  "How to Install Dual Python on Mac OSX"
date:   2017-09-03 02:38:41 +0800
categories: python
tags: [python]
---
## Install Homebrew
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install python
brew install python3
```
Python will be installed at `/usr/local/Cellar`
## Install ipython & other libraries
install pip

install ipython and other package with `--target` at local user's directory

## Setup link & env
Set python(/2/3) / pip(/2/3) / ipython(/2/3) s' link

```
$ ls -ahl /usr/local/bin/p*
-rwxr-xr-x  1 root      wheel   281B Jul 27 11:13 /usr/local/bin/pip
lrwxr-xr-x  1 lvzihong  admin    34B Sep  1 00:24 /usr/local/bin/pip2 -> ../Cellar/python/2.7.13_1/bin/pip2
lrwxr-xr-x  1 lvzihong  admin    36B Sep  1 00:24 /usr/local/bin/pip2.7 -> ../Cellar/python/2.7.13_1/bin/pip2.7
lrwxr-xr-x  1 lvzihong  admin    32B Sep  1 00:27 /usr/local/bin/pip3 -> ../Cellar/python3/3.6.2/bin/pip3
lrwxr-xr-x  1 lvzihong  admin    34B Sep  1 00:27 /usr/local/bin/pip3.6 -> ../Cellar/python3/3.6.2/bin/pip3.6
lrwxr-xr-x  1 lvzihong  admin    35B Jul 27 15:25 /usr/local/bin/protoc -> ../Cellar/protobuf/3.3.2/bin/protoc
lrwxr-xr-x  1 lvzihong  admin    36B Aug 10 15:20 /usr/local/bin/pydoc2 -> ../Cellar/python/2.7.13_1/bin/pydoc2
lrwxr-xr-x  1 lvzihong  admin    38B Aug 10 15:20 /usr/local/bin/pydoc2.7 -> ../Cellar/python/2.7.13_1/bin/pydoc2.7
lrwxr-xr-x  1 lvzihong  admin    34B Jul 27 12:04 /usr/local/bin/pydoc3 -> ../Cellar/python3/3.6.2/bin/pydoc3
lrwxr-xr-x  1 lvzihong  admin    36B Jul 27 12:04 /usr/local/bin/pydoc3.6 -> ../Cellar/python3/3.6.2/bin/pydoc3.6
-rwxr-xr-x  1 lvzihong  admin   239B Jul 27 12:05 /usr/local/bin/pygmentize
lrwxr-xr-x  1 lvzihong  admin    37B Aug 10 15:20 /usr/local/bin/python2 -> ../Cellar/python/2.7.13_1/bin/python2
lrwxr-xr-x  1 lvzihong  admin    44B Aug 10 15:20 /usr/local/bin/python2-config -> ../Cellar/python/2.7.13_1/bin/python2-config
lrwxr-xr-x  1 lvzihong  admin    39B Aug 10 15:20 /usr/local/bin/python2.7 -> ../Cellar/python/2.7.13_1/bin/python2.7
lrwxr-xr-x  1 lvzihong  admin    46B Aug 10 15:20 /usr/local/bin/python2.7-config -> ../Cellar/python/2.7.13_1/bin/python2.7-config
lrwxr-xr-x  1 lvzihong  admin    35B Jul 27 12:04 /usr/local/bin/python3 -> ../Cellar/python3/3.6.2/bin/python3
lrwxr-xr-x  1 lvzihong  admin    42B Jul 27 12:04 /usr/local/bin/python3-config -> ../Cellar/python3/3.6.2/bin/python3-config
lrwxr-xr-x  1 lvzihong  admin    37B Jul 27 12:04 /usr/local/bin/python3.6 -> ../Cellar/python3/3.6.2/bin/python3.6
lrwxr-xr-x  1 lvzihong  admin    44B Jul 27 12:04 /usr/local/bin/python3.6-config -> ../Cellar/python3/3.6.2/bin/python3.6-config
lrwxr-xr-x  1 lvzihong  admin    38B Jul 27 12:04 /usr/local/bin/python3.6m -> ../Cellar/python3/3.6.2/bin/python3.6m
lrwxr-xr-x  1 lvzihong  admin    45B Jul 27 12:04 /usr/local/bin/python3.6m-config -> ../Cellar/python3/3.6.2/bin/python3.6m-config
lrwxr-xr-x  1 lvzihong  admin    38B Aug 10 15:20 /usr/local/bin/pythonw2 -> ../Cellar/python/2.7.13_1/bin/pythonw2
lrwxr-xr-x  1 lvzihong  admin    40B Aug 10 15:20 /usr/local/bin/pythonw2.7 -> ../Cellar/python/2.7.13_1/bin/pythonw2.7
lrwxr-xr-x  1 lvzihong  admin    34B Jul 27 12:04 /usr/local/bin/pyvenv -> ../Cellar/python3/3.6.2/bin/pyvenv
lrwxr-xr-x  1 lvzihong  admin    38B Jul 27 12:04 /usr/local/bin/pyvenv-3.6 -> ../Cellar/python3/3.6.2/bin/pyvenv-3.6
```
Set PATH & PYTHON_PATH in `~/.profile`
```
export PATH=$PATH:$GOPATH/bin:/Users/megvii/Library/Python/2.7/bin:/Users/megvii/Library/Python/3.6/bin
# export PYTHONPATH=/Users/megvii/Library/Python/2.7/lib/python/site-packages:/Users/megvii/Library/Python/3.6/lib/python/site-packages
export PYTHON2PATH=/Users/megvii/Library/Python/2.7/lib/python/site-packages
export PYTHON3PATH=/Users/megvii/Library/Python/3.6/lib/python/site-packages
```
## Reference
[Install python](https://stringpiggy.hpd.io/mac-osx-python3-dual-install/)