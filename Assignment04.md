Due: 23 November 2020

Please make sure your homework has your name (both Chinese and pinyin). You are free to work with others in the class, but everyone should submit their own assignment. You can submit your assignment as a Jupyter notebook, a PDF file, or a combination of both. *For all plots, please clearly label the axes and provide a legend to describe all lines and points. Please also include a figure caption for each plot.*


1. Galaxies do not have arbitrarily large or small luminosities. How they are distributed in luminosity tells us about their formation and evolution. The galaxy luminosity function tells us the number of galaxies that exist at a given luminosity per unit volume. *In this exercise, you will derive for yourself the galaxy r'-band luminosity function from SDSS data*. I recommend you follow these steps:

a. Use the Sloan Digital Sky Survey Data Release 16 (SDSS DR16) to obtain a large (i.e., representative) sample of galaxies with measured redshifts. The SDSS data is an excellent source for this exercise because it has spectroscopy of millions of galaxies. You will not need to use millions, but I suggest that you obtain a sample of at least many thousands. You should start with the [SDSS DR16 Spectroscopic Query Form](http://skyserver.sdss.org/dr16/en/tools/search/SQS.aspx). When searching for galaxies, I suggest the following search constraints:

* Limit number of output rows: The default is 50, and this is good for checking whether the output you are getting makes sense. Once you want to download the full sample, enter '0' to get everything.
* Output format: I would choose HTML at first, just to see what it looks like, but when you want to download the data to work with, I would suggest csv or FITS, or whatever other format you are more comfortable with.
* Parameters to return: Select 'typical' for both spectroscopy. For photometry, select 'typical' and 'grModelColor'. You can select these both by using 'Ctrl-click'. These will give you basic parameters that you will need (redshift, r-band magnitude, g-r color, etc.)
* Position constraints: Pick a rectangular region that gives you the maximum area (10 square degrees). This probably will not give you enough galaxies, so you may need to do this several times in different regions. It doesn't matter too much which regions you pick, as long as they are in the survey area. 
* Spectroscopy constraints: Make sure 'no warnings' is checked, and that he classification is 'GALAXY'
* Target flags (PRIMTARGET): Select 'GALAXY'. This ensures that all objects returned were targeted as galaxies.
* For everything else, you can leave the default values

Plot 1: What is the apparent r' magnitude distribution of your sample? The SDSS spectroscopic magnitude limit for the main galaxy sample was r'=17.7 mag. Do you see this feature in the data?
Plot 2: What is the redshift (z) distribution of the sample? What is the median redshift of SDSS galaxies?

b. To determine the galaxy luminosity function, you will need to convert from 

Read [Larson & Tinsley 1978](https://ui.adsabs.harvard.edu/abs/1978ApJ...219...46L). Beatrice Tinsley was a pioneer in the study of galaxies and their stellar populations. In this important paper, she and Richard Larson showed how we can use stellar population synthesis models to derive recent star formation histories of "peculiar" galaxies using their UBV colors. Please read the paper and answer the following questions.
