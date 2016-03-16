Big Data in Finance final exam, Part B1, calculating PI using MPI
=================================================================

The MPI program has several bugs. These bugs can be in the C code,
the makefile, or the PBS job file. Your task is to find these bugs,
fix them, compile and run the program, then share your results.

In this file, write any thoughts or comments that might help
improve your grade.

A hint to help you on your way. Remember that make uses tabs to indent
the commands below targets.

And, remember, to use Git you must first load Git:

  module load git
  
These may also be useful commands:

  module list
  
  module avail

++++
In the makefile:
change the second line:
mpicc -o mpi mpi.cpp       shoule be     mpicc -o mpi mpi.c
because the mpi file name is wrong

  mpicc -o mpi mpi.cpp
should be
\t mpicc -o mpi mpi.cpp

  rm mpi
should be
\t rm mpi

In the mip.c:
if (myid = 0) {            should be         if (myid == 0) {



