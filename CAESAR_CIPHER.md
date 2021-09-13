# Caesar Cipher

The Caesar cipher is a type of substituion cipher that takes a number as a key. 

## Encrypting
To encrypt a message using the Caesar cipher you replace each letter in the message with the letter (key) number of characters away from that letter within the alphabet. This wraps around for example if the letter is 'y' and the key is 5 the resulting character would be 'd'

## Decrypting

To decrypt a message encrypted using the Caesar cipher you replace each letter in the encrypted message with the letter (-key) away from that letter within the alphabet. This wraps around just like encrypting. 

## Examples

If we were to encrypt the message "Hello There" with a key of 3 using the caesar cipher we would first take the first letter and replace it with the letter e letters away from it (as the key is 3) within the alphabet. 
```
abcdefghijklmnopqrstuvwxyz
       ^  ^
       l l+3
```

|Letter   |h|e|l|l|o|t|h|e|r|e|
|---------|-|-|-|-|-|-|-|-|-|-|
|encrypted|k|

This is then repeated for each character in the message

|Letter   |h|e|l|l|o|t|h|e|r|e|
|---------|-|-|-|-|-|-|-|-|-|-|
|encrypted|k|h|o|o|r|w|k|h|u|h|

This results in the encrypted message "khoor wkhuh"

To decrypt a message encrypted with a Caesar cipher you do the same process in except subtracting the key instead of adding it. 

```
abcdefghijklmnopqrstuvwxyz
       ^  ^
      l-3 l
```

|encrypted|k|h|o|o|r|w|k|h|u|h|
|---------|-|-|-|-|-|-|-|-|-|-|
|Letter   |h|

This is repeated for each letter in the message

|encrypted|k|h|o|o|r|w|k|h|u|h|
|---------|-|-|-|-|-|-|-|-|-|-|
|Letter   |h|e|l|l|o|t|h|e|r|e|

resulting in the unencrypted message of 'hellothere'