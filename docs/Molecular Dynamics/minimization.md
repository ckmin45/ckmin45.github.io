---
layout: default
title: Minimization
parent: Molecular Dynamics
nav_order: 2
---

System minimization is often the first step in a molecular dynamics simulation. The goal of the minimization step is to 'minimize' the number of inappropriate contacts and distances that are part of the system. The previous step of adding hydrogens and solvating the system involved introducing potentially unfavorable or physically unfeasable clashes within the system. Minimization is usually a multi-step procedure where restraints, i.e. forces applied to stabilize atomistic positions, are applied and slowly reduced to achieve a lower energy state. In Amber, we typically apply a Cartesian positional restraint given by the equation $\E_{\text{restraint}} = k(r - r_{\text{eq}})^2 \$

The following is a sample input file for minimization: 

```
Minimization step 1 (setup)
 &cntrl
  imin=1,
  ntx=1,
  irest=0,
  ntmin=1,
  maxcyc=10000,
  ncyc=5000,
  ntb=1,
  ntf=1,
  ntpr=1000,
  cut=10.0,
  nsnb=10,
  ntr=1,
  restraintmask=":1-261",
  restraint_wt=50.0,
 &end
```

The &cntrl section is a namelist in Amber used to denote the settings and parameters used for the simulation and the &end keyword signifies the end of the section. 




