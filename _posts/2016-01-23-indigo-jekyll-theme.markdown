---
title: "Fluid directed Rigid Ball using Deep Reinforcement Learning"
layout: post
date: 2019-01-10 15:10
tag: jekyll
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: "project1."
category: project
author: johndoe
externalLink: false
---

Course project from CIS563 (Physics based simulations) during my 1st semester at Penn. This is an interdisciplinary project at the intersection of simulations, computer graphics, and machine learning.

---

Languages: 
- C++
- Python
- Matlab

Libraries: 
- Gym by OpenAI
- Keras (backend: Tensorflow)
- Eigen (linear algebra in C++)
- Partio (data I/O)
- Stable-baselines

---

Two different modeling approaching were mixed to solve the problem at hand. The task was to balance a rigid ball in air using a jet of water, which is controlled by a neural network. The motion of ball is based on the classical laws of physics (deterministic approach), whereas the movement of the water jet is based on a probabilistic approach as the neural network learns to evaluate the best set of moves for a given state of the environment. 

I planned the project in various stages. 
- Physics Simulator: The motion of the ball and fluid is modeled using Newtons laws and Navier Stokes equations and these are numerically integrated to simulate this coupled motion. I followed a variational pressure framework approach desribed by Prof. Batty in his 2007 paper. I wrote this code in C++11 using a supporting library called Eigen for handling linear algebra operations. 
- C++ to Python: As most of the machine learning libraries are based on Python, I had to port the simulator (from C++) to Python. For this I used an interface compiler called SWIG (Simplified Wrapper and Interface Generator), which allowed to package the entire C++ code into a single shared library file that could be imported directly in Python. This provided a convenient way to simulate the fluid-ball motion in Python at an added advantage of fast computations as the backend was still in C++. 
- Gamify the Simulator: 

