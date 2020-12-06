My tmux Config
==============

My [tmux](https://tmux.github.io/) config files.

Installation
------------

### Ubuntu 20.04

Install [fish shell](https://github.com/seanh/fish), my tmux.conf sets it as tmux's
default shell.  
FIXME: Set fish as tmux's default shell only if fish is installed.

Then:

```terminal
sudo apt install --yes myrepos git tmux
git clone https://github.com/seanh/tmux.git ~/.tmux
cd ~/.tmux
mr -j 5 checkout
ln -s ~/.tmux/tmux.conf ~/.tmux.conf
```
