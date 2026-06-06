# MBD-analysis-4R
The project showcases a MBD (Multibody Dynamics) solver for a 4R mechanism using Python. 
# Introduction 
The project is built using the **Kane's extension to the Newton-Euler Equations**. The dynamics and Kinematics formalism is made using the Kane's Equations of Motion combined with D-'Alembert's Principles. Further more, the DAE (Differential Algebraic Equations) formed has been evaluated using a combination of Scipy's ```fsolve``` and Scipy's ```solve_ivp``` using **Runge Kutta (RK4/5)** methods in an attempt to solve the **Initial Value Problem (IVP)** presented by the Kinematics and Dynamics Formalism. 
# Modules used 
1. For Symbolic Computations and Formalism- ```Sympy``` has been used.
2. For performing Numerical Calculations and translation of Symbolics to Numerics- ```numpy``` has been used.
3. For performing the computations using Numerical techniques- ```Scipy``` has been used.
4. For standard plotting and animation- ```matplotlib``` has been used.

# Required modules: 
Make sure you have imported the following modules and the set the defaults before running the simulation: 
``` python
import sympy as sm     
import sympy.physics.mechanics as me
import numpy as np 
import matplotlib.pyplot as plt
me.init_vprinting(use_latex='mathjax') 
import scipy.integrate as sp
import scipy.optimize as so
from matplotlib.animation import FuncAnimation          #For animation of the mechanism
from IPython.display import HTML
import matplotlib as ilt
ilt.rcParams['animation.embed_limit'] = 50.0          #For the animation to be fit the entire time steps for a memory of 50MB 
```
