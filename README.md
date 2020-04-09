# AFC Codebase

The AFC_Codebase is the sole repository for all AFC software (both flight code and analysis tools) for the Elroy Air *H*ybrid *T*ransition *C*apable *V*ehicle (HTCV).

The high-level objective of this repository architecture is to separate analysis tools (trim, linear analysis, control power analysis, etc) from all things flight-code related (generated code, the models that generated that code, the data the defines the tunable parameters, the tests that verify the completeness and validity of the code, etc)



## Set-up Instructions

After cloning the repository, navigate to the root level.
Run the script named initializeAfcEnvironment.m and wait until it completes (may take a few minutes). This script will do the following:

. Clear all workspace variables
. Close all open figures
. Close all open Simulink diagrams
. Set all necessary paths 
. Load most current vehicle data (aero, mass properties, etc)
. Trim the vehicle at nominal, hovering flight


## Repository Structure

- AFC_Analysis
  - 1.LinearAnalysis
  - 2.ControlPowerAnalysis
  - 3.Trim
- AFC_Code
  - 1.MassProperties
  - 2.Aero
  - 3.Propulsion
  - 4.Models
  - 5.Utilities
- initAfcEnvironment.m


