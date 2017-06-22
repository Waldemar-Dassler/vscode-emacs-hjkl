# vscode-emacs-hjkl

This is emacs like plugin for Visual Studio Code.

## Operation
Use `Shift+DEL` to cut to clipboard, the `Ctrl+C` is not overridden.
Use `Shift+Insert` to paste from clipboard.

### Move command
|Command | Status | Desc |
|--------|--------|------|
| `ALT-l` | OK | Move forward |
| `ALT-h` | OK | Move backward |
| `ALT-j` | OK | Move to the next line |
| `ALT-k` | OK | Move to the previous line |
| `ALT-a` | OK | Move to the beginning of line |
| `ALT-e` | OK | Move to the end of line |
| `ALT-f` | OK | Move forward by one word unit |
| `ALT-b` | OK | Move backward by one word unit |
| `M->` | NO | Move to the end of buffer |
| `M-<` | NO | Move to the beginning of buffer |
| `C-v` | NO | Scroll down by one screen unit |
| `M-v` | NO | Scroll up by one screen unit |
| `C-x C-n` | - | Set goal column |
| `C-u C-x C-n` | - | Deactivate C-x C-n |
| `M-g g` | NO | Jump to line (command palette) |


### Search Command
|Command | Status | Desc |
|--------|--------|------|
| `C-s` | NO | Search forward |
| `C-r` | NO | Search backward |
| `C-M-n` | NO | Add selection to next find match |
| `C-l` | - | Use `ext install keyboard-scroll` to activate |

### Edit command
|Command | Status | Desc |
|--------|--------|------|
| `ALT-e` | OK | Delete right  (DEL) |
| `ALT-w` | OK | Delete left  (BACKSPACE) |
| `ALT-o` | OK | Delete word |
| `C-k` | NO | Kill to line end |
| `C-w` | NO | Kill region |
| `M-w` | NO | Copy region to kill ring |
| `C-y` | NO | Yank |
| `C-j` | NO | Line Feed |
| `C-m` | - | Carriage Return |
| `C-i` | - | Horizontal Tab |
| `C-x C-o` | NO | Delete blank lines around |
| `C-x h` | NO | Select All |
| `C-x u` (`C-/`)| NO | Undo |
| `C-;` | △ | Toggle line comment in and out |
| `M-;` | △ | Toggle region comment in and out |

### Other Command
|Command | Status | Desc |
|--------|--------|------|
| `C-g` | NO | Cancel |
| `C-space` | NO | Set mark |
| `C-\` | - | IME control |
| `C-quote` | NO | IntelliSense Suggestion |
| `C-doublequote` | △ | IntelliSense Parameter Hint |
| `M-x` | NO | Open command palette |
| `M-/(dabbrev)` | - | Auto-completion |
| `M-num command` | - | Repeat command `num` times |
| `C-M-SPC` | NO | Toggle SideBar visibility |

### File Command
|Command | Status | Desc |
|--------|--------|------|
| `C-o` | NO | Open a file |
| `C-x b` | NO | QuickOpen a file |
| `C-x C-f` | NO | Open a working directory |
| `C-x C-s` | NO | Save |
| `C-x C-w` | NO | Save as |
| `C-x i` | - | Insert buffer from file |
| `C-x C-d` | - | Open Folder |
| `C-x C-n` | - | Open new window |
| `C-x C-b` | - | Create new file and open |

## Conflicts with default key bindings
- `ctrl+d`: editor.action.addSelectionToNextFindMatch => **Use `ctrl+alt+n` instead**;
- `ctrl+g`: workbench.action.gotoLine => **Use `alt+g g` instead**;
- `ctrl+b`: workbench.action.toggleSidebarVisibility => **Use `ctrl+alt+space` instead**;
- `ctrl+space`: toggleSuggestionDetails, editor.action.triggerSuggest => **Use `ctrl+'` instead**;
- `ctrl+x`: editor.action.clipboardCutAction => **Use `shift+delete` instead**;
- `ctrl+v`: editor.action.clipboardPasteAction => **Use `shift+insert` instead**;
- `ctrl+k`: editor.debug.action.showDebugHover, editor.action.trimTrailingWhitespace, editor.action.showHover, editor.action.removeCommentLine, editor.action.addCommentLine, editor.action.openDeclarationToTheSide;
- `ctrl+y`: redo;
- `ctrl+m`: editor.action.toggleTabFocusMode;
- `ctrl+/`: editor.action.commentLine => **Use `ctrl+;` instead**;
- `ctrl+p` & `ctrl+e`: workbench.action.quickOpen => **Use `ctrl+x b` instead**;
- `ctrl+p`: workbench.action.quickOpenNavigateNext => **Use `ctrl+n` instead**.
