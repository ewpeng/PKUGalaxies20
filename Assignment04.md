Due: 23 November 2020

Please make sure your homework has your name (both Chinese and pinyin). You are free to work with others in the class, but everyone should submit their own assignment. You can submit your assignment as a Jupyter notebook, a PDF file, or a combination of both. *For all plots, please clearly label the axes and provide a legend to describe all lines and points. Please also include a figure caption for each plot.*


Galaxies do not have arbitrarily large or small luminosities. How they are distributed in luminosity tells us about their formation and evolution. The galaxy luminosity function tells us the number of galaxies that exist at a given luminosity per unit volume. *In this exercise, you will derive for yourself the galaxy r'-band luminosity function from SDSS data*. I recommend you follow these steps:

1. Obtaining your galaxy sample. Use the Sloan Digital Sky Survey Data Release 16 (SDSS DR16) to obtain a large (i.e., representative) sample of galaxies with measured redshifts. The SDSS data is an excellent source for this exercise because it has spectroscopy of millions of galaxies. You will not need to use millions, but I suggest that you obtain a sample of at least many thousands. You should start with the [SDSS DR16 Spectroscopic Query Form](http://skyserver.sdss.org/dr16/en/tools/search/SQS.aspx). When searching for galaxies, I suggest the following search constraints:

* Limit number of output rows: The default is 50, and this is good for checking whether the output you are getting makes sense. Once you want to download the full sample, enter '0' to get everything.
* Output format: I would choose HTML at first, just to see what it looks like, but when you want to download the data to work with, I would suggest csv or FITS, or whatever other format you are more comfortable with.
* Parameters to return: Select 'typical' for both spectroscopy. For photometry, select 'typical', 'ugModelColor', and 'grModelColor'. You can select these both by using 'Ctrl-click'. These will give you basic parameters that you will need (redshift, r-band magnitude, u-g color, g-r color, etc.)
* Position constraints: Pick a rectangular region that gives you the maximum area (10 square degrees). This probably will not give you enough galaxies, so you may need to do this several times in different regions. It doesn't matter too much which regions you pick, as long as they are in the survey area. It would be better if they were contiguous.
* Spectroscopy constraints: Make sure 'no warnings' is checked, and that he classification is 'GALAXY'
* Target flags (PRIMTARGET): Select 'GALAXY'. This ensures that all objects returned were targeted as galaxies.
* For everything else, you can leave the default values

Plot 1: What is the apparent r' magnitude distribution of your sample? The SDSS spectroscopic magnitude limit for the main galaxy sample was r'=17.7 mag. Do you see this feature in the data?
Plot 2: What is the redshift (z) distribution of the sample? What is the median redshift of SDSS galaxies?

2. Luminosity distances. To determine the galaxy luminosity function, you will need to convert from apparent magnitude to absolute magnitude using the redshift. (Let's ignore extinction for now, as it should be small at high Galactic latitude). To do this you need to use the *luminosity distance* for a standard cosmology (H_0 = 70, Omega_m = 0.3, Omega_lambda = 0.7). This can be calculated using the [Astropy cosmology package](https://docs.astropy.org/en/stable/cosmology/index.html). Please follow the first example, where they set the cosmology, and then use cosmo.luminosity_distance(z) to get the luminosity distance (in Mpc) at redshift z=4. You will need to do this for your entire sample of galaxies. Once you have the luminosity distance, you can calculate the absolute r' magnitude using the distance modulus formula: m-M = 5log10(d)+25 when d is in Mpc.

Plot 3: What is the absolute r' magnitude distribution of your sample? Plot a histogram with reasonable bin sizes (0.1 to 0.5 mag, depending on your sample size)

3. Vmax correction. More luminous galaxies can be seen at a larger distance. To make the luminosity function, you now need to correct each bin for the maximum volume within which SDSS can see these galaxies. A simple way to do this: for each bin in absolute r' mag (M_r'), find the maximum distance (d_max) for an object in that bin. The maximum volume within which you are observing these galaxies is the just 4/3*PI*d_max^3. 

Plot 4: Show the maximum distance (d_max in Mpc) as a function of M_r' to show how the distance probed by the survey changes with luminosity.

4. The r'-band galaxy luminosity function. For each bin in M_r', you can now calculate the galaxy number density (number of galaxies per Mpc^3) by dividing the number of galaxies by the maximum volume calculated in Question 3. 

Plot 5: Show the number of galaxies per Mpc^3 as a function of M_r'. Plot the y-axis as log(number/Mpc^3). You may want to ignore fainter bins (fainter than M_r'=-16) where there are very few galaxies. These are likely affected by severe incompleteness. This is the r'-band galaxy luminosity fuction. 

5. The galaxy luminosity function (LF) should be characterized by a steep cutoff at bright magnitudes, and a flatter slope at fainter magnitudes. We typically fit this with a Schechter (1976) function. Fit a Schechter function to your galaxy LF and determine the values of M*, the characteristic "knee" of the LF, and the faint-end power law slope.

Plot 6: Show your luminosity function with your best-fit Schechter function overplotted. 

6. Galaxies can be roughly separated into 'red' (quenched) galaxies and 'blue' (star-forming) galaxies.

Plot 7: Show a histogram of your galaxy sample in u'-r' color (which is just ugModelColor+grModelColor because u'-g'+g'-r' = u'-r'). You may see a somewhat bimodal distribution. Around what color would you divide these two populations? Draw a vertical line there.

7. Star-forming and quenched galaxies have different luminosity functions.

Plot 8: In a single plot, show the luminosity functions for both the red and blue galaxy samples from the previous plot. Derive the LFs in the same way as you did for the full sample. Overplot your best-fit Schechter functions for each subsample and show the fitted parameters. What is the difference between the LFs of the two types of galaxies? 

8. Redshift-spatial distributions of red and blue galaxies.

Plots 9 and 10: Plot a "pie" plot (polar) with redhsift (z) along the radial axis, and RA (or Dec, whichever is wider) along the angle. You should see some large-scale structure in the galaxy distribution. Do this for the red and blue galaxies separately. Do you see any difference in how the red and blue galaxies are distributed? In their clustering properties?
