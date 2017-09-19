Due: 9 October 2017

Please make sure your homework has your name (both Chinese and pinyin). You are free to work with others in the class, but everyone should submit their own assignment. You should submit your assignment as a Jupyter notebook, with PDF attachments if necessary. You may work in groups of 3 or fewer people.

The spectral energy distributions (SEDs) of galaxies tell us about what they are made of, and how they evolved. One of the main constituents of galaxies that we can see is stars. Understanding "stellar populations" (star clusters, galaxies) is an important extension of our knowledge of stellar evolution. In this assignment, we will explore how our theoretical and empirical knowledge of stars and stellar evolution can tell us something about galaxies.

0) Read Chapter 10 of Galaxy Formation & Evolution (GF&E). It covers the basics of stellar evolution, structure, and population synthesis.

1) Two resources we will use are **stellar libraries** and **stellar evolutionary models**. Together, we can perform "stellar population synthesis", and compare the results we get with observations.

**Stellar libraries** are collections of stellar spectra, taken in a homogeneous manner, that allow us to know what the SED of a star should be as a function of stellar parameters (effective temperature, gravity, metallicity, chemical abundance, etc). It is an empirical way of sampling the parameter space of stellar properties. The advantage of this method is that these are the SEDs of real stars, so we know they must exist. The main disadvantage is that the stars that we can include in our libraries (i.e., those in the Milky Way, near us) may not represent the full range of stellar parameters that exist in the Universe. The alternative is to use computer code that reproduces stellar atmospheres from first principles and known atomic transitions. While this technique allows the exploration of a large range of stellar parameters, the models can suffer from missing physics or unknown atomic and molecular transitions or oscillator strengths. For this assignment, we will use stellar libraries. Below are a few examples of commonly used spectral libraries.

* [Pickles Spectral Library](http://www.eso.org/sci/facilities/paranal/decommissioned/isaac/tools/lib.html)
* [ELODIE Spectral Library](http://www.obs.u-bordeaux1.fr/m2a/soubiran/elodie_library.html)
* [MILES Spectral Library](http://www.iac.es/proyecto/miles/)
* Make your own! You can also use the SDSS and other surveys to find calibrated spectra.

1a) Using the galaxies you identified in Assignment 1, find their spectra in the SDSS database and plot them.
1b) Plot flux calibrated spectra of stars from type O through M. Compare them to the spectra of galaxies from 1a. Which stars are similar to the galaxies? Do any galaxies match?
1c) See if you can add combinations of stars (in different ratios) to get a spectrum that approximates a "blue" galaxy and a "red" galaxy. Ignore emission lines, as they come from the interstellar medium, not the stars.
1d) What do your composite spectra tell us about the likely ages or metallicities of the galaxies? What do you estimate for the mass-to-light ratio?

2) **Simple stellar populations (SSP).** The simplest stellar population to synthesize is one that formed stars in a single burst (a delta function in time) and then have passively evolved (e.g., no further star formation).

The **initial mass function (IMF)** tells us about the number of stars formed as a function of their mass. Over time, the mass function will evolve, as more massive stars leave the main sequence and reach their end state (black hole, neutron star, white dwarf).

Using a stellar library and a Salpeter (1955) initial mass function for the stars, synthesize the expected color evolution (u-g, g-r) for a solar metallicity SSP. For simplicity, assume that stars do not have any post-main sequence phase. Once they leave the main sequence, they disappear.

3) **Stellar evolutionary models** aim to reproduce the evolution of a star's properties over time based on known physics. The simplest form of stellar population synthesis assumes little about the evolution of stars. Like we started in class, we can try to match a galaxy SED using weighted combinations of stars. This, however, leads to many degenerate (non-unique) solutions, and does not directly tell us about the star formation history of the galaxy. Knowing how stellar evolution proceeds allows us to put stronger constraints on the stellar content and star formation histories of galaxies.

* Padova [isochrones](http://stev.oapd.inaf.it/YZVAR/cgi-bin/form) and [evolutionary tracks](http://stev.oapd.inaf.it/YZVAR/)
* [Victoria-Regina models](http://www.cadc-ccda.hia-iha.nrc-cnrc.gc.ca/community/VictoriaReginaModels/)
* [Starburst99](http://www.stsci.edu/science/starburst99/docs/default.htm)

3a) An isochrone represents a snapshot in time (iso = same, chrone = time) of a single-age, single-metallicity stellar population. One can approximate the star formation history of a galaxy as a combination of single-age populations. Using evolutionary synthesis models, plot the evolution of (u-g) vs (g-r) color for isochrones ranging in age from 0.01-13 Gyr and -2.3<[Fe/H]<+0.3.

3b) Overplot the colors of the SDSS galaxies in the same color-color plot. What can we say about these galaxies' star formation histories?
