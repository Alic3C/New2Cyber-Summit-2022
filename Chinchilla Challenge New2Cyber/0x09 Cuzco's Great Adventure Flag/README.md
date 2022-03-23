# 0x09 Cuzco's Great Adventure Flag
> 20pts

## Category
> Web

## Briefing
> Cuzco was aware that the file had information about Parkour that would help her learn even more, so she decided it was safe, downloaded it, and tried to open it. That’s when she learned the file had been encrypted. Can you help her crack the password?

> She had one additional piece of information, this MD5 Hash: 51F8571B1EC5D507670802B3A5F06B65

## Solution
A Google search of the MD5 hash `51F8571B1EC5D507670802B3A5F06B65` gives the word `Parkour`. 

This can be confirmed via terminal:

```console
CDSkids@kali:~/Desktop$echo -n "Parkour" | md5sum
51f8571b1ec5d507670802b3a5f06b65
```

## Flag
Flag: `Parkour`