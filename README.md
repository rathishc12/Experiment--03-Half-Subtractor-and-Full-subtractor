# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
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
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Rathish kumar C
RegisterNumber: 212222100043
*/
```
### HALF SUBTRACTOR:
```
module exp3(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule  
```   
### FULL SUBTRACTOR:
```
module exp31(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference=(a^b^c);
assign borrow=(~a&(b^c)|(b&c));
endmodule
```

## Output:
## Truthtable

### HALF SUBTRACTOR:
![exp4 1 tr](https://user-images.githubusercontent.com/120539823/230785711-cb86ef74-6d51-4909-90c6-2442d6a12f30.png)


### FULL SUBTRACTOR:
![full tr](https://user-images.githubusercontent.com/120539823/230785715-f2220f69-41a7-4d3d-b272-945a9b004359.png)



##  RTL realization
### HALF SUBTRACTOR:


![exp 4 1](https://user-images.githubusercontent.com/120539823/230786102-2b1cf2a9-7449-46ac-9cbc-4559d00b1b37.png)

### FULL SUBTRACTOR:

![4 1 full](https://user-images.githubusercontent.com/120539823/230786096-be9a9c62-3800-41b0-a5c5-0c55fd08f3f6.png)


## Timing diagram 

## HALF SUBTRACTOR:
![time1](https://user-images.githubusercontent.com/120539823/230786114-d59ca460-142e-423e-86bb-87a16027bae2.png)



FULL SUBTRACTOR:
![time 2](https://user-images.githubusercontent.com/120539823/230786128-133e5435-ca33-4c15-8e25-41121d4a8fb3.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
