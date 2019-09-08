Due: 23 October 2018

Please make sure your homework has your name (both Chinese and pinyin). You are free to work with others in the class, but everyone should submit their own assignment. You should submit your assignment as a Jupyter notebook, with PDF attachments if necessary. You may work in groups of 3 or fewer people.

The spectral energy distributions (SEDs) of galaxies tell us about what they are made of, and how they evolved. One of the main constituents of galaxies that we can see is stars. In this assignment, we will explore our theoretical and empirical knowledge of stars and stellar evolution with the goal of having a better understanding of "stellar populations" in the next assignment.

1) The **initial mass function (IMF)** tells us about the number of stars formed as a function of their mass. Over time, the mass function will evolve, as more massive stars leave the main sequence and reach their end state (black hole, neutron star, white dwarf). What are the masses of stars in Solar neighborhood? The **IMF** describes the relative proportion of the masses of stars at the time that they are formed, and is a fundamental piece of input into galaxy stellar populations studies. [Salpeter (1955)](https://ui.adsabs.harvard.edu/abs/1955ApJ...121..161S) performed one of the earliest measurements of the shape of the IMF. Today, of course, we have much better data. Read Salpeter's paper, and repeat his study using The Hipparcos catalog. Make the same assumptions he did about star formation rate of the Galaxy being constant (which is not a good assumption, but okay for this exercise). When doing this exercise, feel free to make __reasonable assumptions__ that simplify the problem as long as you explicitly describe these assumptions.
   a) Determine the luminosity function (Equation 1 of Salpeter 1955) of stars. The distance out to which you select stars should depend on the luminosity and scarcity of the stars. In each luminosity bin, you should go far enough to get enough stars, and be sure to divide by the volume sampled.
   b) Convert your luminosity function into a "present-day mass function" using known mass-to-light ratios of stars as a function of temperature/color.
   c) Under the assumption of a constant star formation rate, correct your measured luminosity function to an initial mass function.

Use links:
* Padova [isochrones](http://stev.oapd.inaf.it/cgi-bin/cmd) and [evolutionary tracks](https://people.sissa.it/~sbressan/parsec.html)
* [Hipparcos Catalog](http://cdsarc.u-strasbg.fr/viz-bin/Cat?I/239)
