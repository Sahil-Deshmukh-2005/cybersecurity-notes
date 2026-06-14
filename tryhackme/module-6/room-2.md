# Module-6 : Software Basics

## Room-2 : Data Encoding

***

Every character we know are just numbers with agreed meanings. This agreement is called an `Encoding`.  
If a sender has sent you a encoded file but you decoded using different type of encoder, what youll get is garbage characters.  

***

### Encoding 

***

#### 1. ASCII = American Standard Code for Information Interchange
Uses 7 bits.  
0-127 numbers to represent English letters, digits, punctuations, and some control characters.  

***

#### 2. ISO/IEC 8859 series (For European Languages)
ASCII numbers could not cover european characters.  
1) ISO-8859-1 : Covered Western European language
2) ISO-8859-2 : Covered Central/Eastern European language

***

❕Dont you see all these encoders as a headache to remember, what if we use different encoder, thats where `Unicode` comes in play.  

***

#### 3. Unicode
It is a universal character encoding standard. It assigns unique code points to characters from all modern and historical writing systems worldwide.  
That means we dont need to worry about what encoding type the sender is using we can decode it using `Unicode`.  
1) UTF-8 :  
Uses,
ASCII = 1 Byte,  
Non-ASCII = 2 Bytes,
Emoji = 4 Bytes.

2) UTF-16 :
Uses,
ASCII and Non-ASCII = 2 Bytes,
Emoji = 4 Bytes.

3) UTF-32 :
Uses,
4 Bytes for all but it wastes most bits.

***
