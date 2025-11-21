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
        - Discuss fitting procedures (could include stripping, lsq, half-life)
    - MSR Phenomena
        - ANL paper (chemical removal rate and residence time for perfect mix (static) and no mix (current)) (example with 100\% removal and one for residence times)
        - Define the scaled flux method
	- Discuss chemical removal
- Methodology
    - MoSDeN overview
        - MoSDeN package
        - Residual, least squares, uncertainty tracking
        - Explicit group solve form
    - 0D scaled model
        - 0D scaled model overview
        - Scaled flux and CFY
        - Limitations
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
    - Verification and Validation using MSRE (OpenMC sim for spectrum, cross sections, depletion)
    - Improved group spectra (important for betaeff)
    - Transient modeling (Moltres, several slides) (relate to 3s's) (diversion depletion simulations)
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
### Groupping
### Recirculation
- Explicit modeling can entail using time (irradiate for in-core, decay ex-core) or space (such as a 1D advection model). Some way of representing the different regions and having them happen at the correct time.
- The scaled flux method would be the same as a stationary irradiation.
- Scaled flux scales by fraction of time in the core
- The scaled flux method accurately captures concentrations that change linearly with the flux
- Explicitly capturing this will be more accurate, comparing with scaled flux could be interesting
### Reprocessing
### Mosden
### Least squares
### Residual
- The 2-norm is the square root of the sum of the squares, squaring it makes it faster to calculate and doesn't change the minimized solution
### Uncertainty
### MoSDeN group form
- The orange bit is new, the rest exists in the T,t form of the equation normally derived. The new bit represents the in-core and ex-core regions
### 0D scaled
### 0D scaled limitations
- DNPs have negligible cross sections so this should be okay
- Equilibrium means no pulse irradiation (challenging for data)
- Chemical removal misses intermediate elements, such as not capturing I removal for Xe conc
### Params
- Orange highlights show ~4 orders of magnitude larger chemical removal rates in the MSBR
### Yields
- Talk about what the yield represents
- Talk about how Br87 isn't here
- Talk about how 2/3rds of yield is from 6 DNPs
### Counts
- Different DNPs from yield
- Ge86 dominates early, but most delayed neutrons after saturation come from I137
- Talk about pulse vs saturation irradiation
### Long Cycle
### Chem bool
- 0.57\% difference, or 12 pcm, difference in the yield.
- This is expected to be higher with the 0D flow model.
### Time spacing
- The total delayed neutron yield does not change between linear and log
### Number of time nodes
- Computational cost roughly constant as number of time nodes varies (strange)
### Total decay time
### Time node density
- The time node density of the 1200 second decay time with 800 nodes is two time nodes for every three seconds of decay; the time node density of the 2400 second decay time with 1600 nodes is the same. If the \ac{DNP} group parameters primarily depend on the node density, then these two different sets of decay times and time nodes should give the same set of \ac{DNP} group parameters. Instead, the results remain approximately constant with varying node numbers, with the main difference arising from the total decay time. This indicates the total decay time sensitivity analysis does not need to account for varying time node density.
### Nuclear data
- PCC of 1.0 vs PCC of 0.19 (very strongly correlated vs weakly) (surprising there is any correlation)
### PCC magnitudes
- Ge86 is the bright yellow spot, some others can be seen around it
- Iodine and antimony dominate the upper area
- These nuclides have large PCCs because they either dominate a group (such as Br87), have large CFYs and emission probabilities, or a combination
### Scaled PCC
- Ge86 is expected (large values of PCC, and large uncertainties in dataset used)
- Discuss how Ge86 Pn in ENDFB71 is 5.2% without uncertainty, wheras IAEA uses 45+/-15%
- Overlap with the previous table given in blue (only 2 out of 10 nuclides)
- The non-overlapping DNPs have very large uncertainty even though the PCC values may not be as large
### Verify
- This is conducted for a stationary sample such that results can be compared with literature
### Verify 2
- Lead into proposed work
### 0D flow
### Validation
- The prompt method is beta_eff \approx 1 - k_p/k_{eff} (using two monte carlo sims, one with and one without delayed neutrons)
