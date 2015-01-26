# Pair Programming with tmux

## 0. Setup Files

**profile_dotfile**
- should be placed in the user's homedir
- should be renamed to `.profile`
- should have the corresponding user's file permissions and ownership


**tmux-pair-session**
- is a script that creates a brand new tmux server and session
- it creates a tmux server socket file in `/tmp/pair/` and `chmod`s that file to 777
- when session is created, a new tmux window is created too that connects to the server automatically
- this script should be tweaked (change server that does port forwarding) in order to work on your machine

## 1. Logging to the same machine - port forwarding

- buy new DigitalOcean server
- ssh deamon setup (one time)
  - in `/etc/ssh/sshd_config` ensure there's: `GatewayPorts yes`
  - $ kill ssh-deamon-process-pid

- do remote port forwarding for rails server
  $ ssh -R2345:localhost:3000 name_of_server

- do remote port forwarding for ssh            # this is the one-liner to remember
  $ ssh -R2345:localhost:22 name_of_server

- allow others to log-in as: tmux; password123
  $ ssh -p2345 tmux@name_of_server             # this logs you directly to my server

## 2. Attaching to the same tmux session

- tmux server socket has to be accessible            (i.e. in /tmp)
  $ tmux -S /tmp/something new

- tmux server socket has to be shared w other users
  $ chmod 777 /tmp/something

- other users attach
  $ tmux -S /tmp/something attach      # add `-r` for readme attach

## 3. Automatic attach to the tmux session (magic)

- preconditions:
  - tmux has to be running and socket has to be 777

- `~/.profile` file magic (on OS X)



