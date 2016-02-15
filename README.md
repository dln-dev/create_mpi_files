# create_mpi_files
Creates specified number of mpi directive files necessary for parallel execution of the feap FE² implementation.

This simple bash script takes an integer n and a filename file and creates $n copies of files named $file with an extension counting from 1 up to $n. Leading zeros are added to the extension in order to have equal filename size. The files are prefilled with feap directives, which include solve_mpi among other things.

Intended use is for the feap FE² implementation, which needs a number of input files equal to the number of processors to be used to solve the FE² problem with equal file name sizes. For this to work with more than 99 processors, the source code needs a few adjustments.
