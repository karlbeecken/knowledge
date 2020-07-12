---
layout: default
title: tmux cheatsheet
---

Tested
{: .label .label-green }
# tmux cheatsheet

- `tmux` – start new session
- `tmux new -s <name>` – start new named session
- `tmux a` – attach to existing session
- `tmux a -t <name>` – attach to named session
- `tmux ls` – list all sessions

For every other command inside tmux, hit `Ctrl-b` and then enter the desired command.

## General

- `t` – show big clock in current window/pane
- `d` – detach from current session
- `?` – show help

## Panes/Splits

- `%` – horizontal split
- `"` – vertical split
- `q` – show pane numbers
- `o` – swap panes
- `⍽` – toggle layouts
- `x` – kill current pane

## Windows/Tabs

- `c` – new window
- `p` – previus window
- `n` – next window
- `0`...`9` – selected window by number
- `,` – name window
- `w` – list windows
- `f` – find window
- `&` – kill window
- `.` – move window, prompts for new number
