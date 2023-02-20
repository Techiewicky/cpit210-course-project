# Calculator Project:

### Introduction:
.
## Group Members

- [Baraa Majed Algomlas](https://github.com/Techiewicky)
- [Faisal Alzahrani](https://github.com/fsalzhrane)
- [Salman Balahwal](https://github.com/SalmanBalahwal)


### Contribution:
- Baraa Majed Algomlas 30%
- Faisal Alzahrani 40%
- Salman Balahwal 30%


## Problem Statement:



.

## Addition

### Half Adder:
Half Adder has two inputs, and it has two outputs which are the sum and carry. For example, if both inputs are 1 the output in sum will be 0 and the carry will be 1.

### Half Adder Circuit:

![Our Project](Images/Half%20Adder.png)

### Full Adder using combined Half-Adder:


### Full Adder Circuit:

![Our Project](Images/Full%20Adder.png)

### 8-bit parallel binary Adder:



### 8-bit Adder Circuit:

![Our Project](Images/8-Bit%20Adder.png)

## Subtraction
### 8-bit parallel binary Subtractor:


Subtraction can be represented as adding a positive number to a negative number,

for example: 4–2 = 4 + (-2) 

the real question is, how do we represent a negative number in binary?

One of the most efficient ways is to use 2’s complement which basically is to invert the added value and add 1 to the total.  
The way we will represent that in the Subtraction component we re-used the 8-bit adder the only difference is that the circuit inverts the B inputs and sets the carry input to 1.

As you can see, we added an enable button to control the circuit and to add 1 to the carry.

### Components: 
- 8-Bit Adder
- Not Gate
- Buffer

### Subtractor Circuit:

![Our Project](Images/Subtractor.png)

## Multiplication
### Multiplier Helper:

Firstly, when we want to implement the 8-Bit Multiplication Circuit we will use a lot of space, and also, we can’t just multiply 8x8 once, So In order to do it we need to understand how does Binary multiplication works.

In the case of a binary operation, we deal with only two digits, 0 and 1.

the only possible multiplication operations scenarios are:

0 × 0 = 0

0 × 1 = 0

1 × 0 = 0

1 × 1 = 1

If we take close look, we will notice that we can use an AND gate for this, 
but we can’t just multiply 8x8 we need to take it apart.

In order to do that we will use the multiplier helper.

The purpose of the multiplier helper is to multiply one bit by 8-Bits partially Then add them one by one using the 8-bit adder.
Let’s say we have A8xB8:

First we will calculate A8xB1 by multiplier helper

Then we will calculate A8xB2 by multiplier helper 

Then we add them together using 8-bit adder and so on until we reach A8xB8 … 

For example: 

A = 10110110

B = 10010110

A8xB1 = 10110110 x 0 = 00000000

because 0 AND 1 = 0

### Components: 
- AND Gate
- Splitter
### Multiplier Helper Circuit:

![Our Project](Images/Multiplier%20helper.png)

### Full Multiplier:

After finishing the multiplier helper our main problem is that the multiplier helper does 8 by 1 bit only so the main goal here is to expand this concept to a full 8
by 8 bit multiplication circuit allowing us to multiply two 8 bit binary numbers


First we used multiplier helpers and connected them with the inputs from A and B the idea here is to multiply the selected bit in B with all bits in A.

ex: A=11101010 B=1  

equal: 11101010

Then we used 8-bit parallel binary adder to take the outputs that are coming from 2 different multiplier helper to apply addition on the multiplication outputs and
proceed to do so with all the rest A*bi outputs,then
take 1 bit from every binary adder output to connect them in the end with the (lo) output and the rest of the last binary adder bits went to the (hi) output


### Components:
- Multiplier Helper
- 8-bit parallel binary Adder


![8x8Multiplier](Images/Full%20Multiplier.png)

## Final Circuit:
### Explanation:

<br>

### Final Circuit Design:

![Our Project](Images/Full%20project.png)
