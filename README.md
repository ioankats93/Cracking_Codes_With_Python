# Cracking Codes With Python
### These chapters are from Cracking Codes With Python Book written by Al Sweigart. <br>Every Chapter, generally alternate between a Cipher and how You can hack that cipher. <br>The Book can be found [Here](https://nostarch.com/crackingcodes).

# Brief Contents
- The Reverse Cipher
- The Caesar Cipher
- Hacking the Caesar Cipher with Brute-Force
- Encrypting with Transposition Cipher
- Decrypting with the Transposition Cipher
- Programming a Program to Test Your Program
- Encrypting and Decrypting Files
- Detecting English Programmatically
- Hacking the transposition Cipher
- A Modular Arithmetic Module for the Affine Cipher
- Programming the Affine Cipher
- Hacking The Affine Cipher
- Programming the Simple Substitution Cipher
- Hacking the Simple Substitution Cipher
- Programming the Vigenére Cipher
- Frequency Analysis
- Hacking the Vigenére Cipher
- The One-Time Pad Cipher
- Finding and Generating Prime Numbers
- Generating Keys for the Public Key Cipher
- Programming the Public Key Cipher

1) ### The Reverse Cipher
The reiverse cipher encrypts a message by printing it in reverse order. So "Hello, world!" encrypts to "!dlrow , olleH". To Decrypt, or get the original message, you simpy reverse the encrypted message. The encryption and the decryption steps are the same .

2) ### The Caesar Cipher
The reverse cipher encrypts the same way. But the Caesar cipher uses keys, which encrypt the message differently depending on which key is used. The keys for the Caesar cipher are the integers from 0 to 25. Even if a cryptanalyst knows the Caesar cipher was used, that alone doesn't give them enough information to break the cipher. The must also know the key.

3) ### Hacking The Caesar Cipher With Brute-Force
We can hack the Caesar cipher by using a cryptanalytic technique called brute-force. A brute-force attack tries every possible decryption key for a cipher.

4) ### Encrypting with Transposition Cipher
The transposition cipher is more difficult to brute force because the number of possible keys depends on the message's length. There are many different types of transposition ciphers, including the rail fence cipher, route cipher, Myszkowski transposition cipher. This example covers a simple transposition cipher called the ***columnar transposition cipher***

5) ### Decrypting with the Transposition Cipher
Steps for decrypting the Transposition Cipher :
  * Calculate the number of columns you need by dividing the length of the message by the key and then rounding up.
  * Draw boxes in columns and rows. Use the number of columns and you calculated before. The number of rows is the same as the key
  * Calculate the number of boxes to shade in by taking the total number of boxes and subtracking the length of the ciphertext message.
  * Shade in the number of boxes you calculated in step 3 at the bottom of the rightmost column.
  * Fill in the characters of the ciphertext starting at the top row and going from left to right. Skip any of the shaded boxes.
  * Get the plaintext by reading the leftmost column from top to bottom, and continuing to do the same in each column.

6) ### Programming A Program to Test Your Program
You can not be absolutely sure the programs always work unless you test the ***encryptMessage()*** and ***decryptMessage()*** functions with all sort of message and key parameter values. But this would take a lot of time because you would have to type a message in the encryption program, set the key, run the encryption program, paste the cipher txt into the decryption program, set the key, and then run the decryption program.

7) ### Encrypting And Decrypting Files
In previous examples, our programs have only worked on small messages that we type directly into the source code as string values. The cipher program we will make in this chapter will allow us to encrypt and decrypt entire files, which can be millions of characters in size.
