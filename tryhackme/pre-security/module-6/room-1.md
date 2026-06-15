# Module-6 : Software Basics

## Room-1 : Data Representation

***

Data is representated in `0` and `1`.  

***

### Color Representation 
1) Binary :-
```
    R      G      B
   0,1    0,1    0,1  ---->  2x2x2 = 8 Combinations
```

8 different colors only for 1 bit representation.  

For 8 bit representation,  
2^8 = 256  
```
    R      G      B
   256    256    256  ---->  256x256x256 = more than 16,000,000 Combinations
```

Total bits = 8x3 = 24 bits  
Representing 24 bits with `0` and `1` is not so much convinient.  
Ex, 101000111110101000101010  
  
here comes Hexadecimal representation for rescue,  
256 ----> 8 bits ----> 1 byte  

2) Hexadecimal :-
We use group of 4 bits to represent hexadecimal code.
```
0 ----> 0000
1 ----> 0001
2 ----> 0010
3 ----> 0011
4 ----> 0100
5 ----> 0101
6 ----> 0110
7 ----> 0111
8 ----> 1000
9 ----> 1001
A ----> 1010
B ----> 1011
C ----> 1100
D ----> 1101
E ----> 1110
F ----> 1111
```
Ex,  
```
        1010-0011-1110-1010-0010-1010  ----> Binary
         A    3    E    A    2    A    ----> A3EA2A ----> Hexadecimal
```

***

### Number Representation
1) Decimal :- 21 = 2x10^1 + 1x10^0 = 21
2) Binary :- 1001 = 1x2^3 + 0x2^2 + 0x2^1 + 1x2^0 = 9
3) Hexadecimal :- 9BDF = 9x16^3 + 11x16^2 + 13x16^1 + 15x16^0 = 39,903
4) Octal :- 357 = 3x8^2 + 5x8^1 + 7x8^0 = 239

***


