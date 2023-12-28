# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit
# Developed by: Naveen Kumar.T 
# Reference Number: 23002899
# Implementation-of-Half-Adder-and-Full-Adder-circuit
### Aim:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

# Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

# Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
![163552156-a13e5a56-c638-4110-97d9-8896907c8d25](https://github.com/820NaveenKumar208/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154746066/488ea778-131c-4868-9aca-bda55e3086a1)
#### Figure -01 HALF ADDER 

# Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.


                                         moduleHalfAdder(a,b,sum,carry);
                                         input a,b;
                                         output sum,carry;
                                         xor(sum,a,b);
                                         and(carry,a,b);
                                         endmodule



# RTL Realization:

![291238403-9aca016b-7128-4d2e-a901-ddaac9a35bec](https://github.com/820NaveenKumar208/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154746066/975d4308-7f8c-4812-814e-6c6435b3d8bc)

# Truth Table:

![291240788-11615dbf-2ba8-4e05-9fd9-334496a9e29f](https://github.com/820NaveenKumar208/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154746066/d257cbd8-6276-4a0c-b8ea-f7cf92617f91)

# Timing Diagram:

![291242520-99b728ac-2283-46ac-9177-ea99c810fa18](https://github.com/820NaveenKumar208/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154746066/60b3b592-1591-456d-ab49-6a3faf9db70a)



# Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

# Procedure:

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

# Program:

                  module Full Adder(a,b,c,sum,carry);
                  input a,b,c;
                  output sum,carry;
                  xor(sum,a,b,c);
                  assign carry=a&b|b&c|a&c;
                  endmodule              

# Truth Table:

![291243734-6f9b5471-6948-4c7f-9864-9075adaf1c7b](https://github.com/820NaveenKumar208/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154746066/ec84b13f-6283-4342-b1c1-6da8cc079d2b)

# RTL Realization:

![291243116-02586837-ef74-4e96-a02d-4600a635b24b](https://github.com/820NaveenKumar208/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154746066/05c54749-9dfc-45f6-bce0-880eb5aa684b)

# Timing Diagram:

![291243892-7c3a3c8d-f5d9-43ee-adb5-5b9ce2561be2](https://github.com/820NaveenKumar208/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/154746066/08e9f83f-bd81-4f62-9848-ac9381a08c99)

# Result:

Thus the given logic functions are implemented and their operations are verified using verilog programming.
