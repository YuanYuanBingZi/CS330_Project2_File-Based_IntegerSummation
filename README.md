# CS330_Project2_File-Based_Integer_Summation_in_C

## Project Overview
This project is written in C and is designed to read unsigned integers from two input files, compute their sums, and save the results in an output file. It demonstrates the use of dynamic memory allocation, file I/O operations, and efficient handling of large integers.

## Key Features
- **Dynamic Memory Allocation**: The program uses `malloc` to allocate memory based on the input file size, ensuring efficient memory management.
- **File I/O Operations**: It supports reading integers from input files and writing results to an output file, suitable for large data sets.
- **Modular Design**: The project is structured into several independent functions, each handling a specific task, making the code clean and easy to maintain.
- **Handling Large Integer Sums**: The program carefully manages integer summation to prevent overflow, ensuring accurate results with large datasets.

## Compilation and Execution
To compile the project, use the following command:
```bash
gcc -std=c11 main.c -o sum_ints
./sum_ints input1.txt input2.txt output.txt
```

## Function Descriptions

- **`int get_num_ints(char** argv)`**: Reads the number of integers in the input files.
- **`void allocate_mem(unsigned int** input_one, unsigned int** input_two, unsigned long int** output, int num_ints)`**: Dynamically allocates memory for input and output data.
- **`void get_ints(char** argv, unsigned int* input_one, unsigned int* input_two, unsigned long int* output, int num_ints)`**: Reads integers from the input files.
- **`void sum_ints(unsigned int* input_one, unsigned int* input_two, unsigned long int* output, int num_ints)`**: Adds two input arrays and stores the result in the output array.
- **`void save_output(char** argv, unsigned int* input_one, unsigned int* input_two, unsigned long int* output, int num_ints)`**: Saves the output data to the specified output file.

## Testing Instructions
The project includes test cases with the following files:

- Input files: file_1.txt and file_2.txt
- Output file: output.txt (You can compare this with the provided solution file file_3.txt)

To test the program, follow these steps:
- Prepare the input files in the correct format.
- Run the program as shown in the execution example.
- Verify the generated output file by comparing it to file_3.txt.

## Future Plans

1. **Expand Operations**:
   - Add support for additional arithmetic operations like subtraction and multiplication. This will make the program more versatile and useful for various mathematical tasks.

2. **Improve Error Handling**:
   - Implement more detailed error handling and reporting to cover edge cases like invalid file formats or incorrect input data, ensuring the program is more robust and user-friendly.

3. **Add Unit Tests**:
   - Develop a simple suite of automated unit tests to verify the correctness of each function. This will improve code reliability and make future updates easier to manage.