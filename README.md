# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

**Half adder**

```
module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule

```

Program to design a half adder and half subtractor circuit and verify its truth table in quartus using Verilog programming.
![WhatsApp Image 2025-11-15 at 20 39 05_55a97c33](https://github.com/user-attachments/assets/32ef7f6d-a255-4376-82f1-97e708278429)


**Half subtractor**

```
module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule
```

Program to design a half adder and half subtractor circuit and verify its truth table in quartus using Verilog programming.
![WhatsApp Image 2025-11-15 at 20 39 25_f36f6663](https://github.com/user-attachments/assets/602cbe13-9be6-49c4-9642-24d5c870f819)



Developed by: PERARASU K RegisterNumber: 25004665

**RTL Schematic Half adder**

![WhatsApp Image 2025-11-15 at 21 58 17_5bb27604](https://github.com/user-attachments/assets/f91c9c01-0bf8-4ccf-9ed1-33048d87537a)

**Half Subtractor**

![WhatsApp Image 2025-11-15 at 21 58 17_c2cef054](https://github.com/user-attachments/assets/d519dfcf-a1b0-4efe-bc3a-a51d6fac6153)



**Output/TIMING Waveform Half adder**

![image](https://github.com/user-attachments/assets/0597ca12-88b3-4231-878a-e3a4da2af7ff)

**Half subtractor**
![image](https://github.com/user-attachments/assets/5d6b55fe-2e1d-43a7-a3a5-51dd04b9b713)


**Result:**

Thus the a half adder and half subtractor circuit is designed and its truth table is verified in Quartus using Verilog programming .
