# 0x05 Cuzco's Great Adventure Flag
> 20pts

## Category
> Stego, OSINT

## Briefing
> Flag 5 Use the image file to find the question

## Solution
The provided file can be found [here](believe_with_layers.png).

Strings and a quick Google search make light work of this:

```console
CDSkids@kali:~/Desktop$ strings "believe_with_layers.png"
...
"FLAG 4 Question: Use OSINT, Who invented Parkour?"
"FLAG 5 Question: Use OSINT, What do you call someone who does Parkour?"
```

## Flag
Flag: `traceur`