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

### Prefix key

Either <kbd><kbd>Ctrl</kbd> + <kbd>a</kbd></kbd> or <kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> works as tmux's prefix key.

<kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>b</kbd></kbd> sends the prefix key into a nested tmux.

### Tabs ("windows")

* <kbd><kbd>Ctrl</kbd> + <kbd>t</kbd></kbd> opens a new tab
* <kbd><kbd>Ctrl</kbd> + <kbd>Page Up</kbd></kbd> and <kbd><kbd>Ctrl</kbd> + <kbd>Page Down</kbd></kbd> go to the previous and next tab
* <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Left</kbd></kbd> and <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Right</kbd></kbd> move the current tab left
  and right
* <kbd><kbd>Alt</kbd> + <kbd>1</kbd> &hellip; <kbd>8</kbd></kbd> jumps to tab 1&hellip;8
* <kbd><kbd>Alt</kbd> + <kbd>9</kbd></kbd> jumps to the last tab
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd></kbd> goes back to the tab you were last in

### Panes

* <kbd>F11</kbd> zooms or unzooms the current pane

### Copy & Paste

See [Copy & Paste in tmux](https://www.seanh.cc/2020/12/27/copy-and-paste-in-tmux/) for the full details on copy & paste.

* Click-and-drag to select text and copy it into the primary selection
* Double-click on a word to select the word and copy it into the primary selection
* Triple-click on a line to select the line and copy it into the primary selection
* <kbd>Middle Mouse Button</kbd> pastes from the primary selection (you don't need to hold down <kbd>Shift</kbd>)
* <kbd>y</kbd> or <kbd><kbd>Ctrl</kbd> + <kbd>c</kbd></kbd> copies the selected text into the system clipboard
* To paste from the system clipboard just use your terminal emulator's paste command:
  <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>v</kbd></kbd> in GNOME Terminal or st

### Copy mode

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>[</kbd></kbd> enters copy mode
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>Page Up</kbd></kbd> or just <kbd><kbd>Shift</kbd> + <kbd>Page Up</kbd></kbd> enters copy mode and scrolls up by one page
* You can also enter copy mode by scrolling with the mouse wheel or by clicking-and-dragging, double-clicking or triple-clicking with the <kbd>Left Mouse Button</kbd>
