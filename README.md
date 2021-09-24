# Python
#1.Check the current python version

a. Check directly on the editor:

import sys

print (sys.version)

b. Check on Anaconda prompt

python --version

c. Check on cmd prompt

py --version

2. 
a. Comment out multiple lines

choose all the lines, then ctr+4. 

b. Uncomment multiple lines

choose all the lines, then ctrl+1

3. Check type of an object

nrepeat =100

type(nrepeat)

4. Indent multiple lines:

Ctrl ]

Dedent multiple lines:

Ctrl [

5. Descriptive statistics of vector a

scipy.stats.describe(a)

6. Install/Uninstall a python package (python module) 

a. Install numpy with cmd prompt: 

py -3.9. -m pip install numpy

Uninstall

py -3.9 -m pip uninstall numpy

b. With anaconda prompt:

conda install numpy 

Install in a certain environment by:

conda install --name myenv iopro

Remove a package by 

conda remove numpy 

c. Some times using conda doesnot work for a certain package due to conda not updated fast enough then we need to do pip on the Anaconda prompt instead, so 

pip install numpy

pip remove numpy

Or uninstall multiple packages by:

pip remove numpy pandas

Or uninstall a package in an environment by

conda remove -n myenv numpy

d. For packages on github (on anaconda prompt)

pip install git+https://github.com/LouisRaynal/cost_based_selection.git

7. Check existing package on anaconda prompt with 

pip list 

Or using: conda list

8. Make sure we have pip command in our python 

py -m ensurepip --default-pip (on the cmd prompt)

9. Escape python on cmd prompt or Anaconda by

quit()

10. Check all packages available in conda by:

conda show

11. Update a package by:

conda update package


12.Look at inside a function and learn how it was created by the inspect module.

import inspect

inspect.getsourcelines(EoN.get_infected_nodes) # Look at the function EoN.get_infected_nodes line by line

13. Column sum or row sum of a matrix

Columnsum of A: A.sum(axis=0,dtype='float')

Rowsum of A: A.sum(axis=1,dtype='float')

14. Check number of nodes in networkx:

G.number_of_nodes()

15. Learn information avaialble from a module by using:

help(EoN): Learn the most general information of EoN

help(EoN.get_infected_nodes) : Learn how to use the get_infected_nodes function of EoN

dir(EoN): Know all functions available in EoN module

16. Check degree distribution and count 

from collections import Counter

dict(G.degree()) : Give the dictionary for each node and its corresponding degree

Counter(dict(G.degree()).values()): Make all degree as a frequency sequence

17. Delete an index in an array A with numpy:

np.delete(A, index)

18. Maximum index of a matrix

A.max() # max elements wise

A.max(0) # max each column

A.max(1) # max each row

19. Extract the ajacency matrix of a network:

A1 = nx.adjacency_matrix(G, nodelist=None, dtype=None, weight='weight')

Ajacency_mat = A1.todense()

20. Extract numbers from a list:

float(mylist[i]) # converge (i+1)-th element of mylist to a float number

21. Print out all neighbors of a node:

list(G.neighbors(1)) #print out neigbors of node 1 in the G graph

22. Make a line graph of 20 nodes

L =nx.path_graph(20)

nx.draw(L, with_labels=True)

23. Take difference lag 1 of a vector A

np.diff(A, n=1)

24. Remove k-th element of a vector A

np.delete(A, k)



















