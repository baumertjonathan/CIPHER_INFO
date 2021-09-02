## Autokey Cipher

The autokey cipher is a type of substitution cipher that uses the [tabula recta](https://en.wikipedia.org/wiki/Tabula_recta)

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

This cipher functions similarly to the vigenere cipher except
when the key is shorter than the text the text is appended to the key. 

# Encrypting

To encrypt the text is first appended onto the key if the key is shorter than the text. Then each letter is is paired with the letter in the same position in the key. Then find the intersection of the two letters in the tabula, one headed on the row the other heading the column. 

# Decrypting

To dectypt the text you begin by pairing the first letter of the text with the first letter of the key. The column or row headed by the letter key is found then that row or column is searched for the encrypted letter. then theat is followed to the end of that row or column (opposite of what was used). Then that resulting character is appended onto the key. 

# Examples

If we were to encipher "Hello There" with the key "secret" the following process would be followed. First you would append the text on the key untill they are the same length like so:

|text|h|e|l|l|o|t|h|e|r|e|
|----|-|-|-|-|-|-|-|-|-|-|
|key |s|e|c|r|e|t|h|e|l|l|

Then the result of those two is found on the tabula recta, this is the encrypted character:

|text|h|e|l|l|o|t|h|e|r|e|
|----|-|-|-|-|-|-|-|-|-|-|
|key |s|e|c|r|e|t|h|e|l|l|
|encrypted character| z|i|n|c|s|m|o|i|c|p|

To decrypt this we would take the first letter of the key and first letter of the encrypted message and find the resulting row or column. 

|key|s|e|c|r|e|t|||||
|---|-|-|-|-|-|-|-|-|-|-|
|encrypted|z|i|n|c|s|m|o|i|c|p|
|decrypted|h|

Then the resulting letter is appended on the key

|key|s|e|c|r|e|t|h||||
|---|-|-|-|-|-|-|-|-|-|-|
|encrypted|z|i|n|c|s|m|o|i|c|p|
|decrypted|h|

This process is repeated with the next character


|key|s|e|c|r|e|t|h|e|||
|---|-|-|-|-|-|-|-|-|-|-|
|encrypted|z|i|n|c|s|m|o|i|c|p|
|decrypted|h|e|

this is repeated untill the entire message is decrypted

|key|s|e|c|r|e|t|h|e|l|l|
|---|-|-|-|-|-|-|-|-|-|-|
|encrypted|z|i|n|c|s|m|o|i|c|p|
|decrypted|h|e|l|l|o|t|h|e|r|e|