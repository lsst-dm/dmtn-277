# The Monster: a southern reference catalog with synthetic ugrizy fluxes for the Vera C. Rubin Observatory

## Abstract

In order to facilitate bootstrap photometric calibrations of early Rubin Observatory data we have created the Monster.
This reference catalog uses a ranked order set of other reference catalogs to generate synthetic ugrizy fluxes that can be used calibrate images processed with the LSST science pipelines.

All code used to create the monster can be found in [lsst-dm/the_monster](https://github.com/lsst-dm/the_monster) on GitHub. 



## Simulated monster for Ops Rehearsal 3

For the operations rehearsal 3, using simulated ComCam data, a simulated reference catalog was created ([DM-42510](https://rubinobs.atlassian.net/browse/DM-42510)). This catalog is intended to act as a photometric and astrometric reference catalog for the simulated data, and it does not include proper motions. It does include positions and _gri_-band fluxes with realistic errors. 

The monster reference catalog is expected to be used for early calibrations and so, for this data, we used the properties of the monster to in a high-Galactic latitude region to create the simulated reference dataset. Briefly: 
- The limiting magnitude is roughly `r < 21` over the `g-i` color range of `0.5 < g-i < 3`
- Coordinate errors come from _Gaia_ DR3 and become non-linear at the faint limit (see Figure 1).

:::{figure} ./_images/coordRAError.png
:name: coordRAError
:target: ../_images/coordRAError.png

Fig 1: RA errors (in radians) as a function of r-band magnitude for the high galactic latitude sample of `the_monster`. The red line shows the spline fit used to assign errors to the simulated refcat. 
:::

- Magnitude errors come mainly from DES data in this region and synthetic Gaia XP photometry at the bright end. 
Figure 2 demonstrates g-band errors as a function of magnitude. 

:::{figure} ./_images/gmagError.png
:name: gmagRAError
:target: ../_images/gmagError.png

Fig 2: g-band magnitude errors as a function of magnitude for the high galactic lattitude sample of `the_monster`. The red line shows the spline fit used to assign errors to the simulated refcat. 
:::

This reference catalog can be accessed in the repo:

> `repo = /repo/ops-rehearsal-3-prep` 

with the collection 

> `collection = refcats/DM-42510`. 

For more details/plots see [DM-42510](https://rubinobs.atlassian.net/browse/DM-42510).


% Make in-text citations with: :cite:`bibkey`.

% Uncomment to use citations

% .. rubric:: References

%

% .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib

% :style: lsst_aa
