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
```

  module exp2(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
  wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
  assign x1=((~a)&(~b)&(~c)&(~d));
  assign x2=(a&(~c)&(~d));
  assign x3=((~b)&(c)&(~d));
  assign x4=((~a)&(b)&(c)&(d));
  assign x5=(b&(~c)&(d));
  assign f1=x1|x2|x3|x4|x5;
  
  assign y1=(x&(~y)&(z));
  assign y2=((~x)&(~y)&z);
  assign y3=((~w)&x&y);
  assign y4=(w&(~x)&(y));
  assign y5=(w&x&y);
  assign f2=y1|y2|y3|y4|y5;
  endmodule
```

Developed by: Thanushree Vijayakanth

Register Number: 212224110054





**RTL realization**

**Output:**

**Truth Table**

***1) F1***
![image](https://github.com/user-attachments/assets/099c0777-79bc-4c27-bd66-7fc5eb378a4c)

***2)*** F2![image](https://github.com/user-attachments/assets/b2c1e875-152e-4dcd-9fef-077e200745e6)




**RTL**
![image](https://github.com/user-attachments/assets/0cb55f35-47ab-44a6-89d1-d190bb5fec2c)

**Timing Diagram**
![image](https://github.com/user-attachments/assets/90618bd3-5bfb-4133-b83c-968255f617d6)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

