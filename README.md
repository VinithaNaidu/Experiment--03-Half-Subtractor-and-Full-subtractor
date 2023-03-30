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

### Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: D.Vinitha Naidu
RegisterNumber: 212222230175 

### Half Subtracter
```
module expfour(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference = (a^b);
assign borrow = (~a&b);
endmodule
```

### Full Subtracter:
```
module expfour(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign difference = (a^b^c);
assign borrow = (~a&(b^c)|(b^c));
endmodule
```

## Output:
### RTL:
### Half Subtracter:
![Screenshot_20230330_091807](https://user-images.githubusercontent.com/121166004/228892669-8c805957-be82-4f72-9b0c-21e611360411.png)

### Full Subtracter:
![Screenshot_20230330_091825](https://user-images.githubusercontent.com/121166004/228892850-c9d73de3-8d0e-484e-bdcb-40d678226e08.png)


## Truthtable:

### Half Subtracter:
![Screenshot_20230330_091758](https://user-images.githubusercontent.com/121166004/228893121-b1dd3561-2bd4-4c7d-ba60-5a991a623c75.png)

### Full Subtracter:
![Screenshot_20230330_092123](https://user-images.githubusercontent.com/121166004/228893247-4e12a45d-53ce-4434-a74d-acf6eb3f5bb7.png)

### Timing diagram :

### Half Subtracter:
![Screenshot_20230330_091818](https://user-images.githubusercontent.com/121166004/228893716-4bd4b909-8db0-4c3f-9d7e-20693c40c0f1.png)

### Full Subtracter:
![Screenshot_20230330_091833](https://user-images.githubusercontent.com/121166004/228893778-4cc1e5e6-4308-43e7-b0e8-7f846accdb0f.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
