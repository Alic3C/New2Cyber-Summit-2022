# 0x07 Another Pivot
> 75pts

## Category
> Network

## Briefing
> Connect to the second pivot

> IP: 10.112.3.12

> User: crease

> Pass: NoThatsaV

## Solution
```console
CDSkids@kali:~/Desktop$ssh -J tunneler@tunneler.threatsims.com:2222,whistler@1
0.218.176.199 crease@10.112.3.12
tunneler@tunneler.threatsims.com's password:
whistler@10.218.176.199's password:
The authenticity of host '10.112.3.12 (<no hostip for proxy command>)' can't be established.
ECDSA key fingerprint is SHA256:x7iaUdw97Mk64GKef+3SdjKPY8xZTqLA4fYsu6jQjcE.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.112.3.12' (ECDSA) to the list of known hosts.
crease@10.112.3.12's password:
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 4.15.0-171-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Thu Mar 24 09:26:35 2022 from 10.112.3.199
.___________. __    __  .__   __. .__   __.  _______  __       _______ .______
|           ||  |  |  | |  \ |  | |  \ |  | |   ____||  |     |   ____||   _  \
`---|  |----`|  |  |  | |   \|  | |   \|  | |  |__   |  |     |  |__   |  |_)  |
    |  |     |  |  |  | |  . `  | |  . `  | |   __|  |  |     |   __|  |      /
    |  |     |  `--'  | |  |\   | |  |\   | |  |____ |  `----.|  |____ |  |\  \----.
    |__|      \______/  |__| \__| |__| \__| |_______||_______||_______|| _| `._____|

ts{TunnelsInTunnelsInTunnels}

Pivot-2:

Not all SSH servers allow tunnels, so you have to get creative sometimes.

Socat is here if you need it.


$
```

## Flag
Flag: `ts{TunnelsInTunnelsInTunnels}`