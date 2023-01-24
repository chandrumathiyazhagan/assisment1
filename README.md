# assisment1

 F=(x+y')(x'+y)z' to design and simulate the logic diagram using Verilog
 
## AIM:

TO design and simulate the logic diagram using Verilog for F=(x+y')(x'+y)z'

## HARDWARE REQUIRED:

PC Cyclone || USB flasher

## SOFTWARE REQUIRED:

Quartus prime model sim

## THEORY
## INTRODUCTION:

To design and simulate the logic diagram for the expression F=(x+y')(x'+y)z', we will use the Verilog programming language. Verilog is a hardware description language that allows for the modeling, simulation, and synthesis of digital circuits.

First, we will start by declaring the input and output variables for our circuit. In this case, we have three inputs (x, y, and z) and one output (F).

module logic_diagram(input x, y, z, output F);

Next, we will use the Verilog operators to create the intermediate expressions for each term in the original equation. The "+" operator represents the logical OR operation, while the "'" symbol represents the logical NOT operation.

wire x_or_not_y = x + y';
wire not_x_or_y = x' + y;

Finally, we will use the "*" operator to represent the logical AND operation and connect the intermediate expressions to the output variable F.

assign F = x_or_not_y * not_x_or_y * z';

endmodule

With this Verilog code, we have successfully designed and modeled the logic diagram for the expression F=(x+y')(x'+y)z'. We can now use a simulation tool to test the circuit's behavior with different input values.
 
## LOGICAL EXPRESSION:
 
 F = (x AND NOT y) OR (NOT x AND y) AND NOT z
In simpler terms, this function is true when one of the following conditions is met:
x is true and y is false
x is false and y is true
However, this function is only true if z is false. If z is true, then the function is false.

## Procedure:

1.start the module using module program().
2.Declare the inputs and outputs.
3.Use wire to assign intermediate outputs.
4.Use and gates to get the desired output.
5.End the module.
6.Generate RTL realization and timing diagrams.

## PROGRAM:
```
Program to verify the truth table in quartus for the basic logic gates using Verilog programming. Developed by: CHANDRU.M RegisterNumber: 22008631

module MK(input x, y, z, output F);
    wire temp1,temp2;
    assign temp1=x|!y;
    assign temp2=!x|y;
    assign F=temp1|(temp2 & !z);
endmodule
```

## OUTPUT:
RTL Diagram

![Screenshot (76)](https://user-images.githubusercontent.com/119393023/214293497-767aecae-ae8c-4976-8de6-78e1df966f86.png)

## RTL Timing Diagram:

![Screenshot (77)](https://user-images.githubusercontent.com/119393023/214293681-46db98a4-43d1-4c8b-bae7-2bc38887b27d.png)

## TRUTH TABLE:

![ass 1](https://user-images.githubusercontent.com/119393023/214294649-d33b72a2-57bb-4b75-8b6f-2bfa78d7b509.jpg)


## RESULT:
Hence  has been implemented and verified using verilog code programming and its output are validated

