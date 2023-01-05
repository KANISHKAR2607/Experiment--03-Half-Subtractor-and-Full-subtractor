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
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: KANISHKAR M
RegisterNumber:  22007816

Half Subtractor
module halfsub(A,B,diff,borrow);
input A,B;
output diff,borrow;
assign diff=(A^B);
assign borrow=(~A&B);
endmodule

Full Subtractor
module fullsub(A,B,C,diff,borrow);
input A,B,C;
output diff,borrow;
assign borrow = (~A&(B^C)|(B&C));
assign diff = (A^B^C);
endmodule
```

## Output:

## Truthtable
Truth table for Half Subtractor

![half-subtractor truth table](https://user-images.githubusercontent.com/118886772/210710584-296ccc73-0037-484c-a96f-eaf711bd74c8.png)

Truth table for Full Subtractor

![full-subtractor truth table](https://user-images.githubusercontent.com/118886772/210710642-5cbf6f91-b137-4e63-86c9-273fb0250036.png)

##  RTL realization
RTL realization for Half Subtractor

![half sub logic diagram](https://user-images.githubusercontent.com/118886772/210711129-6d1caf66-0dae-46f7-8a61-f29aff2dd62f.png)

RTL realization for Full subtractor

![full sub logic diagram](https://user-images.githubusercontent.com/118886772/210711233-381c91ce-26ec-4396-a121-7cb25a3f3500.png)

## Timing diagram
Timing diagram for Half Subtractor

![half sub time diagram](https://user-images.githubusercontent.com/118886772/210711390-e779954c-ae08-4f27-8430-68ccf7b29e8a.jpg)

Timing diagram for Full Subtractor

![full sub time diagram](https://user-images.githubusercontent.com/118886772/210711531-b3829e56-5a2c-48d7-8cab-fb72d126d943.jpg)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
