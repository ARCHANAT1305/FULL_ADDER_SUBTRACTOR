## DATE: 
#  EXPERIMENT NO: 3 FULL_ADDER_SUBTRACTOR

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
### FULL ADDER:
1. Inputs: a, b, c (carry-in)  
2. Outputs: s (sum), cout (carry-out)  
3. Calculate sum (s) as the XOR of a, b, and c.  
4. Calculate carry-out (cout) as the OR of all possible combinations of two inputs.

### FULL SUBRACTOR:
1. Inputs: a, b, c
2. Outputs: d (result), bout (borrow-out)
3. Calculate result (d) as the XOR of a, b, and c.
4. Calculate borrow-out (bout) as the OR of all possible combinations of two inputs with one inverted.

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.  
 Developed by:ARCHANA T  
 RegisterNumber:212223240013
## FULL ADDER:
module fadd(a,b,c,s,cout);   
input a;  
input b;   
input c; output s;   
output cout;  
assign s = (a ^ b) ^ c;  
assign cout = (a & b)|( b & c)|(c & a);   
endmodule  

**RTL Schematic**
![DG fulladd](https://github.com/ARCHANAT1305/FULL_ADDER_SUBTRACTOR/assets/145975189/37558a06-567d-4274-8f34-2e167c16bb2a)


**Output Timing Waveform**
![DG fulladd waveform](https://github.com/ARCHANAT1305/FULL_ADDER_SUBTRACTOR/assets/145975189/ac3dfe82-2a61-4bb7-b02d-7aefb57e7a19)

## FULL SUBRACTOR:

 input a;  
 input b;  
 input c;  
 output d;   
 output bout;   
 assign d = (a ^ b) ^ c;   
 assign bout = (~a & b)|( b & c)|(c & ~a);   
endmodule   

**RTL Schematic**
![image](https://github.com/ARCHANAT1305/FULL_ADDER_SUBTRACTOR/assets/145975189/64f4b63b-4a5b-41cb-b6a3-5e925b131e71)

**Output Timing Waveform**
![DG fullsub waveform](https://github.com/ARCHANAT1305/FULL_ADDER_SUBTRACTOR/assets/145975189/3da9804c-344d-4801-a2a4-6c9d19f98d8b)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



