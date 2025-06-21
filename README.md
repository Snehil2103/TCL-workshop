# TCL Scripting for Synthesis and Pre-Layout Timing Analysis in VLSI Design from Fundamentals to Advanced Techniques

Tool Command Language (TCL) is a powerful scripting language widely used in the field of VLSI for automating EDA tools. It is used for writing re-usable scripts for automating synthesis, PnR and timing analysis.

The Main goal of this repository is to develop a TCL script that takes a CSV file containing Design name, Output directory, Netlist directory, Early library path, Late library path and Constraints file to generate the Synthesized netlist for the RTL using an Open-source tool Yosys and perform STA using Open-Timer.

# Day 1: Introduction to TCL and VSDSYNTH ToolBox Usage

# TASK:

- Write a Shell script & TCL script to automate Synthesis and Static timing analysis of the Design details mentioned in CSV file

![Screenshot 2025-06-21 114624](https://github.com/user-attachments/assets/48e284b5-29b7-4f00-9c4b-ae4bde752b94)

# SUB-TASKS:

- Create a shell script and pass csv from UNIX shell to TCL script
- Convert all inputs in csv to format[1] & SDC format and pass to synthesis tool 'Yosys'
- Convert format[1] & SDC to format[2] and pass to timing tool 'Opentimer'
- Generate output report

![Screenshot 2025-06-21 114811](https://github.com/user-attachments/assets/942e1d4e-9c7d-45c9-9ac2-34c6ae993bf1)

Start the shell script with a shebhang. It tells the system which interpreter to use to run the script

```#!/bin/tcsh -f```

There are three general scenarios to consider from user point of view while writing the shell script

- Not provide .csv file as input
- Provide a .csv file which doesn't exist
- Type "-help" to find out the usage

![Image](https://github.com/user-attachments/assets/20bce904-eccc-4e9b-9856-8ee40240a27d)

To give execution permission to a shell script, use the following command in the bash

```chmod +x script_name```

# Day 2: Variable Creation and Processing Constraints from CSV

![Screenshot 2025-06-21 114438](https://github.com/user-attachments/assets/2b27f163-0c40-4306-9eba-00382eed9f63)

- Auto Creation of variables using matrix and arrays

 ![Screenshot 2025-06-19 182110](https://github.com/user-attachments/assets/86f48374-3b99-462e-8e18-7bd3ac352282)

- Checking the existence and files and folders mentioned in design_details.csv

 ![Screenshot 2025-06-19 182651](https://github.com/user-attachments/assets/c63d9363-5e9c-49bd-99e8-50eacb4f7b8a)

# Day 3: Processing constraints.csv file and generating SDC format

SDC - Synopsys Design Constraints format is industry standard format which is widely accepted by many EDA tools for various stages flow.

- Algorithm :

- From the constraints.csv file, a matrix named 'constraints' is created using the command ```::struct::matrix constraints```
- A rectangular search space is created and values in that space are accessed through row and column numbers
- After accessing the values, they are converted to SDC format through TCL code
- This is done seperately for clock, input and output constraints

![Screenshot 2025-06-21 123542](https://github.com/user-attachments/assets/86019fd5-9d4a-4e8e-b9e5-d2bc13d924ef)

- Processing clock constraints and conversion to SDC format

 ![Screenshot 2025-06-19 184519](https://github.com/user-attachments/assets/f5548e84-0d70-469a-a148-4117280264e5)

 ![Screenshot 2025-06-19 184249](https://github.com/user-attachments/assets/c5794837-5baa-48e2-a8b6-d20f9ec41f12)

- Categorizing as input constarints as bits and bussed and conversion to SDC format

 ![Screenshot 2025-06-19 185811](https://github.com/user-attachments/assets/50bd881c-48c2-434b-bb87-a3d89430a0b5)

 ![Screenshot 2025-06-19 190013](https://github.com/user-attachments/assets/131381cc-366e-4d91-89de-ece70bb75840)

- Processing output constraints and conversion to SDC format

 ![Screenshot 2025-06-19 190724](https://github.com/user-attachments/assets/8982241c-dec2-4d83-bb3d-ff43711efadd)

 ![Screenshot 2025-06-19 190632](https://github.com/user-attachments/assets/8bc839fa-aaca-4a94-ae29-e41c5b842af7)
 


 





















