# Beaufort Cipher

The Beaufort cipher is a type of substitution using the [tabula recta](https://en.wikipedia.org/wiki/Tabula_recta)

||a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|
|--|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|a|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|
|b|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|
|c|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|
|d|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|
|e|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|
|f|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|
|g|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|
|h|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|
|i|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|
|j|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|
|k|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|
|l|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|
|m|m|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|
|n|n|o|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|
|o|o|p|q|r|s|T|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|
|p|p|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|
|q|q|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|
|r|r|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|
|s|s|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|
|t|t|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|
|u|u|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|
|v|v|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|
|w|w|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|
|x|x|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|
|y|y|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|
|z|z|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|

This cipher functions similarly to the vigenere cipher but the encryption process follows closer to the decryption process of the vigenere cipher. 

## Encrypting

To encrypt using this cipher first if the key is shorter than the text you append the key on itself untill it is as long as the text. Then you pair each letter of the text with the letter of the key in the same position, then for each letter you find the column starting with the text you want to encrypt, follow that down untill you find the key, then follow the row of that key to the start, that is the encrypted character. 

## Decrypting

To decrypt text encoded with this cipher you just follow the same process as encrypting with the text and key. 

## Examples

If we were to encipher "Hello There" with the key "secret" the following process would be followed. First you would append the key on itself untill they are the same length like so:

|Text|h|e|l|l|o|t|h|e|r|e|
|----|-|-|-|-|-|-|-|-|-|-|
|Key-|s|e|c|r|e|t|s|e|c|r|

Then for the first pair of character (h and s) you find the 'h' column and search that column for 's', then the resulting encoded character is that column in this case that is the 'l' column

|Text|h|e|l|l|o|t|h|e|r|e|
|----|-|-|-|-|-|-|-|-|-|-|
|Key-|s|e|c|r|e|t|s|e|c|r|
|Encrypted Characters|l|

Repeat this process for all pairs

|Text|h|e|l|l|o|t|h|e|r|e|
|----|-|-|-|-|-|-|-|-|-|-|
|Key|s|e|c|r|e|t|s|e|c|r|
|Encrypted Characters|l|a|r|g|q|a|l|a|l|n|

This results in the following encrypted message 'largqalaln'

To decrypt this message you pair up the encrypted text and the key then follow the same process as encrypting

|Encrypted Text|l|a|r|g|q|a|l|a|l|n|
|--------------|-|-|-|-|-|-|-|-|-|-|
|Key|s|e|c|r|e|t|s|e|c|r|
|Decrypted characters|h|e|l|l|o|t|h|e|r|e|

resulting in the following decrypted message: 'hello there'