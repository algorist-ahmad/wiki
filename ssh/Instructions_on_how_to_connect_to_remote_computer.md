
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

---

## BRAINSTORM

configuration is stored in /etc/ssh

How to do Passwordless SSH using ssh-copy-id Command:

(hold-up... the server doesn't actually need the private key? Recreate with entire flow)

```
client$ ssh-keygen
> 1 x 🔑 (private)
> 1 x 🗝️ (public)
```

SUCCESS

1. Port forwarding on Bel Modem

use curl command to discover Public IP as opposed to local IP
and use ip one-liner to discover Local IP

on router settings, set

Name = any string
Protocol = TCP
Internal port = port number
External port = Internal port value
Local IP = Local Ip

Save and activate

do ssh user@publicIp -p port

done.

add port forwarding to diagram

it stopped working???????

ping publicIp results in 100% packet loss, what could this mean???????
