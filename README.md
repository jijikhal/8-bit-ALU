# 8-bit ALU

This project contains all the files for a 8-bit arithmetic-logic unit made in the [Digital](https://github.com/hneemann/Digital) simulator. It is made of only basic gates (this mainly means that I did not use any more complicated things like sumators or multipliers) -- almost 3500 of them.

The unit supports the following operations (the arithmetic ones are all signed):

- Addition

- Subtraction

- Multiplication

- Division + modulo

- Shift and rotate in both directions

- AND, OR, XOR, NOT

- PASS (can be used for flags)

- Twos compliment

- INC and DEC

## Interface

The ALU has three input registers and three output registers. The two input 8-bit registers are used for the two operands and the other 4-bit register is used for selecting the OPT code

There are two output 8-bit registers, usually only one is used but for multiplication they connect into one 16-bit register. For DIV/MOD one of them is for division result and one for modulo result. There is also a 6-bit flag register with the following flags about the result:

- Overflow (OF)

- Zero (Z)

- Less than zero (LZ)

- Greater than zero (GZ)

- Parity (PAR)

- Error (ERR) -- only used for division by 0

## Usage

You need to have [Digital](https://github.com/hneemann/Digital) installed. Then you can either open the `demo.dig` file for easy usage of the ALU or any of the other files to see some smaller components used in the ALU. The `alu.dig` file contains the ALU itself.
