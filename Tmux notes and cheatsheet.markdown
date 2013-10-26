# Tmux notes and cheatsheet

* `ctrl-a,c` = create a new window
* `ctrl-a,n` = next window
* `ctrl-a,p` = previous window
* `ctrl-a,w` = list of windows
* `ctrl-a,0` = selects window at 0
* `ctrl-a + ,` = rename the current window

## Layouts
* `ctrl-a, spacebar` = cycle through layouts
* `ctrl-a,%` = split window vertically
* `ctrl-a,"` = split window horizontally
* `ctrl-a,o` = moves the cursor back and forth between panes
* `ctrl-a,ctrl-o` = swaps the order of the panes

## Sessions
* `ctrl-a,d` = detach tmux session
* `tmux ls` = lists open sessions
* `tmux attach -t session_name` = attaches to a session
* `tmux attach -t 0` = attaches to session at index 0
