# game-of-life-parallel
### Description
This is a parallel version of John Conway's Game of Life written in OpenMP, a parallel programming language. The simulation revolves around a 2-dimensional matrix divided into cells, which are either dead or alive (dead = 0, alive = 1). The state of the cells in the next iteration is a function of its neighbors in the current iteration (the 8 cells vertically, horizontally, or diagonally adjacent to that cell) following 4 rules:
1. An alive cell with fewer than two alive neighbors dies in the next generation. 
2. An alive cell with more than three alive neighbors also dies in the next generation. 
3. An alive cell with exactly two or three alive neighbors stays alive in the next generation. 
4. A dead cell with exactly three alive neighbors becomes alive in the next generation. 

The 2-dimensional world is restricted to an NxN matrix.

ex.
Generation 0:
0 0 0 0 0 
0 1 1 0 0 
0 0 1 0 0 
0 0 1 0 0 
0 0 0 0 0

Generation 1:
0 0 0 0 0 
0 1 1 0 0 
0 0 1 1 0 
0 0 0 0 0 
0 0 0 0 0



### Input:
The program requires 4 arguments in the following order:
1. The number of generations
2. The dimension N of the NxN matrix
3. The number of threads
4. The filename of the text file that contains the initial matrix. The file should a NxN matrix of integers. Cells at each row are separated by a space. An alive cell is represented by a 1, while a dead one is presented by a 0. 

ex.
0 0 0 0 0 
0 1 1 0 0 
0 0 1 0 0 
0 0 1 0 0 
0 0 0 0 0


### Output:
The program will output the amount of time spent in parallel (in seconds) to the console.

It will also generate the final iteration of the NxN matrix and write it to an output text file.



