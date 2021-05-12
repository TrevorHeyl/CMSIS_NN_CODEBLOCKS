# CMSIS_NN_CODEBLOCKS
A CMSIS-NN Codeblocks shell project 

This is a shell project that allows one to evaluate the CMSIS-NN library on a windows PC using Codeblocks. It may also work in Linux although I have not tried it.
The CMSIS-NN library includes all source.  This shell project uses the CIFAR-10 exmaple to compile and test the project.
this project was tested with the MINGW compiler toolchain

'''NOTE:'''
The CMSIS-NN source isnot included in this project git.  You need to download that from https://github.com/ARM-software/CMSIS_5 as a zip file and copy the content of the CMSIS folder to your local CMSIS folder once you have cloned this porject

If you want to create a CodeBlocks project yourself from scratch, follow these steps

* Get the CMSIS-NN source from https://github.com/ARM-software/CMSIS_5 as a zip file
* Extract the file , we want only the CMSIS folder and its contents (including all subdirectories)
* Create a new CodeBLocks Console application - specify a C rproject
* Copy the CMSIS folde rinto the root of this project
* Change the project build options -> Search paths, add :
** CMSIS\NN\include
** CMSIS\Core\include
** CMSIS\DSP\Include ( for ARM stuff)
** CMSIS\NN\Examples\ARM\arm_nn_examples\cifar10 ( for the example code)
* Add all the sources from CMSIS\NN\Source to the source tree
* Delete the defualt content from main.c
* Copy the contents of CMSIS\NN\Examples\ARM\arm_nn_examples\cifar10\arm_nnexamples_cifar10.cpp to the main.c file
* Build and Run

