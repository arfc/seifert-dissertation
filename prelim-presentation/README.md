# Slide Guidelines

## Purpose
Inform of the preliminary work conducted and propose the next steps.

## Central Message
The proposed work offers an improvement to existing modeling of MSRs by incorporating MSR physical phenomena into the generation of the delayed neutron precursor group parameters.

## Slide Structure
- Title
- Outline
- Introduction - something people care about, a problem, how it can be solved
    - Defining terms
        - What are DNPs?
        - What are DNP groups and parameters?
        - What are safety, security, and safeguards by design?
    - Motivation
        - Discuss how MSRs have effects that are not captured by existing parameters
    - Objectives
        - Objectives
- Background
    - DNPs
        - Define the process for calculating DNP group parameters
        - DNP groups were originally determined using macroscopic measurements
        - More detailed discussion of macro (pics, equations)
        - More detailed discussion of micro (pics, equations)
        - Discuss fitting procedures
    - MSR Phenomena
        - ANL paper (chemical removal rate and residence time for perfect mix (static) and no mix (current)) (example with 100\% removal and one for residence times)
    - Safety, security, and safeguards
        - Transients for safety and security
        - Safeguards diversion scenarios
- Methodology
    - MoSDeN package
    - General modeling approach (several slides) (uncertainty tracking and Monte Carlo approach)
    - 0D scaled model (several slides) (limitations)
    - 0D flow model (several slides) 
    - Transient modeling (Moltres, several slides)
    - Discuss ORNL, ANL, and INL work (motivation behind the problem)
- 0D Scaled Model Results
    - DNPs of interest
    - Sensitivity Studies
        - Long cycle time elements
        - Removal rate bool
        - Time node spacing
        - Number of time nodes
        - Total decay time
        - Time node density
        - Nuclear data uncertainties
    - Verification with the literature
- Proposed Work
    - 0D flow model with differing residual treatments
    - Varying data sources
    - Verification and Validation using MSRE
    - Improved group spectra (important for betaeff)
    - 3s transient simulations 
    - Gantt Chart


## Slide Notes
### What are delayed neutron precursors
- Emission probability contains probability of beta- decay and then probability of that decay emitting a delayed neutron.
- The number of atoms depends on fission yields, cross-sections, and decay chains.
### What are DNPs groups and parameters
- The delayed neutron yield contains the concentration and emission probability data
- There are hundreds of DNPs, but in reality 99% of delayed neutrons come from about 90 of them. 50% come from about 4 DNPs.
### 3SBD
- Critical for cost savings, timely deployment, and regulatory requirements
- Security, I am only looking at sabotage for this work.
### MSR not captured
### This work captures
### Two ways to create DNP groups
### Macroscopic
- Nobody has used this approach with an MSR
- Need shielding and distance between irradiation and measurement, but minimize time to capture short-lived DNPs
### Microscopic
- The concentrations come from depletion simulations or cumulative fission yields for a simulated irradiation
