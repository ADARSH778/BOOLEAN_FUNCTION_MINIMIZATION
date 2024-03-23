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
```
module booleanmin(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule
 

Developed by:R Adarsh Chowdary
 RegisterNumber:212223040166

```
**RTL realization**

**Output:**

**RTL**
![Screenshot (28)](https://github.com/ADARSH778/BOOLEAN_FUNCTION_MINIMIZATION/assets/149347361/9c41f91f-9598-4474-b862-1d3de27f9cec)

**Timing Diagram**
![Screenshot (27)](https://github.com/ADARSH778/BOOLEAN_FUNCTION_MINIMIZATION/assets/149347361/e113328f-3a54-433f-8798-c801db502104)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

