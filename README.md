# SSEM Project

## Introduction
This project is an implementation of the Small-Scale Experimental Machine (SSEM), also known as the Manchester Baby. The SSEM was the world's first stored-program computer. This project aims to simulate the SSEM using C++.

## Features
- **Processor Simulation**: Simulates the SSEM's processor, handling control instructions, present instructions, and accumulator operations.
- **Store Simulation**: Simulates the SSEM's storage, allowing loading, writing, and printing of instructions.
- **Instruction Set**: Implements a variety of operations including arithmetic, logical, and control operations.

## Directory Structure
- **Processor.h**: Header file defining the Processor class and its methods.
- **Processor.cpp**: Implementation of the Processor class.
- **Store.h**: Header file defining the Store class and its methods.
- **Store.cpp**: Implementation of the Store class.
- **Util.h**: Header file defining auxiliary functions and global variables.
- **Util.cpp**: Implementation of auxiliary functions.
- **main.cpp**: Main program that initializes the processor and store, and executes the fetch-decode-execute cycle.
- **Example.txt**: Example file containing machine instructions for the SSEM.
- **help.txt**: Help file providing instructions on how to run the program.
- **CMakeLists.txt**: CMake configuration file for building the project.

## Installation
To set up this project locally, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/YinheeeChen/SSEM-master.git
   cd SSEM-master
   ```

2. Create a build directory and navigate to it:
   ```sh
   mkdir build
   cd build
   ```

3. Generate the build files using CMake:
   ```sh
   cmake ..
   ```

4. Compile the project:
   ```sh
   make
   ```

## Usage
To use this project, follow these instructions:

1. Run the executable with the required arguments:
   ```sh
   ./SSEM procedure <all|single> file <filename> store <store size> register <register size>
   ```
   Example:
   ```sh
   ./SSEM procedure all file Example.txt store 64 register 64
   ```

2. You can also view the help file by running:
   ```sh
   ./SSEM -h
   ```

## Project Structure
- **Processor**: Handles the control instructions (CI), present instructions (PI), and accumulator (ACC) operations.
  - **increaseCI()**: Increases the control instruction counter.
  - **decodeOP()**: Decodes the operand and opcode from the present instruction.
  - **binToDec()**: Converts a binary sequence to a decimal number.
  - **decToBin()**: Converts a decimal number to a binary sequence.

- **Store**: Manages the storage of instructions.
  - **LoadFileIntoStore()**: Loads instructions from a file into the store.
  - **writeInStore()**: Writes instructions into the store.
  - **printStore()**: Prints the contents of the store.

- **Util**: Contains auxiliary functions and global variables.
  - **analyticArgs()**: Analyzes command-line arguments.
  - **fetchExecute()**: Executes the fetch-decode-execute cycle.
  - **display()**: Displays the current state of the processor and store.

## Contributing
If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Push the branch to your forked repository.
5. Create a pull request to the main repository.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
If you have any questions or suggestions, feel free to contact the authors:
- Yinhe Chen
- Jiarong He
- Jian Lu
- Haojun Xie
- Zhengyi Li
