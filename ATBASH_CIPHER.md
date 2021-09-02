# Atbash Cipher

The atbash cipher is a type of substitution cipher with no key. 

Each letter is replaced with a seperate letter in the alphabet is replaced with the letter in the same position as if the alphabet was reversed (a with z, b with y etc...) as shown in this table

|Letter|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|
|------|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Encrypted Letter|z|y|x|w|v|u|t|s|r|q|p|o|n|m|l|k|j|i|h|g|f|e|d|c|b|a|


# Encrypting

To use this cipher just replace each letter with the corrosponding letter in the reversed alphabet.

# Decrypting

To decrypt text encrypted by this cipher just repeat the encryption progress to obtain the decoded text. 

# Examples

If we were to encipher 'Hello There' using this cipher the following steps would be followed. each letter would be replaced with the letter in the same position in the reversed alphabet. for 'h' the encrypted letter would be 's' this is repeated through the entire message resulting in the following 

|Letter|h|e|l|l|o|t|h|e|r|e|
|------|-|-|-|-|-|-|-|-|-|-|
|encrypted letter|s|v|o|o|l|g|s|v|i|v|

The encrypted message being 'svoolgsviv'

Decrypting follows the same process resulting in the following

|Letter|s|v|o|o|l|g|s|v|i|v|
|------|-|-|-|-|-|-|-|-|-|-|
|decrypted letter|h|e|l|l|o|t|h|e|r|e|