vim
===

Summary
-------

1. [Basis](#basis)
2. [Command](#command)
3. [Shortcuts](#shortcuts)
4. [Search](#search)

Basis
-----

### Mode

| Mode        | Pattern   | Function                       |
| ----------- | --------- | ------------------------------ |
| Interactive | `NORMAL`  | Motions, commands and searches |
| Insertion   | `INSERT`  | Insert content                 |
| Visual      | `VISUAL`  | Select content                 |
| Replace     | `REPLACE` | Replace content                |

### Modelike

| Modelike        | Pattern | Function                             |
| --------------- | ------- | ------------------------------------ |
| Command         | `:`     | Handle commands                      |
| Search to start | `?`     | Search patterns from cursor to start |
| Search to end   | `/`     | Search patterns from cursor to end   |

Command
-------

| Function                            | Command                             |
| ----------------------------------- | ----------------------------------- |
| Save as                             | `:w FILENAME`                        |
| Close saved                         | `:q`                                 |
| Close unsaved                       | `:!q`                                |
| Save and close                      | `:wq` | `x`                          |
| Undo                                | `:u`                                 |
| Undo N actions                      | `:nu`                                |
| Replace once from cursor            | `:s/PATTERN/STRING/OPTIONS`          |
| Replace from cursor to end          | `:s/PATTERN/STRING/OPTIONS`          |
| Replace from line START to line END | `:START,ENDs/PATTERN/STRING/OPTIONS` |
| Replace all                         | `:%s/PATTERN/STRING/g`               |
| Replace all with confirmation       | `:%s/PATTERN/STRING/g`               |
| Insert file content                 | `:r FILENAME`                        |
| Run shell command                   | `:!SHELL_COMMAND`                    |
| Insert shell command result         | `:r !SHELL_COMMAND`                  |
| Split horizontally                  | `:sp FILENAME`                       |
| Split vertically                    | `:vsp FILENAME`                      |

Shortcuts
---------

### Access mode

| Access                       | Shortcut |
| ---------------------------- | -------- |
| Interactive                  | `Echap`  |
| Insertion (before cursor)    | `i`      |
| Insertion (after cursor)     | `a`      |
| Insertion (line start)       | `I`      |
| Insertion (line end)         | `i`      |
| Add line above and insert in | `O`      |
| Add line below and insert in | `o`      |
| Visual                       | `v`      |
| Replace                      | `R`      |

### Motions

| Motion                                   | Shortcut     |
| ---------------------------------------- | ------------ |
| Up                                       | `k` | `↑`    |
| Down                                     | `j` | `↓`    |
| Left                                     | `h` | `←`    |
| Right                                    | `l` | `→`    |
| Line start                               | `0`          |
| Line end                                 | `$`          |
| Line N                                   | `NG` | `Ngg` |
| First line                               | `gg`         |
| Last line                                | `G`          |
| () | {} | [] extremities                 | `%`          |
| Previous occurence                       | `N`          |
| Next occurence                           | `n`          |
| Next short word (cursor at start)        | `w`          |
| Next N short words (cursor at start)     | `Nw`         |
| Next short word (cursor at end)          | `e`          |
| Previous short word (cursor at start)    | `b`          |
| Next long word (cursor at start)         | `W`          |
| Next long word (cursor at end)           | `E`          |
| Previous long word (cursor at start)     | `B`          |

### Edition

| Edition                                | Shortcut |
| -------------------------------------- | -------- |
| Delete character                       | `x`      |
| Delete character and insert            | `c`      |
| Cut current line                       | `dd`     |
| Cut current line and N - 1 next lines  | `Ndd`    |
| Cut from cursor to line start          | `d0`     |
| Cut from cursor to line end            | `d$`     |
| Cut N next words                       | `Ndw`    |
| Yank current line                      | `yy`     |
| Yank current line and N - 1 next lines | `Nyy`    |
| Yank from cursor to line start         | `y0`     |
| Yank from cursor to line end           | `y$`     |
| Yank N next words                      | `Nyw`    |
| Paste before                           | `P`      |
| Paste after                            | `p`      |

### Viewport navigation

| Navigation                 | Shortcut                   |
| -------------------------- | -------------------------- |
| Next viewport              | `Control + w, Control + w` |
| Top viewport               | `Control + w, k`           |
| Bottom viewport            | `Control + w, j`           |
| Left viewport              | `Control + w, h`           |
| Right viewport             | `Control + w, l`           |
| Maximise current viewport  | `Control + w, +`           |
| Minimise current viewport  | `Control + w, -`           |
| Equalize all viewports     | `Control + w, =`           |
| Viewports rotation         | `Control + w, r`           |
| Viewports reverse rotation | `Control + w, Shift + r`   |
| Close current viewport     | `Control + w, q`           |

### Other

| Function                        | Shortcut      |
| ------------------------------- | ------------- |
| Save and quit                   | `ZZ`          |
| Quit without saving             | `ZQ`          |
| Undo                            | `u`           |
| Undo N actions                  | `Nu`          |
| Undo last un                    | `Control + r` |
| Show position                   | `Control + g` |
| Replace from cursor to word end | `ceSTRING`    |
| Replace from cursor to line end | `c$STRING`    |

Search
------

| Function                           | Shortcut         |
| ---------------------------------- | ---------------- |
| Search string from cursor to start | `?STRING`        |
| Search string from cursor to end   | `/STRING`        |
| Case insensitive search            | `/STRING\c`      |
| POSIX regular expression search    | `/REGEX\OPTIONS` |
