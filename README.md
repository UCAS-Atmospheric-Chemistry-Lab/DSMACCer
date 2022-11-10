Overview of DSMACCer
==============================================================

The Dynamically Simple Model for Atmospheric Chemical Complexity in reactors (DSMACCer) is modified from the DSMACC original version and is designed to simulate the atmospheric chemistry in both chamber reactor and flow reactor. The original source code of DSMACC box model is avaliable from [barronh/DSMACC](https://github.com/barronh/DSMACC) and has been integrated into the Geos-Chem global atmospheric model as chemical transport submodel. The DSMACC box model was modified to simulate the chamber data from the University of Florida UF-APHOR outdoor chamber. The current version of DSMACCr is designed to simualte the data from flowtube and chamber.

Reference:
1. Development of DSMACC: Emmerson, KM; Evans, MJ (2009) Comparison of tropospheric gas-phase chemistry schemes for use within global models, ATMOS CHEM PHYS, 9(5), pp1831-1845 doi: 10.5194/acp-9-1831-2009 .
2. Applying DSMACC to UF chamber study1: Yu, Zechen, and Myoseon Jang. "Atmospheric Processes of Aromatic Hydrocarbons in the Presence of Mineral Dust Particles in an Urban Environment." ACS Earth and Space Chemistry 3.11 (2019): 2404-2414.
3. Applying DSMACC to chamber study 2: Yu et al., "Simulation of Monoterpene SOA Formation by Multiphase Reactions Using Explicit Mechanisms." ACS Earth and Space Chemistry 5.6(2021): 1455-1467.

Contents
================================================================

1. [Install DSMACCr and the necessary environments](#1-Install-DSMACCr)
8. [Q&A](#8-Questions-and-answers)

## 1. Install DSMACCr

This describes the necessary steps to run the DSMACCr model in a lunix environment.

1. The necessary environmental packages: make sed byacc flex bison gfortran-7 vim csh
2. add the following path to the env:
```
export DSMACCr=/path-to-the-DSMACCr-directory/
export KPP_HOME=$DSMACCr/kpp
export PATH=$PATH:$KPP_HOME/bin
```
3. The fortran compiler used for DSMACCr is gcc-7 and gfortran-7, which should be preinstalled
4. Compile "KPP" PreProcessor
```
cd $KPP_HOME
make distclean
make
```

## 8. Questions and answers

1. cannot syncronize with github in Lunix server.
Answer: Check the global proxy, cancel the setup of global proxy for github.
```
git config --global --unset http.proxy
git config --global --unset http.proxy
```
