
**status**: DRAFT

# title...

## Server side

verify sshd running

```systemctl status sshd```

If not running, do

```sudo systemctl start sshd```

Or start it daemon by itself??

```sshd```

3. Get computer's user ID with `whoami`
4. Get computer's IP address from either router admin page or some one-liner
5. ```ssh user@ipaddress```

## Client side

### LAN

From server, get *user* with ```whoami``` and get *localIp* with [MISSING METHOD]
On client side, to connect to computer in LAN, do

```ssh $user@$local-ip```

then enter `yes` if prompted, should now be connected.

### WAN

To connect in WAN, must specify port number ```ssh $user@$localIp -p $port```

## SORTME

configuration is stored in /etc/ssh
