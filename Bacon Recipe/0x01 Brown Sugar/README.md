# 0x01 Brown Sugar
> 25pts

## Category
> Forensics

## Briefing
> The accounts received a suspicious email with attachments today, and after opening the attachment it was all gibberish to them.

> After noticing some unusual behavior, scared of being infected, the operator shut down the system.

> Here's the network log of the system in question.

> There is a free gift from the organizers, find it!

## Solution
The provided file can be found [here](bacon_recipe.pcapng).

Some grep and strings quickly locate the flag:

```console
CDSkids@kali:~/Desktop$ strings bacon_recipe.pcapng > output.txt
CDSkids@kali:~/Desktop$ grep "flag{" output.txt
[{"html":"<p>Hey PwnEIP,</p>\n<p>What does RTFM mean?</p>\n<p>Regards,</p>\nLazzslayer<p></p>\n","headers":{"content-type":"multipart/alternative; boundary=\"===============6931498031006120959==\"","mime-version":"1.0","subject":"I have a question","to":"pwneip@bacon.threatsims.com","from":"\"Lazzslayer\" <lazzslayer@redteamvillage.io>","x-priority":"normal"},"subject":"I have a question","priority":"normal","from":[{"address":"lazzslayer@redteamvillage.io","name":"Lazzslayer"}],"to":[{"address":"pwneip@bacon.threatsims.com","name":""}],"id":"QncWHVnT","time":"2021-12-19T19:10:50.132Z","read":true,"envelope":{"from":{"address":"lazzslayer@redteamvillage.io","args":false},"to":[{"address":"pwneip@bacon.threatsims.com","args":false}],"host":"k0kut3n.k0kut3n.ts","remoteAddress":"172.16.95.133"},"source":"/tmp/maildev-1/QncWHVnT.eml","size":0,"sizeHuman":"0 bytes","attachments":null},{"html":"<p>What&#x2019;s the best gift ever?</p>\n<p>A broken drum. You just can&#x2019;t beat it.</p>\n<p>flag{g1f7_fr0m_th3_0rg4niz3r5}</p>\n","headers":{"content-type":"multipart/alternative; boundary=\"===============4960371473434655538==\"","mime-version":"1.0","subject":"what's the best gift ever?","to":"nopres
{"html":"<p>What&#x2019;s the best gift ever?</p>\n<p>A broken drum. You just can&#x2019;t beat it.</p>\n<p>flag{g1f7_fr0m_th3_0rg4niz3r5}</p>\n","headers":{"content-type":"multipart/alternative; boundary=\"===============4960371473434655538==\"","mime-version":"1.0","subject":"what's the best gift ever?","to":"nopresearcher@bacon.threatsims.com","from":"\"PwnEIP\" <pwneip@pwneip.com>","x-priority":"normal"},"subject":"what's the best gift ever?","priority":"normal","from":[{"address":"pwneip@pwneip.com","name":"PwnEIP"}],"to":[{"address":"nopresearcher@bacon.threatsims.com","name":""}],"id":"NnIckaZq","time":"2021-12-19T19:11:10.813Z","read":true,"envelope":{"from":{"address":"pwneip@pwneip.com","args":false},"to":[{"address":"nopresearcher@bacon.threatsims.com","args":false}],"host":"k0kut3n.k0kut3n.ts","remoteAddress":"172.16.95.133"},"source":"/tmp/maildev-1/NnIckaZq.eml","size":589,"sizeHuman":"589 bytes","attachments":null}
<p>flag{g1f7_fr0m_th3_0rg4niz3r5}</p>
```

## Flag
Flag: `flag{g1f7_fr0m_th3_0rg4niz3r5}`
