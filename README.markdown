My tmux Config
==============

My [tmux](https://tmux.github.io/) config files.

Installation
------------

### Ubuntu 20.04

Install [fish shell](https://github.com/seanh/fish), my tmux.conf sets it as tmux's
default shell.  
FIXME: Set fish as tmux's default shell only if fish is installed.

Enable Ubuntu's "Community-maintained free and open-source
software (universe)" option in the **Software & Updates** app,
then:

```terminal
sudo apt install --yes myrepos git tmux && git clone https://github.com/seanh/tmux.git ~/.tmux && mr -c ~/.tmux/.mrconfig -j 5 update && ln -s ~/.tmux/tmux.conf ~/.tmux.conf
```
