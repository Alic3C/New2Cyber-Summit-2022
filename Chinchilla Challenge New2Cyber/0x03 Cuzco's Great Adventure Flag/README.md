# 0x03 Cuzco's Great Adventure Flag
> 20pts

## Category
> Web

## Briefing
> Cuzco deciphered the code, broke open the lock, and was about to break through the barriers when she found another clue.

> U2VjdXJpdHkgdGhyb3VnaCBvYnNjdXJpdHkgY2FuIGFsc28gbWVhbiB0aGF0IGl0IGlzIGp1c3QgaGlkZGVuIGluIHRoZSBsYXllcnM

## Solution
```console
CDSkids@kali:~/Desktop$ echo "U2VjdXJpdHkgdGhyb3VnaCBvYnNjdXJpdHkgY2FuIGFsc28gbWVhbiB0aGF0IGl0IGlzIGp1c3QgaGlkZGVuIGluIHRoZSBsYXllcnM" | base64 -d
Security through obscurity can also mean that it is just hidden in the layers
```

## Flag
Flag: `Base64`