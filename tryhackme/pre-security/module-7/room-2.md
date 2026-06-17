# Module-7 : Attacks and Defences

## Room-2 : Cryptography Concepts

***

Data doesnt travel directly from the sender to receiver.  
It bounces through dozans of computers and routers along the way. Without protection anyone with access to those systems could read, change or block your data.  
Cryptography solves this by using mathematical rules and secret keys to scramble information into gibbrish that only authorized people can unscramble.  

***

### Basics 
- Plaintext = A message you can read normally.  
- Ciphertext = A scrambled version thats not supposed to make sense.
- Key = The secret ingredient that controls how scrambling and unscrambling works. Think of it as a password that algorithm uses.
- Algorithm = (The public recipe) The set of steps that explains how to use the key on the message. Everyone can know the algorithm. Security comes from keeping the key secret.

***

### Encryption Process
Plaintext + Key + Encryption Algorithm = Ciphertext

***

### Decryption Process
Ciphertext + Decryption Algorithm + Key = Plaintext

***

### Symmetric Encryption
1) The same key is used for encryption and decryption.
2) Both sender and receiver needs a copy of that key.
3) The key stays secret from everyone else.

#### Ceaser Cipher
- The Ceaser Cipher is an example of symmeteric encryption.
- Ceaser Cipher is, doing an offset by a particular number called key.
  ```
  HELLO ----> KHOOR
  offset = 3
  ```

#### Benefits 
1) Its Fast = Symmetric algorithm can churn through huge amounts of data really quickly.
2) Its Efficient = Perfect for encrypting files, had drives, and network traffic where speed matters.

#### Problem
How does the sender and receiver share the secret key in the first place?  
Send as `Plaintext`, then attackers will know the key.  
Send as `Ciphertext`, then that `Ciphertext` would need a key, how to send that, back to square one.  
This is called the `Key Distribution Problem`.  

***
