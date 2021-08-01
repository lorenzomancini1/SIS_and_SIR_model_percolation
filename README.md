# Monte Carlo simulations of SIS and SIR model: two different percolation universality classes
Final project of  the "Physics of Complex Systems" course at University of Padua during 2020/2021

## Assignment and goal
The purpose of this project is to implement a simulation using a programming language (Python in my case) in order to simulate two epidemic models, namely the SIS (Contact Process) and the SIR, in order to find the critical point of the phase transition and the critical exponents of the corresponding percolation universality class.

## Simulation
Some functions exploit **Numba** in order to speed up the computation. Refer to the `presentation.pdf` for the theoretical details concerning the simulation and the analysis.
### Contact Processes (SIS)
The `Project_CP.ipynb` file contains the simulation of the 1-dimensional Contact Process.\
A linear lattice of size **N** is build with an arbitrary percentage of initial infected nodes and the **Monte Carlo** algorithm is performed (with periodic boundary condition) using a list in order to keep track of the positions of the infected nodes.\
The critical point is estimated with a quick and not rigorous method. Indeed, a more rigorous method would've required a lot of computational resources. For the critical exponents, some scaling relationships are used (see references in the presentation).
### SIR model 
The simulation of the 2-dimensional SIR model is contained in the `Project_SIR.ipynb` file. Again, a linear lattice of size **N** = **LxL** is built and considered as a square lattice of linear size **L**. The Monte Carlo algorithm is performed (with periodic boundary condition) using two lists in order to keep track of the Infected and Recovered nodes. The critical point is estimated in a similar way as in the previous case and the critical exponents are estimated exploiting scaling laws as well.

## Animation
The file `GIF_SIR.ipynb` contains the code used to create a simple animation of the SIR model: starting from a single infected node, it shows how the epidemic spreads near the critical point until the absorbing phase is reached. The code creates a folder with the images for the movie and the .gif file as well.
