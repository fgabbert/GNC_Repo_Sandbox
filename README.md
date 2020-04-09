# AFC Codebase

The AFC_Codebase is the sole repository for all AFC software (both flight code and analysis tools) for the Elroy Air **H**ybrid **T**ransition **C**apable **V**ehicle (HTCV).

The high-level objective of this repository architecture is to separate analysis tools (trim, linear analysis, control power analysis, etc) from all things flight-code related (generated code, the models that generated that code, the data the defines the tunable parameters, the tests that verify the completeness and validity of the code, etc)



## Set-up Instructions

After cloning the repository, navigate to the root level.
Run the script named initializeAfcEnvironment.m and wait until it completes (may take a few minutes). This script will do the following:

- Clear all workspace variables
- Close all open figures
- Close all open Simulink diagrams
- Set all necessary paths 
- Load most current vehicle data (aero, mass properties, etc)
- Trim the vehicle at nominal, hovering flight


## Repository Structure


As previously stated, the main focus of the AFC_Codebase architecture is to separate **flight code** from **analysis tools**



- AFC_Analysis (Tools only! Nothing from this folder will be inside generated flight code)
  - 1.LinearAnalysis (All things related to linearization/linear analysis)
  - 2.ControlPowerAnalysis (Control Power Analysis scripts, models, etc)
  - 3.Trim (Trim routines and Trim Databases)
- AFC_Code (Flight Code! This contains all models that generate flight code, all of the data that is used to generate flight code parameters, and all of the unit tests/coding standard enforcement tools that ensure our code is safe)
  - 1.MassProperties (Vehicle geometry, mass, inertias, etc)
  - 2.Aero (Aerodynamic tables and reference geometry)
  - 3.Propulsion (Propulsion parameters such as motor transfer functions, etc)
  - 4.Models (ALL of the Reference Models that are autocoded into our beautiful autopilot)
  - 5.Utilities (Matlab and Simulink utilities including unit tests, styleguides, utility libraries (for things like divide-by-zero protection, etc))
- initAfcEnvironment.m


