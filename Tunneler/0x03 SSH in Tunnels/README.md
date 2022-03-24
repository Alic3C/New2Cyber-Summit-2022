# 0x03 SSH in Tunnels
> 50pts

## Category
> Network

## Briefing
> SSH through the bastion to the pivot.

> IP: 10.218.176.199

> User: whistler

> Pass: cocktailparty

## Solution
```console
CDSkids@kali:~/Desktop$ssh -L 1234:10.174.12.14:80 tunneler@tunneler.threatsims.com -p 2222
tunneler@tunneler.threatsims.com's password:
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 4.15.0-171-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Thu Mar 24 00:59:11 2022 from 90.242.2.42
.___________. __    __  .__   __. .__   __.  _______  __       _______ .______
|           ||  |  |  | |  \ |  | |  \ |  | |   ____||  |     |   ____||   _  \
`---|  |----`|  |  |  | |   \|  | |   \|  | |  |__   |  |     |  |__   |  |_)  |
    |  |     |  |  |  | |  . `  | |  . `  | |   __|  |  |     |   __|  |      /
    |  |     |  `--'  | |  |\   | |  |\   | |  |____ |  `----.|  |____ |  |\  \----.
    |__|      \______/  |__| \__| |__| \__| |_______||_______||_______|| _| `._____|

ts{SSHtoANonStandardPort}

Bastion Hosts are an amazing way to provide secure access from a public internet to a private subnet.

A secure deployment of a bastion host would only allow users to ssh in with a ssh private key. We already failed and left ours open with a password, you should never do that.

We also put our SSH server on port 2222, this doesn't offer any security.  It just cuts down on the amount of logging we get from people scanning our host with tools like shodan.

The first challenge is to forward a port or forward tunnel to view a web server on an internal network.  The address is 10.174.12.14 and it is listening on port 80.

The second challenge is to connect to the pivot host.  The address is 10.218.176.199 with user: whistler and password: cocktailparty
tunneler@07be4d23d159:~$ ./ssh -L 22:tunneler.threatsims.com:2222 whistler@10.218.176.199
./ssh: /lib/x86_64-linux-gnu/libselinux.so.1: no version information available (required by ./ssh)
whistler@10.218.176.199's password:
bind [::1]:22: Cannot assign requested address
channel_setup_fwd_listener_tcpip: cannot listen to port: 22
Could not request local forwarding.
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 4.15.0-171-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Thu Mar 24 00:55:04 2022 from 10.218.176.93
.___________. __    __  .__   __. .__   __.  _______  __       _______ .______
|           ||  |  |  | |  \ |  | |  \ |  | |   ____||  |     |   ____||   _  \
`---|  |----`|  |  |  | |   \|  | |   \|  | |  |__   |  |     |  |__   |  |_)  |
    |  |     |  |  |  | |  . `  | |  . `  | |   __|  |  |     |   __|  |      /
    |  |     |  `--'  | |  |\   | |  |\   | |  |____ |  `----.|  |____ |  |\  \----.
    |__|      \______/  |__| \__| |__| \__| |_______||_______||_______|| _| `._____|

ts{IThoughtWeLostYouOnTheWay}

Pivot-1:

Some things you can do:

Something is Beaconing to the pivot on port 58671-58680 to ip 10.112.3.199, can you tunnel it back?

scan for the ftp server: 10.112.3.207 user: bishop pass: geese  (Its not where you think it is, also the banner is important)

connect to pivot-2 ip: 10.112.3.12 ssh port: 22 user: crease pass: NoThatsaV

connect to ip: 10.112.3.88 port: 7000, a beacon awaits you

$
```

## Flag
Flag: `ts{IThoughtWeLostYouOnTheWay}`