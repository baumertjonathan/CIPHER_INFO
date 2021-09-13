# Affine Cipher

The affine cipher is a type of substitution cipher. 

The affine cipher takes two numbers as keys (*a* and *b*) *a* must be coprime with 26 (number of letters in the alphabet. ), and both *a* and *b* must be less than 26 and greater than 1

## Encrypting


|letter|a|b|c|d|e|f|g|h|i|j|k|l|m|n|o|p|q|r|s|t|u|v|w|x|y|z|
|------|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|number|0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25|

then the formula to find the enciphered character is 

(*ax*+*b*)mod(*m*)

 where *a* and *b* are the keys *x* is the letter being enciphered, and *m* is the length of the alphabet (26). Then the number is passed back through the table to get the enciphered letter. 

## Decrypting

To decrypt the cipher you first get the number associated with the letter then put it through the following function: 

*a*<sup>-1</sup>(*x*-*b*)mod(*m*)

where *a<sup>-1</sup>* is the multiplicative nverse of *a* in the group of integers modulo *m* to find this inverse we need to find a number *n* such that *an* = 1 (mod(*m*)). *b* is the key *b*, *x* is the number associated with the letter, and *m* is the length of the alphabet (26) The resulting number is then put through the chart and the decrypted letter is obtained. 

## Examples

If we were to encipher "Hello There" with the keys of 5 and 9 (*a* and *b* respectively) the following process would be followed. Each letter would be replaced with the number from the table

|Letter|h|e|l|l|o|t|h|e|r|e|
|------|-|-|-|-|-|-|-|-|-|-|
|Number|7|4|11|11|14|19|7|4|17|4

then each letter is put through the encryption function ((*ax*+*b*)mod(*m*)), for h it would look like this:

(5*7+9)mod(26)<br/>
(35+9)mod(26)<br/>
(44)mod(26)<br/>
18<br/>
s<br/>

this is repeated for each letter giving us the following result

|Letter|h|e|l|l|o|t|h|e|r|e|
|------|-|-|-|-|-|-|-|-|-|-|
|Number|7|4|11|11|14|19|7|4|17|4|
|f(number)|18|3|12|12|1|0|18|3|16|3|
|encrypted letter|s|d|m|m|b|a|s|d|q|d|

The enciphered text being 'sdmmbasdqd'

To decrypt this we would use the decryption function (*a*<sup>-1</sup>(*x*-*b*)mod(*m*)), for s it would look like this

5<sup>-1</sup>(18-9)mod(26)<br/>
21(18-9)mod(26)<br/>
21(9)mod(26)<br/>
(189)mod(26)<br/>
7<br/>
h<br/>

this process is repeated for each letter giving the following results:

|Letter|s|d|m|m|b|a|s|d|q|d|
|------|-|-|-|-|-|-|-|-|-|-|
|Number|18|3|12|12|1|0|18|3|16|3|
|f(Number)|7|4|11|11|14|19|7|4|17|4|
|decrypted letter|h|e|l|l|o|t|h|e|r|e|

The decrypted result being 'hellothere'