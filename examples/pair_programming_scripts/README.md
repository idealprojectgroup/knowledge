Brief instructions for the scripts
----------------------------------

**profile_dotfile**
- should be placed in the user's homedir
- should be renamed to `.profile`
- should have the corresponding user's file permissions and ownership


**tmux-pair-session**
- is a script that creates a brand new tmux server and session
- it creates a tmux server socket file in `/tmp/pair/` and `chmod`s that file to 777
- when session is created, a new tmux window is created too that connects to the server automatically
- this script should be tweaked (change server that does port forwarding) in order to work on your machine
