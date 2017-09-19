Screen
======

Summary
-------

1. [Configuration](#configuration)
2. [Parameters](#parameters)
3. [Shortcuts](#shortcuts)

Configuration
-------------

	~/.screenrc

Parameters
----------

| Action                         | Parameter               |
| ------------------------------ | ----------------------- |
| Create named session           | `-S NAME`               |
| Start detached session         | `-d -m`                 |
| Reattach to session            | `-r NAME`, `-r PID`     |
| List opened sessions           | `-ls`                   |
| Detach session                 | `-d NAME`, `-d PID`     |
| Delete session                 | `-wipe`                 |
| Set specific configuration     | `-c FILE`               |
| Set session history scrollback | `-h NUMBER`             |
| Join attached session          | `-x NAME`, `-x PID`     |
| Preselect session window       | `-p NUMBER`, `-p TITLE` |
| Name window                    | `-t TITLE`              |

Shortcuts
---------

### Shortcut Syntax

	Control + a, KEY

### General

| Action                         | Shortcut                 |
| ------------------------------ | ------------------------ |
| Enter in scroll mode           | `Control + a, ESC`       |
| Start selection in scroll mode | `ENTER`                  |
| End selection in scroll mode   | `ENTER`                  |
| Paste scroll mode selection    | `Control + a, ]`         |
| List all attached session      | `Control + a, *`         |
| Start logging content in file  | `Control + a, Shift + h` |
| End logging content in file    | `Control + a, Shift + h` |

> Log file path : *~/screenlog.[windows number]*

### Help

| Action          | Shortcut         |
| --------------- | ---------------- |
| Open new help   | `Control + a, ?` |
| Go to next page | SPACE            |
| Close help      | ENTER            |
| Display version | `Control + a, v` |

### Windows

| Action                    | Shortcut                        |
| ------------------------- | ------------------------------- |
| Create new window         | `Control + a, c`                |
| List opened windows       | `Control + a, w`                |
| Rename current window     | `Control + a, Shift + a`        |
| Go to next window         | `Control + a, n`                |
| Go to previous window     | `Control + a, p`                |
| Jump to last window       | `Control + a, Control + a`      |
| Jump to window [0-9]      | `Control + a, [0-9]`            |
| Enter window number       | `Control + a, '`                |
| Choose window             | `Control + a, "`                |
| Close current window      | `Control + a, k`, `Control + d` |
| Resize window             | `Control + a, Shift + f`        |

### Split

| Action                  | Shortcut                 |
| ----------------------- | ------------------------ |
| Create new split        | `Control + a, Shift + s` |
| Go to next split        | `Control + a, Tab`       |
| Close current split     | `Control + a, Shift + x` |
| Close not current split | `Control + a, Shift + q` |

### Detach

| Action                          | Shortcut                            |
| ------------------------------- | ----------------------------------- |
| Detach screen from terminal     | `Control + a, d`                    |
| Detach screen and close session | `Control + a, Shift + d, Shift + d` |
