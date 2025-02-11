LEARN CUDA KERNEL BASICS WITH ANJUL
===================================
Build Status: passing

Welcome to "Learn CUDA Kernel Basics with Anjul"! This repository is your gateway to understanding the fundamentals of CUDA programming through hands-on examples. Whether you're just starting with GPU computing or looking to sharpen your parallel programming skills, these examples offer clear insights into how CUDA works.

-----------------------------------------------------------------------
TABLE OF CONTENTS
-----------------------------------------------------------------------
1. Project Overview
2. Repository Structure
3. Prerequisites
4. Getting Started
   a. Cloning the Repository
   b. Compiling the Code
5. Code Insights
6. Further Improvements
7. Contributing
8. Contact

-----------------------------------------------------------------------
PROJECT OVERVIEW
-----------------------------------------------------------------------
This project is divided into FOUR interactive examples that build your CUDA programming skills step by step:

1. SIMPLE 1D VECTOR ADDITION
   - A straightforward CUDA program that performs element-wise addition of two 1D vectors.
   - Learn the basics of memory allocation, data transfer between the host (CPU) and the device (GPU),
     kernel execution, and result retrieval.

2. 1D VECTOR ADDITION WITH BLOCKS
   - Enhance your understanding of CUDA's grid and block architecture by partitioning the vector addition
     task among multiple blocks and threads.
   - This example illustrates how to scale your computation effectively.

3. 2D MATRIX ADDITION
   - Extend the concept of vector addition to 2D matrices.
   - This example covers thread mapping for two-dimensional data structures and demonstrates more complex
     memory management strategies.

4. COMBINED SUMMARY
   - A comprehensive summary that brings together the insights from the previous examples.
   - Serves as a quick reference for the concepts learned and provides best practices for writing efficient CUDA code.

-----------------------------------------------------------------------
PREREQUISITES
-----------------------------------------------------------------------
Before diving in, ensure you have the following installed:

- NVIDIA CUDA Toolkit
  Download and install the CUDA Toolkit (version 10.x or later is recommended)
  from: https://developer.nvidia.com/cuda-toolkit

- CUDA-Capable GPU
  A GPU that supports CUDA is required to run the programs.

- Compiler
  The NVIDIA CUDA Compiler (nvcc) is used to compile the source files.

- Operating System
  These examples have been tested on Linux and Windows. Adjustments might be needed for other OS.

-----------------------------------------------------------------------
GETTING STARTED
-----------------------------------------------------------------------

Cloning the Repository:
-----------------------
Clone this repository to your local machine with the following commands:

    git clone https://github.com/anjul1008/LearnCudaKernelBasicsWithAnjul.git
    cd LearnCudaKernelBasicsWithAnjul

Compiling the Code:
-----------------------
You have two options to compile the code: using the Makefile or compiling manually with nvcc.

1. Using the Makefile:
   -----------------------
   The Makefile simplifies the build process.

   To compile ALL examples, run:

       make all

   To compile an individual example, specify the target. For example:

   - Simple 1D Vector Addition:
       
         make simple_vector_addition
         ./simple_vector_addition

   - 1D Vector Addition with Blocks:
       
         make vector_addition_blocks
         ./vector_addition_blocks

   - 2D Matrix Addition:
       
         make matrix_addition
         ./matrix_addition

   - Combined Summary:
       
         make summary
         ./summary

2. Direct Compilation with nvcc:
   -----------------------
   Alternatively, compile each example manually using the nvcc compiler.

   - Simple 1D Vector Addition:

         nvcc -o simple_vector_addition simple_vector_addition.cu
         ./simple_vector_addition

   - 1D Vector Addition with Blocks:

         nvcc -o vector_addition_blocks vector_addition_blocks.cu
         ./vector_addition_blocks

   - 2D Matrix Addition:

         nvcc -o matrix_addition matrix_addition.cu
         ./matrix_addition

   - Combined Summary:

         nvcc -o summary summary.cu
         ./summary

-----------------------------------------------------------------------
CODE INSIGHTS
-----------------------------------------------------------------------
- MEMORY MANAGEMENT:
  Each example demonstrates efficient memory allocation and deallocation on both the host (CPU)
  and the device (GPU), along with proper data transfers between them.

- KERNEL LAUNCH PARAMETERS:
  Learn how to configure the number of threads per block and blocks per grid. Understanding these
  parameters is essential for optimizing performance on the GPU.

- ERROR HANDLING:
  While the examples focus on fundamental operations, it is good practice to integrate robust error
  checking after CUDA API calls for enhanced reliability.

- PERFORMANCE OPTIMIZATION:
  Experiment with different block and grid sizes in the block-based and matrix addition examples to
  better understand the nuances of parallel execution and performance tuning.

-----------------------------------------------------------------------
FURTHER IMPROVEMENTS
-----------------------------------------------------------------------
- SHARED MEMORY:
  Explore the use of shared memory to minimize global memory access latency and further optimize performance.

- ADVANCED EXAMPLES:
  Future iterations might include more sophisticated CUDA applications such as matrix multiplication,
  parallel reduction, and other advanced algorithms.

- ENHANCED ERROR HANDLING:
  Adding comprehensive error checks after every CUDA API call can help in debugging and ensuring the
  stability of your programs.

-----------------------------------------------------------------------
CONTRIBUTING
-----------------------------------------------------------------------
Contributions are highly welcome! If you have ideas for improvements, new examples, or optimizations,
please feel free to fork the repository and submit a pull request. For any major changes, opening an
issue first is appreciated to discuss the modifications.

-----------------------------------------------------------------------
CONTACT
-----------------------------------------------------------------------
For any questions, suggestions, or feedback, you can reach out via:

    Email: anjuljangir@gmail.com
    GitHub: anjul1008 (https://github.com/anjul1008)

-----------------------------------------------------------------------
Happy coding and enjoy your journey into CUDA programming!
-----------------------------------------------------------------------

