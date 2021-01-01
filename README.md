My tmux Config
==============

My [tmux](https://tmux.github.io/) config files.

Installation
------------

### Ubuntu 20.04

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

### Copy & Paste

See [Copy & Paste in tmux](https://www.seanh.cc/2020/12/27/copy-and-paste-in-tmux/)
for the full details on copy & paste.

#### Copying into the primary selection

Just click-and-drag to select some text with the mouse and copy it into the primary selection.
(As in most apps, selecting text with the _keyboard_ _doesn't_ copy it into the primary selection.)

Double-click on a word to select the word and copy it into the primary selection.

Triple-click on a line to select the line and copy it into the primary selection.

#### Copying into the system clipboard

Select some text with either the mouse or the keyboard and click <kbd>y</kbd>.

### Pasting from the primary selection

<kbd>Middle Mouse Button</kbd> (you don't need to hold down <kbd>Shift</kbd>).

### Pasting from the system clipboard

Just use your terminal emulator's paste command:
<kbd><kbd>Shift</kbd> + <kbd>Ctrl</kbd> + <kbd>v</kbd></kbd> in GNOME Terminal
or st.
