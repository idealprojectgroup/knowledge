Pair Programming setup

1. Logging to the same machine - port forwarding
================================================
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

2. Attaching to the same tmux session
=====================================
- tmux server socket has to be accessible            (i.e. in /tmp)
  $ tmux -S /tmp/something new

- tmux server socket has to be shared w other users
  $ chmod 777 /tmp/something

- other users attach
  $ tmux -S /tmp/something attach      # add `-r` for readme attach

3. Automatic attach to the tmux session (magic)
=======================================
- preconditions:
  - tmux has to be running and socket has to be 777

- `~/.profile` file magic (on OS X)



