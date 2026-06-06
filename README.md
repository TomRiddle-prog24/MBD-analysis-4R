# MBD-analysis-4R
The project showcases a MBD (Multibody Dynamics) solver for a 4R mechanism using Python. 
# Introduction 
The project is built using the **Kane's extension to the Newton-Euler Equations**. The dynamics and Kinematics formalism is made using the Kane's Equations of Motion combined with D-'Alembert's Principles. Further more, the DAE (Differential Algebraic Equations) formed has been evaluated using a combination of Scipy's ```fsolve``` and Scipy's ```solve_ivp``` using **Runge Kutta (RK4/5)** methods in an attempt to solve the **Initial Value Problem (IVP)** presented by the Kinematics and Dynamics Formalism. 

Additionally for the chosen link lengths, the solver solves the equations and performs the simulation for a **Grashof 4R Chain** specifically for a **Crank-Rocker** mechanism. 
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
# Modelling 
The model presents a model of 2 masses suspended to the two non-fixed revolutes of the 4R Mechanism. The links are modelled to be massless. The links are made sure such that, the Grashof Criterion is fullfilled i.e: 
$$ s+L \leq p+q $$
Here the angular velocity of the crank is *not constant* and will change w.r.t time. 
