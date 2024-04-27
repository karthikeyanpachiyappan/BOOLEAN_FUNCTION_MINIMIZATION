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
Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
```
Developed by: karthikeyan P
RegisterNumber:212223230102
```
module BMf1f2(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
  not(adash,a);
  not(bdash,b);
  not(cdash,c);
  not(ddash,d);
  and(p,bdash,ddash);
  and(q,adash,b,d);
  and(r,a,b,cdash);
  or(f1,p,q,r);
//type code for f2 as like f1
 not(ydash,y);
 and(s,x,y);
 and(t,ydash,z);
 and(u,w,y);
 or(f2,s,t,u);
endmodule
```

## RTL realization
![Screenshot 2024-04-27 111204](https://github.com/karthikeyanpachiyappan/BOOLEAN_FUNCTION_MINIMIZATION/assets/155143878/c2bb74a5-7b21-4346-96e7-429fc963d7c9)



## Timing Diagram
![Screenshot 2024-04-27 111651](https://github.com/karthikeyanpachiyappan/BOOLEAN_FUNCTION_MINIMIZATION/assets/155143878/b07c20c9-e7b9-45fe-956f-b1eda0ea1a48)

## Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

