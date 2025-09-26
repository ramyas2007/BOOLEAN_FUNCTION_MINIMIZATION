# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

 Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:RAMYA S

RegisterNumber:212224040268
```
module boolean_minimum(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
and(s,w,y);
and(t,x,y);
and(u,ydash,z);
or(f1,p,q,r);
or(f2,s,t,u);
endmodule
```


**RTL realization**
**Output:**
<img width="943" height="806" alt="Screenshot 2025-09-26 110754" src="https://github.com/user-attachments/assets/b51e8b98-9b97-4d59-a58c-8697a686ba72" />


**RTL**
**Timing Diagram**
<img width="1919" height="1112" alt="Screenshot 2025-09-26 113145" src="https://github.com/user-attachments/assets/da0bf823-1c5e-472e-a117-f73c654eb0ef" />

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

