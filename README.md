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
sudo apt install --yes git
git clone https://github.com/seanh/tmux.git ~/.tmux
~/.tmux/install
```

To install new plugins (that get added to `tmux.conf` after you've ran the
`install` script above):

```terminal
~/.tmux/plugins/tpm/bin/install_plugins
```

To update all the plugins:

```terminal
~/.tmux/plugins/tpm/bin/update_plugins all
```

To delete removed plugins:

```terminal
~/.tmux/plugins/tpm/bin/clean_plugins
```

Usage
-----

See [Copy & Paste in tmux](https://www.seanh.cc/2020/12/27/copy-and-paste-in-tmux/)
for the full details on copy & paste.

### Copying into the system clipboard

* Select some text with the mouse (this already copies it into the primary selection)
  then click <kbd>y</kbd> to also copy it to the system clipboard
* Or select some text with the keyboard in copy mode then click <kbd>y</kbd>

### Pasting from the system clipboard

Just use your terminal emulator's paste command:
<kbd><kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>v</kbd></kbd> in GNOME Terminal
or st.

### Pasting from the primary selection

<kbd><kbd>Shift</kbd> + <kbd>Middle Mouse Button</kbd></kbd>
