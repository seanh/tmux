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

<kbd><kbd><kbd>Ctrl</kbd> + <kbd>a</kbd></kbd> <kbd>a</kbd></kbd> or
<kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>b</kbd></kbd> sends the prefix key into a nested tmux.

### Tabs ("windows")

* <kbd><kbd>Ctrl</kbd> + <kbd>t</kbd></kbd> opens a new tab
* <kbd><kbd>Ctrl</kbd> + <kbd>Page Up</kbd></kbd> and <kbd><kbd>Ctrl</kbd> + <kbd>Page Down</kbd></kbd> go to the previous and next tab
* <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Left</kbd></kbd> and <kbd><kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Right</kbd></kbd> move the current tab left
  and right
* <kbd><kbd>Alt</kbd> + <kbd>1</kbd> &hellip; <kbd>8</kbd></kbd> jumps to tab 1&hellip;8
* <kbd><kbd>Alt</kbd> + <kbd>9</kbd></kbd> jumps to the last tab
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd></kbd>
  or <kbd><kbd><kbd>Ctrl</kbd> + <kbd>a</kbd></kbd> <kbd><kbd>Ctrl</kbd> + <kbd>a</kbd></kbd></kbd>
  goes back to the tab you were last in
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>,</kbd></kbd> renames the current window
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>&</kbd></kbd> kills the current window

### Panes

Pane commands from [tmux-pain-control](https://github.com/tmux-plugins/tmux-pain-control):

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>-</kbd></kbd> splits the current pane horizontally
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>|</kbd></kbd> splits the current pane vertically
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>\\</kbd></kbd> splits the current pane full-width horizontally
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>_</kbd></kbd> splits the current pane full-width vertically
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>h</kbd>, <kbd>j</kbd>, <kbd>k</kbd> or <kbd>l</kbd></kbd>
  or
  <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Ctrl</kbd> + <kbd>h</kbd>, <kbd>j</kbd>, <kbd>k</kbd> or <kbd>l</kbd></kbd></kbd>
  move to the pane on the left, below, on the right or above
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>;</kbd></kbd> moves to the last pane
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>&lt;</kbd></kbd> and <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>&gt;</kbd></kbd>
  move the current pane left and right

My own bindings:

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
* <kbd>Enter</kbd> copies the selected text into a tmux paste buffer and exits copy mode
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>]</kbd></kbd> pastes from the most recent tmux paste buffer
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>=</kbd></kbd> lists all tmux paste buffers and lets you choose one to paste from

More copy & paste shortcuts from [tmux-yank](https://github.com/tmux-plugins/tmux-yank):

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>y</kbd></kbd> copies the current command line to the clipboard
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>y</kbd></kbd></kbd> copies the current working directory to the clipboard
* <kbd><kbd>Shift</kbd> + <kbd>y</kbd></kbd> in copy mode copies the current selection and pastes it onto the command line

### Copy mode

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>[</kbd></kbd> enters copy mode
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>Page Up</kbd></kbd> or just <kbd><kbd>Shift</kbd> + <kbd>Page Up</kbd></kbd> enters copy mode and scrolls up by one page
* You can also enter copy mode by scrolling with the mouse wheel or by clicking-and-dragging, double-clicking or triple-clicking with the <kbd>Left Mouse Button</kbd>

### Opening files and URLs

File and URL opening shortcuts from [tmux-open](https://github.com/tmux-plugins/tmux-open):

* <kbd>o</kbd> in copy mode opens the selected file or URL using `open` (macOS) or `xdg-open` (Linux)
* <kbd><kbd>Ctrl</kbd> + <kbd>o</kbd></kbd> opens the selected file in `$EDITOR`
* <kbd><kbd>Ctrl</kbd> + <kbd>s</kbd></kbd> searches for the selected text in a browser

### Reloading

*  <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>r</kbd></kbd></kbd> reloads the `~/.tmux.conf` file
   (you can also just run `tmux source ~/.tmux.conf`)
*  <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>i</kbd></kbd></kbd> installs new plugins from the `~/.tmux.conf` file
   (you can also just run `~/.tmux/plugins/tpm/bin/install_plugins`)
*  <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>u</kbd></kbd></kbd> upgrades plugins
   (you can also just run `~/.tmux/plugins/tpm/bin/update_plugins all`)
*  <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Alt</kbd> + <kbd>u</kbd></kbd></kbd> uninstalls plugins that're no longer in the `~/.tmux.conf` file
   (you can also just run `~/.tmux/plugins/tpm/bin/clean_plugins`)

### Sessions

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>$</kbd></kbd> renames the current session

Session-management shortcuts from [tmux-sessionist](https://github.com/tmux-plugins/tmux-sessionist):

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>g</kbd></kbd> lists open sessions and lets you change to one of them
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>s</kbd></kbd></kbd> changes the the last session
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>c</kbd></kbd></kbd> creates a new session, prompting your for a session name, and
  changes to the new session
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>x</kbd></kbd></kbd> kills the current session and changes to another session
  (if there are any) or exits tmux (if there aren't any other sessions)
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>@</kbd></kbd> breaks the current pane out into a new session

### Detaching clients

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>d</kbd></kbd> detaches the current client from the current session
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>d</kbd></kbd></kbd> lists all clients attached to the current session and lets you
choose one to detach
