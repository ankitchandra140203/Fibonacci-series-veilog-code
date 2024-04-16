# Fibonacci series
 Digitally implementing fibonacci series with the help of fsm and writing its verilog code.
 
 ## -> let's break down the Verilog code

### Module Declaration:
This declares a module named fibonaci with three ports: reset, number, and value.
Reset is an input used to reset the module.
Number is a 4-bit input that specifies the number of Fibonacci sequence elements to generate.
Value is an 8-bit output that represents the current Fibonacci number.

### Internal Variables and Parameters:
A, B, and temp are registers to store intermediate values.
Count is a register to keep track of the current count of Fibonacci numbers generated.
State and next_state are registers used to control the state machine.
Start, sum, wr_reg1, wr_reg2, and result are parameters defining different states of the state machine.

### Clock Generation:
This block generates a clock signal with a period of 10 time units (#5). It starts with clk set to 0 and toggles it every 5 time units.

### Initialization:
Initializes count to 0, A to 0, and B to 1.

### State Machine:
The module uses a state machine to control the generation of Fibonacci numbers. The states are defined by the state register.
The state transitions are defined in the always @(*) block based on the current state and control signals.

### Counter Adjustment:
The count register is adjusted based on the current state to keep track of the number of Fibonacci numbers generated.

### Combinational Block:
This block calculates the next Fibonacci number (temp) based on the current state.

### Output Assignment:
Assigns the output value to the current Fibonacci number (temp).
