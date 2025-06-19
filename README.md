# TCL Scripting for Synthesis and Pre-Layout Timing Analysis in VLSI Design from Fundamentals to Advanced Techniques

Tool Command Language (TCL) is a powerful scripting language widely used in the field of VLSI for automating EDA tools. It is used for writing re-usable scripts for automating synthesis, PnR and timing analysis.

The Main goal of this repository is to develop a TCL script that takes a CSV file containing Design name, Output directory, Netlist directory, Early library path, Late library path and Constraints file to generate the Synthesized netlist for the RTL using an Open-source tool Yosys and perform STA using Open-Timer.

# Day 1: Introduction to TCL and VSDSYNTH ToolBox Usage

# TASK:

- Write a Shell script & TCL script to automate Synthesis and Static timing analysis of the Design details mentioned in CSV file

# SUB-TASKS:

- Create a shell script and pass csv from UNIX shell to TCL script
- Convert all inputs in csv to format[1] & SDC format and pass to synthesis tool 'Yosys'
- Convert format[1] & SDC to format[2] and pass to timing tool 'Opentimer'
- Generate output report

Start the shell script with a shebhang. It tells the system which interpreter to use to run the script

```#!/bin/tcsh -f```

There are three general scenarios to consider from user point of view while writing the shell script

- Not provide .csv file as input
- Provide a .csv file which doesn't exist
- Type "-help" to find out the usage

To give execution permission to a shell script, use the following command in the bash

```chmod +x script_name```

# Day 2: Variable Creation and Processing Constraints from CSV














