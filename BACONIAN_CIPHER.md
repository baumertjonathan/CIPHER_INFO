# Baconian Cipher

The Baconian Cipher is a type of substitution cypher with no key where each letter is replaced by a series of 5 binary letters (typically 'A', and 'B'). There are two different tables that can be used in replacing the data, a traditional 24 letter table where i/j and u/v are paired, and a modern 26 letter table. 

24 Letter table
|Letter|Encrypted result|
|------|----------------|
|a|aaaaa|
|b|aaaab|
|c|aaaba|
|d|aaabb|
|e|aabaa|
|f|aabab|
|g|aabba|
|h|aabbb|
|i/j|abaaa|
|k|abaab|
|l|ababa|
|m|ababb|
|n|abbaa|
|o|abbab|
|p|abbba|
|q|abbbb|
|r|baaaa|
|s|baabb|
|t|baaba|
|u/v|baabb|
|w|babaa|
|x|babab|
|y|babba|
|z|babbb|

26 letter table
|Letter|Encrypted result|
|------|----------------|
|a|aaaaa|
|b|aaaab|
|c|aaaba|
|d|aaabb|
|e|aabaa|
|f|aabab|
|g|aabba|
|h|aabbb|
|i|abaaa|
|j|abaab|
|k|ababa|
|l|ababb|
|m|abbaa|
|n|abbab|
|o|abbba|
|p|abbbb|
|q|baaaa|
|r|baaab|
|s|baaba|
|t|baabb|
|u|babaa|
|v|babab|
|w|babba|
|x|babbb|
|y|bbaaa|
|z|bbaab|

## Encrypting

To encrypt using the baconian cipher you just check the table and replace the message letter by letter. 

## Decrypting

To decrypt using the baconian cipher you just check the table and replace the message letter by letter. 

## Examples

If we were to encrypt "Hello There" the following steps would be followed. Take the first letter and replace it with the corrosponding result from the table. 

|Letter|Encrypted Letter|
|------|----------------|
|h|aabbb|
|e|
|l|
|l|
|o|
|t|
|h|
|e|
|r|
|e|

Then repeat for each other lettter

|Letter|Encrypted Letter|
|------|----------------|
|h|aabbb|
|e|aabaa|
|l|ababa|
|l|ababa|
|o|abbab|
|t|baaba|
|h|aabbb|
|e|aabaa|
|r|baaaa|
|e|aabaa|

Resulting in the following encrypted message: aabbbaabaaababaababaabbab baabaaabbbaabaabaaaaaabaa

To decrypt a message encrypted with the Baconian Cipher the following steps would be followed. First split the message into chunks of 5 characters

|chunks|
|------|
|aabbb|
|aabaa|
|ababa|
|ababa|
|abbab|
|baaba|
|aabbb|
|aabaa|
|baaaa|
|aabaa|

Then for each chunk find the resulting letter from the tables

|chunks|decrypted character|
|------|-------------------|
|aabbb|h|
|aabaa|e|
|ababa|l|
|ababa|l|
|abbab|o|
|baaba|t|
|aabbb|h|
|aabaa|e|
|baaaa|r|
|aabaa|e|

resulting in the following decrypted text 'hello there'