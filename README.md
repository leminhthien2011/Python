# PYTHON
# 15. Sort order of a vector
x = np.array([1,3,2,4])
idx_sort = np.argsort(x) #get the order of elements in x, smallest to largest

idx_sort
Out[16]: array([0, 2, 1, 3], dtype=int64)

x[idx_sort] #rearrange x to make elements from smallest to largest
Out[17]: array([1, 2, 3, 4])

# 14. Flatten a matrix to one vector of elementwise

M = [[1,2],[3,4],[5,6]]
np.array(M).flatten()

# 13. Define our own summary function

def mysummaryfunction(x):
    val1 = np.mean(x)
    val2 = np.std(x)
    val3 = np.median(x)
    val4 = np.min(x)
    val5 = np.max(x)
    val6 = np.sum(x)
    val7 = len(x)
    mydict = {"mean":val1, "std": val2, "median": val3, "min": val4,"max":val5 ,"sum": val6,
              "length":val7}
    return mydict

# 12. Fill diagonal with 0, Get the upper/lower triangular matrix, Show nonzero location (networkx version 2, 3)


import numpy as np

G = nx.complete_graph(4)

A = nx.to_numpy_array(G) #extract matrix A from G

np.fill_diagonal(A, 0) # Equivalent to remove self-loops 

A1 = np.tril(A,k=0) # Get lower triangular, use np.triu(A,k=0) for upper triangular

A2 = np.transpose(np.nonzero(A1)) #show all non zero position of A1

# 11. Convert network to matrix and vice versa (networkx version 2, 3)

import networkx as nx
import numpy as np

G = nx.complete_graph(4)
nx.draw(G, with_labels =1) #draw G to check
A = nx.to_numpy_array(G) #extract matrix A from G
G1 = nx.from_numpy_array(A)  #make graph G1 from matrix A
nx.draw(G1, with_labels =1) #draw G1 to check


# 0. Remove self-loop edges (networkx version 2, 3)

G.remove_edges_from(nx.selfloop_edges(G))



# 01.Check the current python version

a. Check directly on the editor:

import sys

print (sys.version)

b. Check on Anaconda prompt

python --version

c. Check on cmd prompt

py --version

# 02. Comment out
a. Comment out multiple lines

choose all the lines, then ctr+4. 

b. Uncomment multiple lines

choose all the lines, then ctrl+1



# 03. Indent multiple lines:

Ctrl ]

Dedent multiple lines:

Ctrl [



# 04. Install/Uninstall a python package (python module) 

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

# 05. Check existing package on anaconda prompt with 

pip list 

Or using: conda list

# 06. Make sure we have pip command in our python 

py -m ensurepip --default-pip (on the cmd prompt)

# 07. Escape python on cmd prompt or Anaconda by

quit()

# 08. Check all packages available in conda by:

conda show

# 09. Update a package by:

conda update package


# 010.Look at inside a function and learn how it was created by the inspect module.

import inspect

inspect.getsourcelines(EoN.get_infected_nodes) # Look at the function EoN.get_infected_nodes line by line

help(EoN): Learn the most general information of EoN

help(EoN.get_infected_nodes) : Learn how to use the get_infected_nodes function of EoN

dir(EoN): Know all functions available in EoN module

# 011. Column sum or row sum of a matrix

Columnsum of A: A.sum(axis=0,dtype='float')

Rowsum of A: A.sum(axis=1,dtype='float')

# 012. Check number of nodes in networkx:

G.number_of_nodes()




# 013. Check degree distribution and count 

from collections import Counter

dict(G.degree()) : Give the dictionary for each node and its corresponding degree

Counter(dict(G.degree()).values()): Make all degree as a frequency sequence

# 014. Delete an index in an array A with numpy:

np.delete(A, index)

# 015. Maximum, Minimum, Mean of a matrix

A.max() # max elements wise

A.max(0) # max each column

A.max(1) # max each row

A.min(1) # min each row

A.mean(1) # mean each row

# 016. Extract the ajacency matrix of a network:

A1 = nx.adjacency_matrix(G, nodelist=None, dtype=None, weight='weight')

Ajacency_mat = A1.todense()

# 017. Extract numbers from a list:

float(mylist[i]) # converge (i+1)-th element of mylist to a float number

# 018. Print out all neighbors of a node:

list(G.neighbors(1)) #print out neigbors of node 1 in the G graph

# 019. Make a line graph of 20 nodes

L =nx.path_graph(20)

nx.draw(L, with_labels=True)

# 020. Take difference lag 1 of a vector A

np.diff(A, n=1)

# 021. Descriptive statistics of a vector A

from scipy import stats

stats.describe(A)


# 022. Check type of an object

nrepeat =100

type(nrepeat)


# 023. Save figure at a given folder

After done with the plot, say here we save figure with some variables N, e.g. N = 7

N=7

plot_dir = "C:\\Users\\thl902\\Desktop\\HIV\\1.Workingprogress\\Sep28\\"

plot_name = "myplot" + str(N) + ".pdf"

plt.savefig(plot_dir + plot_name)

# 024. Check current directory and change to another

import os

os.getcwd()

os.chdir('C:\\Users\\thl902\\Desktop\\CONET_Revision')

# 025. Working with nan values and index of a vector

Replace nan values of a vector A by 0s:

np.nan_to_num(A, copy=True, nan=0.0)

Remove all the nan values of a vector A:

A[~np.isnan(A)]

Return all the nan indecies of a vector A:

np.argwhere(np.isnan(A))


Keep components greater than a threshold, say 1, of vector A

A = A[A>1]

# 026. Make plots title with mutiple Arguments, say N, nrepeat, and num_time_steps

plt.title('Complete graph of N=%i nodes - rep=%i - steps=%i' %( N,nrepeat,num_time_steps))

# 027. Append number to a list with loop, say from an empty loop to [0,1,2,3,4]

A = []

for i in range(5):
    A.append(i)

Return: a list as [0,1,2,3,4]

# 028. Read txt file
#use np and skip the first row

import numpy as np

with open('trafficdatatop2020.txt') as f:
    lines = (line for line in f if not line.startswith('#'))
    mydata = np.loadtxt(lines, delimiter=',', skiprows=1)
    
#use pandas

import pandas as pd

mydata = pd.read_csv("trafficdatatop2020.txt", sep=" ")


    
# 029. Create an arrange of numbers

import numpy as np

np.arange(0, 4.5, 0.5) #outputs: 0,0.5,...,3.5,4


# 030. Make a name with mixed of letters, integer, and float of 2 decimals
N =100
p = .5
plt.title('Mean total infected for a ER graph of N=%i nodes, p=%.2f'% (N,p))

The title output then: Mean total infected for a ER graph of N= 100 nodes, p=.5

# 031. Check package version
import networkx as nx
print(nx.__version__)






