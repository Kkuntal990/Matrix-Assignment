#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Wed Feb 13 22:56:35 2019

@author: kuntal
"""

import matplotlib.pyplot as plt
import pylab, math
import numpy as np
xmin = -30
xmax = 30
dx = 0.01


#putting the point given in question in the equation of tangent






p_given = np.array([[8],[3*math.sqrt(3)]])
V  = np.array([[9,0],[0,-16]])

normal_T  = np.matmul(p_given.T,V)
normal = normal_T.reshape((-1,1))
m  = normal[1]/normal[0]





def dir_vec(AB):
    return np.matmul(AB, dvec)


def norm_vec(AB):
    return np.matmul(omat, AB)



dvec = np.array([-1, -1])

omat = np.array([[0, 1], [-1, 0]])


NT = norm_vec(normal)
print(NT)
const = np.matmul(NT.T,p_given)
sts = str(const[0])
sts = sts[1:len(sts) -1]
print("The equation of the normal is: nT.X =", sts)



#plotting hyperbola and and normal at the given point

xlist = [float(x) for x in range(xmin,xmax)]
l1 = [float((m)*x + 25/(math.sqrt(3))) for x in range(xmin,xmax)]
y1list = [float(3*math.sqrt(1 + (x**2)/16)) for x in range(xmin,xmax)]
y2list = [float(-3*math.sqrt(1 + (x**2)/16)) for x in range(xmin,xmax)]


ax = plt.gca()
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))
plt.plot(p_given[0],p_given[1],'o')
plt.text(p_given[0]*(1-0.4),p_given[1]*(1+0.7),'P')
plt.grid(True)
plt.axis('equal')

pylab.plot(xlist,y1list)
pylab.plot(xlist,y2list)
pylab.plot(xlist,l1)
pylab.savefig('plot123.png')
