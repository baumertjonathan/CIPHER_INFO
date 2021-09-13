# Playfair Cipher

The playfair cipher is a type of substitution cipher that takes a key to create a diagram/table used in encrypting. 

## Encrypting
To encrypt a string using the playfair cipher you first map the key to a 5x5 table. This is done by taking the first of each letter in the key, mapping it to the table left to right, top to bottom, then adding all other letters (in alphabetical order omitting either i or j) to the table. For example a key of 'secret' would produce the following table

|s|e|c|r|t|
|-|-|-|-|-|
|a|b|d|f|g|
|h|i|k|l|m|
|n|o|p|q|u|
|v|w|x|y|z|

then pair each letter in the message with another (adding an x for an odd number or to avoid matching letters) then each pair is looked at on the table and a set of rules is used to determine what the encrypted characters are. 

1: If the letters are in the same row of the table replace them with the letters to the right of them (wrapping as needed)

2: If the letters are in the same column of the table replace them with the letters dicectly below them (wrapping as needed)

3: If the letters are in nether the same row or column replace them with the letters on the same row but column of the other (opposite corners of the rectangle)

This is done for all pairs of letters. 

## Decrypting

Decrypting using the playfair ciphe is done similarly to encrypting except rules 1 and 2 are changed, for rule 1 it is to the left instead of right, and for 2 it is above instead of below Afterwards it may be necessary to remove excess 'x' from the resulting message. 

## Examples

If we were to encrypt the message 'Hello There' with a key of "super secret" the following steps would be made:

First map the key to the table, this is done by removing repeated letters (keeping only the first instance) and spaces. 

Key: 'super secret'

removed repeats: 'superct'

This is then placed on a 5x5 table

|s|u|p|e|r|
|-|-|-|-|-|
|c|t|.|.|.|
|.|.|.|.|.|
|.|.|.|.|.|
|.|.|.|.|.|

The rest of the table is filled with the remaining letters (omitting either i or j typically) in alphabetical order

|s|u|p|e|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|h|i|k|
|l|m|n|o|q|
|v|w|x|y|z|

Then the message is split into pairs of letters, pairs that are incomplete or have two of the same characters have an x appended to them

Message: 'Hello there'

Pairs:  'he', 'lx', 'lo', 'th', 'er', 'ex'

Then each pair is viewed in the table and we decide which rule should be applied to get the encrypted characters. 

for the pair 'he' we would look at them on the table

|s|u|p|`e`|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|`h`|i|k|
|l|m|n|o|q|
|v|w|x|y|z|

we see that they are not in the same row or column, so we would apply rule 3, this would result in each letter being replaced with the letter in the same row, opposite column (or opposite corners of the rectangle created by the two characters) this would result in the new characters being 'i' and 'p'

|s|u|`p`|`e`|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|`h`|`i`|k|
|l|m|n|o|q|
|v|w|x|y|z|

|pairs    |he|lx|lo|th|er|ex|
|---------|--|--|--|--|--|--|
|new pairs|ip|

Then we look at the next pair 'lx' on the table

|s|u|p|e|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|h|i|k|
|`l`|m|n|o|q|
|v|w|`x`|y|z|

This is another rule 3, giving us the pair 'nv'

|pairs    |he|lx|lo|th|er|ex|
|---------|--|--|--|--|--|--|
|new pairs|ip|nv|

The next pair 'lo' is in the same row, so we would apply rule 1 taking the letters to the right of them giving us the pair mq

|s|u|p|e|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|h|i|k|
|`l`|`m`|n|`o`|`q`|
|v|w|x|y|z|

|pairs    |he|lx|lo|th|er|ex|
|---------|--|--|--|--|--|--|
|new pairs|ip|nv|mq|

This is repeated for the remaining pairs, checking what rule to use then getting the resulting pair

|pairs    |he|lx|lo|th|er|ex|
|---------|--|--|--|--|--|--|
|new pairs|ip|nv|mq|ag|rs|py|

Resulting in an encrypted message of 'ipvmqagrspy'

To decrypt a similar process is followed with an altered rules 1 and 2. 

the same table is created

|s|u|p|e|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|h|i|k|
|l|m|n|o|q|
|v|w|x|y|z|

The message is split into pairs 'ip', 'nv', 'mq', 'ag', 'rs', 'py'

Then each pair of characters is looked at starting with 'ip'

|s|u|`p`|e|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|h|`i`|k|
|l|m|n|o|q|
|v|w|x|y|z|

|encrypted pairs|ip|nv|mq|ag|rs|py|
|---------------|--|--|--|--|--|--|
|decrypted pairs|he|

This would be a rule 3 which remains the same, This is repeated with the next pair resulting in 'lx'

|encrypted pairs|ip|nv|mq|ag|rs|py|
|---------------|--|--|--|--|--|--|
|decrypted pairs|he|lx|

The next pair 'mq' is in the same row so we use the adjusted rule 1 selecting the characters to the left giving us 'lo'

|s|u|p|e|r|
|-|-|-|-|-|
|c|t|a|b|d|
|f|g|h|i|k|
|`l`|`m`|n|`o`|`q`|
|v|w|x|y|z|

|encrypted pairs|ip|nv|mq|ag|rs|py|
|---------------|--|--|--|--|--|--|
|decrypted pairs|he|lx|lo|

repeat for the remaining pairs using the adjusted rules for decrypting 

|encrypted pairs|ip|nv|mq|ag|rs|py|
|---------------|--|--|--|--|--|--|
|decrypted pairs|he|lx|lo|th|er|ex|

This gives us the following message 'helxlotherex' you then remove the excess 'x' between paired letters and at the end giving us 'hellothere'