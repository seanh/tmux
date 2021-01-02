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

Links
-----

* [Copy and Paste in tmux](https://www.seanh.cc/2020/12/27/copy-and-paste-in-tmux/)
* [Binding Keys in tmux](https://www.seanh.cc/2020/12/28/binding-keys-in-tmux/)
* [Setting Options in tmux](https://www.seanh.cc/2020/12/28/setting-options-in-tmux/)
* [How to Make tmux’s “Windows” Behave like Browser Tabs](https://www.seanh.cc/2020/12/30/how-to-make-tmux's-windows-behave-like-browser-tabs/)
* [Browser-like Search Shortcuts for tmux](https://www.seanh.cc/2020/12/31/browser-like-search-shortcuts-for-tmux/)
* tmux plugins I use:
  * [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm)
  * [tmux-sensible](https://github.com/tmux-plugins/tmux-sensible)
  * [tmux-yank](https://github.com/tmux-plugins/tmux-yank)
  * [tmux-pain-control](https://github.com/tmux-plugins/tmux-pain-control)
  * [tmux-sessionist](https://github.com/tmux-plugins/tmux-sessionist)
  * [tmux-prefix-highlight](https://github.com/tmux-plugins/tmux-prefix-highlight)
  * [tmux-better-mouse-mode](https://github.com/NHDaly/tmux-better-mouse-mode)
  * [tmux-open](https://github.com/tmux-plugins/tmux-open)

Keyboard Shortcuts
------------------

A non-exhaustive list of some of the keyboard shortcuts I use more often.
Some of these are custom key bindings from my [`tmux.conf`](tmux.conf) file,
others are provided by the plugins I use,
and some are default tmux bindings.
The full list of all bindings can be found by running `tmux lsk`.

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
* <kbd><kbd>Alt</kbd> + <kbd>9</kbd></kbd> jumps back to the last tab
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd></kbd>
  or <kbd><kbd><kbd>Ctrl</kbd> + <kbd>a</kbd></kbd> <kbd><kbd>Ctrl</kbd> + <kbd>a</kbd></kbd></kbd>
  goes back to the tab you were last in
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>,</kbd></kbd> renames the current tab
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>&</kbd></kbd> kills the current tab

### Panes

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>x</kbd></kbd> kills the current pane
* <kbd>F11</kbd> zooms or unzooms the current pane

Pane commands from [tmux-pain-control](https://github.com/tmux-plugins/tmux-pain-control):

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>-</kbd></kbd> splits the current pane horizontally
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>|</kbd></kbd> splits the current pane vertically
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>\\</kbd></kbd> splits the current pane full-width horizontally
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>_</kbd></kbd> splits the current pane full-width vertically
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>h</kbd>, <kbd>j</kbd>, <kbd>k</kbd> or <kbd>l</kbd></kbd>
  or
  <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Ctrl</kbd> + <kbd>h</kbd>, <kbd>j</kbd>, <kbd>k</kbd> or <kbd>l</kbd></kbd></kbd>
  move to the pane on the left, below, on the right or above
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>;</kbd></kbd> moves back to the last pane
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>&lt;</kbd></kbd> and <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>&gt;</kbd></kbd>
  move the current pane left and right

### Copy & Paste

* Click-and-drag to select text
* Double-click on a word to select the word
* Triple-click on a line to select the line
* Selecting text with the mouse automatically copies it into the primary selection and into a tmux paste buffer
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

I use tmux's vi-style copy mode keybindings. When in copy mode:

* <kbd>Space</kbd> or <kbd>v</kbd> begins a selection.  
  Selections made with the keyboard don't get automatically copied into the system's primary selection or into a tmux paste buffer.

* <kbd>y</kbd> or <kbd><kbd>Ctrl</kbd> + <kbd>c</kbd></kbd> copies the selection into the system clipboard and into a tmux paste buffer.

* <kbd>Enter</kbd> copies the selection into a tmux paste buffer and exits copy mode.

* <kbd><kbd>Shift</kbd> + <kbd>y</kbd></kbd> copies the selection into a tmux paste buffer and pastes it onto the command line.

* <kbd>Esc</kbd> clears the selection and stays in copy mode

* <kbd>q</kbd> clears the selection and exits copy mode

* <kbd>h</kbd>, <kbd>j</kbd>, <kbd>k</kbd> and <kbd>l</kbd> move left, down, up and right

* <kbd>w</kbd>, <kbd>W</kbd>, <kbd>b</kbd>, <kbd>B</kbd>, <kbd>e</kbd> and <kbd>E</kbd> move forward and backward a word at a time, like in vim

* <kbd>$</kbd> moves to the end of the line and <kbd>0</kbd> goes to the start of the line. <kbd>^</kbd> goes to the first non-blank character on the line

* <kbd>g</kbd> goes to the beginning of the scrollback history (the top) and <kbd>G</kbd> goes to the end (the bottom)

* <kbd>r</kbd> enables rectangle selection

* <kbd>V</kbd> selects the entire current line, same as in vim (in vim <kbd>V</kbd> enters visual line mode). Once you've selected a line you can move the cursor
  up and down to select more lines

* <kbd>/</kbd> begins a forward (downward) search and <kbd>?</kbd> begins a backward (upwards) search. <kbd>n</kbd> and <kbd>N</kbd> go to the next and previous
  search match.

* <kbd>f</kbd> jumps forward to the next occurrence of a character on the same line. For example <kbd><kbd>f</kbd> <kbd>s</kbd></kbd> jumps to the next `s`.
  <kbd>F</kbd> jumps backward. <kbd>;</kbd> repeats the jump (goes to the _next_ `s`), <kbd>,</kbd> goes to the _previous_ match. <kbd>t</kbd> and <kbd>T</kbd> 
  are the same as <kbd>f</kbd> and <kbd>F</kbd> but they jump the cursor to the character _before_ the matching character, instead of on top of the match.

* When the cursor is on an opening bracket <kbd>%</kbd> moves to the closing bracket

* <kbd>D</kbd> copies the text from the cursor to end of line (including the character under the cursor) into a tmux paste buffer and exits copy mode

### Opening files and URLs

File and URL opening shortcuts from [tmux-open](https://github.com/tmux-plugins/tmux-open):

* <kbd>o</kbd> in copy mode opens the selected file or URL using `open` (macOS) or `xdg-open` (Linux)  
  (hint: double-click on a filename or URL with the mouse and then hit <kbd>o</kbd>)
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
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>s</kbd></kbd> lists open sessions and lets you change to one of them

Session-management shortcuts from [tmux-sessionist](https://github.com/tmux-plugins/tmux-sessionist):

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>g</kbd></kbd> lists open sessions and lets you change to one of them  
  (doesn't seem to be as nice as the built in <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>s</kbd></kbd>)
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>s</kbd></kbd></kbd> changes back to the last session
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>c</kbd></kbd></kbd> creates a new session, prompting your for a session name, and
  changes to the new session
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>x</kbd></kbd></kbd> kills the current session and changes to another session
  (if there are any) or exits tmux (if there aren't any other sessions)
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>@</kbd></kbd> breaks the current pane out into a new session

### Detaching clients

* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd>d</kbd></kbd> detaches the current client from tmux
* <kbd><kbd><kbd>Ctrl</kbd> + <kbd>b</kbd></kbd> <kbd><kbd>Shift</kbd> + <kbd>d</kbd></kbd></kbd> lists all clients attached to the current session and lets you
choose one to detach
