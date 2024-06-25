---
layout: default
title: Minimization
parent: Molecular Dynamics
nav_order: 2
---

System minimization is often the first step in a molecular dynamics simulation. The goal of the minimization step is to 'minimize' the number of inappropriate contacts and distances that are part of the system. The previous step of adding hydrogens and solvating the system involved introducing potentially unfavorable or physically unfeasable clashes within the system. Minimization is usually a multi-step procedure where restraints, i.e. forces applied to stabilize atomistic positions, are applied and slowly reduced to achieve a lower energy state. 

In Amber, we typically apply a Cartesian positional restraint given by the equation \( E_{\text{restraint}} = k(r - r_{\text{eq}})^2 \)

