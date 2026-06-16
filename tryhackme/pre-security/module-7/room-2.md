# Module-7 : Attacks and Defences

## Room-2 : Cryptography Concepts

Data doesnt travel directly from the sender to receiver.  
It bounces through dozans of computers and routers along the way. Without protection anyone with access to those systems could read, change or block your data.  
Cryptography solves this by using mathematical rules and secret keys to scramble information into gibbrish that only authorized people can unscramble.  

### Basics 
- Plaintext = A message you can read normally.  
- Ciphertext = A scrambled version thats not supposed to make sense.
- Key = The secret ingredient that controls how scrambling and unscrambling works. Think of it as a password that algorithm uses.
- Algorithm = (The public recipe) The set of steps that explains how to use the key on the message. Everyone can know the algorithm. Security comes from keeping the key secret.

### Encryption Process
Plaintext + Key + Encryption Algorithm = Ciphertext

### Decryption Process
Ciphertext + Decryption Algorithm + Key = Plaintext

