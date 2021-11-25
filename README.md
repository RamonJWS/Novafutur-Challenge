# Data Scientist Technical Test (A) - Ramon Santiago

## Thought Process:
A N-N grid needs to be created, to make things easier I will initiate the matrix to be all zeros. This makes life easier when looping over the grid as I can +1 if the gird falls
within the delivery distance of the pizzeria. I can then loop through all the pizzerias and return the maximum value from the grid.

To find the possible delivery locations I looped through the grid and compared each cell to a pizzerias location and calculated the manhattan distance, if the distance is less than
or equal to the deliveries location then I added 1 to the cell. I could then repeat the process for all the pizzerias in the city, after loop through the pizzerias I can search the 
matrix for the maximum value and return this.


## How to use main():
This function returns the maximum number of pizzeria deliveries available to a single block in City Z

The main function takes in 3 arguments, 2 are required, the other is optional. The main function must be passed an integer N which will determine the size of the N-N matrix.
A list of all the pizzerias must be passed in second (M), e.g. [[3,3,2].[1,1,2]], this represents 2 pizzerias having locations (3,3) and (1,1) respectively,
and delivery range 2, again these must be integers. The third argument print_grid is by default set to False, if set to True the function will also return the final grid with each cell showing the number of deliveries availbale.

e.g. <br/>
main(5, [[3,3,2],[1,1,2]], print_grid=True) will return: <br/>
2 <br/>
[[0. 0. 1. 0. 0.] <br/>
 [0. 1. 1. 1. 0.] <br/>
 [2. 1. 1. 1. 1.] <br/> 
 [1. 2. 1. 1. 0.] <br/>
 [1. 1. 2. 0. 0.]]
 
 ## Complexity:
 I think that the complexity is relatively low. I have added docstrings to all the functions and commented on sections of code that could be more ambiguous.
 Perhaps writing the functions in just one function would improve readability. I also think that using the manhattan distance has retuced the complexity and runtime of
 the code, as I dont have to consider the effect of edges and corners on my algorithm. 
