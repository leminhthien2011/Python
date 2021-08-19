# Python
1. Check the current python version

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

conda uninstall numpy 

c. Some times using conda doesnot work for a certain package due to conda not updated fast enough the need to do pip on the Anaconda prompt instead, so 

pip install numpy

pip uninstall numpy

d. For packages on github (on anaconda prompt)

pip install git+https://github.com/LouisRaynal/cost_based_selection.git

7. Check existing package on anaconda prompt with 

pip list 

Or using: conda list

8. Make sure we have pip command in our python 

py -m ensurepip --default-pip (on the cmd prompt)

9. Escape python on cmd prompt or Anaconda by

quit()

10. 



