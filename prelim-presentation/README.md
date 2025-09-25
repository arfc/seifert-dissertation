# Slide Guidelines

## Purpose
Inform of the preliminary work conducted and propose the next steps.

## Central Message
The proposed work offers an improvement to existing modeling of MSRs by incorporating MSR physical phenomena into the generation of the delayed neutron precursor group parameters.

## Slide Structure
- Title
- Outline
- Introduction - something people care about, a problem, how it can be solved
    - What are DNPs? (some of timeline)
    - What are DNP groups and parameters? (some of timeline) (brief mention of macro/micro approaches) (all are static)
    - Delayed neutron precursor group parameters are important for transient simulations (3 S's)
    - Importance of safety, security, and safeguards (use of transient sims)
    - Discuss how MSRs have effects that are not captured by existing parameters
     (pretend 100\% removal and other simple example)
    - Discuss MSR transient modeling usage of DNP group params
    - Objectives
- Background
    - DNPs
        - Timeline discussion (micro vs macroscopic equations)
        - More detailed discussion of macro (pics, equations)
        - More detailed discussion of micro (pics, equations)
    - MSR Phenomena
        - ANL paper (chemical removal rate and residence time for perfect mix (static) and no mix (current))
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
### What are delayed neutrons
- Emission probability contains probability of beta- decay and then probability of that decay emitting a delayed neutron.
- The number of atoms depends on fission yields, cross-sections, and decay chains.