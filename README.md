## Introduction

Implemented a system that takes input as Instructions in Assembly Language and then outputs the values of the components(Registers and Flags) used in the execution of Instructions inside the Processor based on the Custom Instruction Set Architecture(ISA). The system consists of an [Assembler](https://www.techtarget.com/searchdatacenter/definition/assembler#:~:text=An%20assembler%20is%20a%20program,use%20the%20term%20assembly%20language.)(a computer program that takes basic computer instructions as input and converts them into a binary system as output) and [Simulator](https://www.dictionary.com/browse/simulator)(a program that simulates specific conditions or the characteristics of a real process or machine. Here, the Simulator would imitate the working of the Computer System by taking input as instructions as bits and outputting the state of Registers and Flags). A Scatter Plot is also plotted along with Simulator output depicting which memory address is accessed at what time while Simulator executes the Instructions.

## Flow Diagram

![dfdf - Page 14](https://github.com/abhit-rana/Toucan/assets/88608893/c7fb9a5d-8705-4d10-a760-e82a272264e4)

## Demo

* Assembler

https://github.com/abhit-rana/Toucan/assets/88608893/ec98de1e-50e4-4c7f-8fde-23887dc5e6ef

* Simulator and Scatter Plot

https://github.com/abhit-rana/Toucan/assets/88608893/d45bbf1e-ea05-490d-8f99-609e964d518f

* Entire System: Toucan

https://github.com/abhit-rana/Toucan/assets/88608893/eefc894b-0136-4a96-8059-f7f97bbd9bb8

## Contents of the Repo

* [Assembler](https://github.com/abhit-rana/Toucan/tree/main/Assembler): Contains the code for the Assembler: ToucanAssembler.java
* [Simulator](https://github.com/abhit-rana/Toucan/tree/main/Assembler): Contains the code for the Simulator: ToucanSimulator.java and for plotting the scatter plot: makeGraph.py
* [TestCases](https://github.com/abhit-rana/Toucan/tree/main/TestCases): Contains the test cases for the Assembler and Simulator.
* [TestCasesGeneratedOutput](https://github.com/abhit-rana/Toucan/tree/main/TestCasesGeneratedOutput): This directory would contain the output files from the Assembler and Simulator.
* [TestCasesSolutions](https://github.com/abhit-rana/Toucan/tree/main/TestCasesSolutions): It contains the solutions for the test cases listed in [TestCases](https://github.com/abhit-rana/Toucan/tree/main/TestCases) directory.
* [ISA-DESCRIPTION](https://github.com/abhit-rana/Toucan/blob/main/ISA-DESCRIPTION.pdf): Information regarding the Instruction Set Architecture(ISA) used in the Assembler and Simulator
* [Project_Components_Description](https://github.com/abhit-rana/Toucan/blob/main/Porject_Components_Description.pdf): Information regarding the working of the Assembler, Simulator, and Scatter Plot.
* [runAssembler.py](https://github.com/abhit-rana/Toucan/blob/main/runAssembler.py): Run the Assembler.
* [runSimulator.py](https://github.com/abhit-rana/Toucan/blob/main/runSimulator.py): Run the Simulator.
* [runToucan.py](https://github.com/abhit-rana/Toucan/blob/main/runToucan.py): Run the Entire System: Toucan.

## Installing the System

**1. Downloading the Repo**

* Go to the Homepage of this Repo. Download the ZIP FILE from the "<> Code" button there.
* Extract the ZIP file where you want
* Rename the Downloaded folder(Toucan-main) to be - Toucan

**2. Setting up a virtual environment**
```
pip3 install virtualenv
virtualenv Toucan
```

**4. Making the files inside Toucan to be executable**
```
chmod -R 701 Toucan/
```

**5. Opening up the Repo**
```
cd DaargiBot
```

**6. Activating Virtual Environment**
```
source bin/activate
```

**7. Downloading the Required Python Packages**
```
pip3 install -r requirements.txt
```

Hurray, we are all set up!!

## Running the Assembler

INPUT - INSTRUCTIONS IN ASSEMBLY LANGUAGE

OUTPUT - INSTRUCTIONS IN BINARY SYSTEM

**FORMAT:**

python3 runAssembler.py assembler_test_file_name assembler_solution_file_name


**Example:**
```
python3 runAssembler.py at2 sat2
```

**Note:**

* If you don't have the solution file, leave the assembler_solution_file_name argument empty.
* **Add the new test cases and their solution to the assigned folders, TestCases/Assembler and TestCasesSolutions/Assembler, respectively**.

The Output file of the test case would be inside "TestCasesGeneratedOutput/Assembler/" with the same name as the test file. If the Solution file were provided, the result of whether the output file matched the solution file would be provided in the output.

## Running the Simulator

INPUT - INSTRUCTIONS IN BINARY SYSTEM

OUTPUT - VALUE OF PROGRAM COUNTER, REGISTERS, AND FLAGS AFTER EXECUTING EACH INSTRUCTION. SCATTER PLOT FILE.


**FORMAT:**

python3 runSimulator.py simulator_test_file_name simulator_solution_file_name


**Example:**
```
python3 runSimulator.py st2 sst2
```

**Note:**

* If you don't have the solution file, leave the simulator_solution_file_name argument empty.
* **Add the new test cases and their solution to the assigned folders, TestCases/Simulator and TestCasesSolutions/Simulator, respectively**.

The Output file of the test case would be inside "TestCasesGeneratedOutput/Simulator/" with the same name as the test file. If the Solution file were provided, the result of whether the output file matched the solution file would be provided in the output. **The scatter plot would be available as a Plot.png file inside "Simulator/"**.

## Running the Entire System: Toucan

INPUT - INSTRUCTIONS IN THE FORM OF ASSEMBLY LANGUAGE

OUTPUT - VALUE OF PROGRAM COUNTER, REGISTERS, AND FLAGS AFTER EXECUTING EACH INSTRUCTION. SCATTER PLOT FILE.

**FORMAT:**

python3 runToucan.py toucan_test_file_name=assembler_test_file_name assembler_solution_file_name toucan_solution_file_name=simulator_solution_file_name


**Example:**
```
python3 runToucan.py at2 sat2 sst2
```

**Note:**

* If you don't have the solution files, empty the assembler_solution_file_name and simulator_solution_file_name arguments.
* **Add the new test cases and their solution to the assigned folders, TestCases/Assembler, TestCasesSolutions/Assembler, and TestCasesSolutions/Simulator, respectively**.

For the given test case, the output file from Assembler would be inside "TestCasesGeneratedOutput/Assembler" with the letter 's' appended to the name of the test file that would be input to the Simulator. The output from the Simulator would be inside "TestCasesGeneratedOutput/Simulator/" with the word "sst" followed by the digit(i.e., 1, 2, or 3) that would be the output from the Toucan system. **The scatter plot would be available as a Plot.png file inside "Simulator/"**.
