# Rust-Calculator
Welcome to the second part of my ISP final product which is the calculator app that I developed as evidence of my journey learning Rust programming. I will show how to install, setup, and start using/modifying my work.

## Installation
First, please install the Rust toolchain through rustup and cargo. 
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Next, clone my repository to access the code:
```bash
git clone https://github.com/DragonflyRobotics/RustCalculator-ISP.git
```

Navigate into that directory and run the following:
```bash
cargo build
cargo run
```

This will compile my code and run the project locally.

## Usage
Using this app is relatively straightforward and instructions are provided in the program. 

### Visual Mode
Like Vim and Neovim, this program is bimodal: visual and edit. In visual mode, you cannot edit anything or run another calculation, you can only observe the calculations that have already been made or quit the program `q`. 

### Edit Mode
To enter edit mode from visual mode, press `e` and a cursor will appear over the textbox for editing. Here, you can type calculations like any four function calculator and it will compute the result. Decimal numbers and integers are supported. The following operations are currently supported:
```
+: Addition
-: Subtraction
*: Multiplication
/: Division
^: Power/Exponent
%: Modulo
&: Bitwise AND
```

After a calculation is typed, pressing enter (`<CR>`) will run the calculation and the result will be added to the history shown below.

## Not Supported
Currently, only one operation can be performed at a time and unary operations are not supported. To implement this, I must implement the following:
* Shunting Yard Algorithm for PEMDAS
* A better REGEX formula to extract all the unary operations
