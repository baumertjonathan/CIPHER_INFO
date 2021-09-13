# Bifid Cipher

The Bifid Cipher is both a substitution and transposition cipher, that takes a 25 character key and a period (used in transposition)

## Encrypting

To encrypt using this text you first form the key into a 5x5 square, then the coorinates of each letter in the text is found (row and column) then these pairs are split into periods based on the period, the pairs are then read rows then columns then put back through the square to get the resulting in the encrypted message. 

## Decrypting

To decrypt text encrypted by this cipher you first form the key into a 5x5 square then find the coordinates of each of these, then split these into groups twice as long as the period, the first half of these groups is the rows, the second is the columns. This is then put through the square again resulting in the decrypted message. 

## Examples

If we were to encrypt the message "Hello There" with a key of "qwertyuiopasdfghklzxcvbnm" and a period of 5 the following steps would be followed:


First form the key into a 5x5 square, this is done row by row resulting in the following square

|q|w|e|r|t|
|-|-|-|-|-|
|y|u|i|o|p|
|a|s|d|f|g|
|h|k|l|z|x|
|c|v|b|n|m|

Then the rows and columns are taken for each of the letters in the text. 

The first being 'H' this would give us row 3 and column 0

|Text  |h|e|l|l|o|t|h|e|r|e|
|------|-|-|-|-|-|-|-|-|-|-|
|row   |3|0|3|3|1|0|3|0|0|0|
|column|0|2|2|2|3|4|2|2|3|2|

Then it is seperated into sections based on the period

|Text  |h|e|l| |l|o|t| |h|e|r| |e|
|------|-|-|-|-|-|-|-|-|-|-|-|-|-|
|row   |3|0|3| |3|1|0| |3|0|0| |0|
|column|0|2|2| |2|3|4| |2|2|3| |2|

This example just happens to split by word, this will not usually be the case.

Then the columns are appended onto the rows with the following result:

303022 310234 300223 02

These are then split into pairs, representing rows and columns. 

|row   |3|3|2|3|0|3|3|0|2|0|
|------|-|-|-|-|-|-|-|-|-|-|
|column|0|0|2|1|2|4|0|2|3|2|


Then these rows/columns are put through the square the first one being row 3 and column 0 resulting in 'h'

|row      |3|3|2|3|0|3|3|0|2|0|
|---------|-|-|-|-|-|-|-|-|-|-|
|column   |0|0|2|1|2|4|0|2|3|2|
|encrypted|h|

then repeat for all other sets

|row      |3|3|2|3|0|3|3|0|2|0|
|---------|-|-|-|-|-|-|-|-|-|-|
|column   |0|0|2|1|2|4|0|2|3|2|
|encrypted|h|h|d|k|e|x|h|q|f|e|

this results in the encrypted message of 'hhdkexhqfe'

To decrypt this message we would first create the table using the key, then get the rows and columns for each character

|encrypted|h|h|d|k|e|x|h|q|f|e|
|---------|-|-|-|-|-|-|-|-|-|-|
|row      |3|3|2|3|0|3|3|0|2|0|
|column   |0|0|2|1|2|4|0|2|3|2|

