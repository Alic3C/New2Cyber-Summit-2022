# 0x04 Beacons Everywhere
> 75pts

## Category
> Network

## Briefing
> Something is Beaconing to the pivot on port 58671-58680 to ip 10.112.3.199, can you tunnel it back?

> NOTE: IT IS THE SAME ON EACH PORT ONLY USE ONE PORT AND REMOVE YOUR TUNNEL WHEN YOU ARE DONE

## Solution
For this challenge, you will need two terminals open. In the first one we need a netcat listener:

```console
CDSkids@kali:~/Desktop$nc -lvnp 1234
Listening on 0.0.0.0 1234
```

In the other terminal, SSH using the provided details:

```console
CDSkids@kali:~/Desktop$ssh -J tunneler@tunneler.threatsims.com:2222 whistler@1
0.218.176.199 -R 10.112.3.199:58671:127.0.0.1:1234
tunneler@tunneler.threatsims.com's password:
The authenticity of host '10.218.176.199 (<no hostip for proxy command>)' can't be established.
ECDSA key fingerprint is SHA256:EJ32X70iZRAHPgpgI+Sw7ly3MZrkAJa97+RWHMTkQaw.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.218.176.199' (ECDSA) to the list of known hosts.
whistler@10.218.176.199's password:
Welcome to Ubuntu 20.04.4 LTS (GNU/Linux 4.15.0-171-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Thu Mar 24 10:00:55 2022 from 10.218.176.93
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

Looking back at our netcat listener gives us the following information:

```console
Connection received on 127.0.0.1 54644
ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789    ts{GreatFirstReverseTunnel}    ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789
```

## Flag
Flag: ` ts{GreatFirstReverseTunnel}`