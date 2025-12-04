# FULL_ADDER_SUBTRACTOR
**Date:04/12/2025**
Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**
Full Adder
-------------------------------------
// Full Adder in Verilog
```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```
Full Sub
-------------------------------------
// Full Subtractor in Verilog
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule

```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Srimathi S
RegisterNumber:25017525
*/

**RTL Schematic**

**Output Timing Waveform**
***Full adder**
<img width="1018" height="659" alt="Screenshot 2025-12-04 160310" src="https://github.com/user-attachments/assets/d1f32795-d4e4-4ef7-88b9-55d5f4b2dd09" />
<img width="1321" height="368" alt="Screenshot 2025-12-04 160348" src="https://github.com/user-attachments/assets/66a1453b-14ec-4e4a-9927-400b37900f08" />


**Full subractor**
<img width="960" height="382" alt="Screenshot 2025-12-04 163510" src="https://github.com/user-attachments/assets/d714f64a-823a-435c-bccd-a38823c1000e" />

<img width="1228" height="426" alt="Screenshot 2025-12-04 163523" src="https://github.com/user-attachments/assets/5f7115f0-5284-4183-90a2-4997a05b8682" />

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
..


...
.
....
...
....
.
..
.
........
.
.
.
.
.
.'
.
.
.
.
.
.
.

.
.
.
.
.
.
.
.

/
.
.
.
.
.
.
.
.
.
.
.
.

..

..

