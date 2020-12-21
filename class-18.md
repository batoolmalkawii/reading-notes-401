# Cryptography

## Ceaser Cipher
Ceaser Cipher is one of the simplest and most widely known encryption techniques. 
It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet. 
For example, with a left shift of 3, D would be replaced by A, E would become B, and so on. 
The method is named after Julius Caesar, who used it in his private correspondence.

The encryption step performed by a Caesar cipher is often incorporated as part of more complex schemes, such as the Vigenère cipher, 
and still has modern application in the ROT13 system.
As with all single-alphabet substitution ciphers, the Caesar cipher is easily broken and in modern practice offers essentially no communications security.


> Example:
  The transformation can be represented by aligning two alphabets; the cipher alphabet is the plain alphabet rotated left or right by some number of positions.
  For instance, here is a Caesar cipher using a left rotation of three places, equivalent to a right shift of 23 (the shift parameter is used as the key):

  ```
  Plain:    ABCDEFGHIJKLMNOPQRSTUVWXYZ
  Cipher:   XYZABCDEFGHIJKLMNOPQRSTUVW
  ```

  When encrypting, a person looks up each letter of the message in the "plain" line and writes down the corresponding letter in the "cipher" line.

  ```
  Plaintext:  THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG
  Ciphertext: QEB NRFZH YOLTK CLU GRJMP LSBO QEB IXWV ALD
  ```
  Deciphering is done in reverse, with a right shift of 3.
  
 Also, The encryption can be represented using modular arithmetic by first transforming the letters into numbers, according to the scheme, 
 `A → 0, B → 1, ..., Z → 25.`


The replacement remains the same throughout the message, so the cipher is classed as a type of `monoalphabetic substitution`, as opposed to `polyalphabetic substitution`.

### Breaking Cipher:
The Caesar cipher can be easily broken even in a ciphertext-only scenario. Two situations can be considered:

  * an attacker knows (or guesses) that some sort of simple substitution cipher has been used, but not specifically that it is a Caesar scheme.
  * an attacker knows that a Caesar cipher is in use, but does not know the shift value.


