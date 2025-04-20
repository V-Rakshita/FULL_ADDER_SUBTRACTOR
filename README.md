### Name: V. Rakshita
### Reg no: 212224100049

# EXP 4 - FULL ADDER AND FULL SUBTRACTOR

## **AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## **Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## **Full Adder and Full Subtractor**

### **Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

### **Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## **Procedure**

1. Open Quartus and create a new project. Go to File -> New -> Verilog HDL File and type the program.

2. Compile and run the program.

3. Then go to Tools -> NetList Viewers -> RTL Viewer and generate the RTL schematic and save the logic diagram.

4. Then go to File -> New -> University program VWF. Create nodes for inputs and outputs to generate the timing diagram.

5. Give different input combinations and go to Run Functional Simulation to generate the timing diagram.

## **Program:**

```
module FULLADDERSUBTRACTOR(a,b,bin,cin,sum,cout,diff,bout);
input a,b,bin,cin;
output sum,cout,diff,bout;
assign sum = a ^ b ^ cin;
assign cout = ((a^b) & cin) | (a&b);
assign diff = a ^ b ^ bin;
assign bout = (~(a^b) & bin)| (~a & b);
endmodule
```

## **Truth Table and Logic Diagram:**

![Screenshot (261)](https://github.com/user-attachments/assets/57447aaf-57e8-426b-ab5d-37b8aaa58fe6)

![Screenshot (239)](https://github.com/user-attachments/assets/8dbc4f64-c5cf-4c02-83ac-daa1cadf04bc)

## **Waveform:**

![Screenshot (240)](https://github.com/user-attachments/assets/9cf6c943-8dae-423c-93bf-37727c8c7ed7)

## **Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



