AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming
HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule

FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule



Developed by: K.ABINAYA
RegisterNumber:22005179  

 
LOGIC GATES

![Screenshot (5)](https://user-images.githubusercontent.com/121557762/211149328-d5871afa-f4ca-47c0-86af-5ff2ffa9509c.png)

OUTPUT
RTL

HALF SUBTRACTOR


![Screenshot (8)](https://user-images.githubusercontent.com/121557762/211149399-54301db2-e412-40b4-98ee-26d1dd9c0950.png)


FULL SUBTRACTOR

![Screenshot (9)](https://user-images.githubusercontent.com/121557762/211149415-45fb4d27-4ad5-4269-ae81-5bc44cbaeef7.png)


 TRUTH TABLE
 
 HALF SUBTRACTOR
 
 
![Screenshot (6)](https://user-images.githubusercontent.com/121557762/211149509-5f444539-642b-4ec6-938b-ac62fcdc3625.png)

FULL SUBTRACTOR


![Screenshot (7)](https://user-images.githubusercontent.com/121557762/211149553-7b526719-363d-4926-9506-522de476a90d.png)

 RTL realization

 Timing diagram 
 HALF SUBTRACTOR
 
 
 ![Screenshot (14)](https://user-images.githubusercontent.com/121557762/211149619-6199c807-775c-48a4-a7b9-2c1eea0eebc3.png)

FULL SUBTRACTOR
 
 ![Screenshot (15)](https://user-images.githubusercontent.com/121557762/211149653-6f05805e-89cd-4ad0-bda8-720f103f8d9c.png)


 Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
