# HexCrypt 2.0.2
### This is an encryption and decryption library in python.


This program transforms any kind of text into a non-understandble block of _nosense looking_ characters and numbers.

For example, lets say that i want to encrypt _**"Hexade"**_, my GitHub name, it will be: **_"213d84812c5e7e5c62717e32896e61727354643f757b6671385c60"_**, to a normal person, _this is just a mess of numbers and characters, no one will ever think that there is a hidden message_, but we can send this to a friend, _for example_, to let them know something that everyone else wouldnt understand, or maybe you just want to hide your passwords in a TXT file on your computer but dont risk your accounts.

Cool! So how can i encrypt/decrypt it?

- `encryp( text )` will return the **encrypted text** when **normal text is introduced.**
- `decrypt( encrypted text)` will return the **original text** when an **encrypted text is introduced.**

  
> [!NOTE]
> Both funtions work with string values as input and output.

> [!WARNING]
> Too big texts can cause extreme lag or giant outputs.

> [!CAUTION]
> Using this tool wont work with some characters of some languages, symbols like "ö" or emojis will crash the program.


