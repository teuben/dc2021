# Data Combination notes 

For lecture 10 (November 2, 2021) of https://github.com/anand0xff/FourierOpticsJHU2021

NOTE:  around Nov 2, regularly reload this page as likely changes will occur.

## Combination Techniques

* Combining after deconvolution:
  * feather
     [M100 combination in CASA 5.7](https://casaguides.nrao.edu/index.php?title=M100_Band3_Combine_5.7) or
     [M100 combination in CASA 6.1](https://casaguides.nrao.edu/index.php?title=M100_Band3_Combine_6.1)
  * [dc2019 talk by Ginsburg](https://keflavich.github.io/talks/FeatheringPresentation/FeatheringPresentation.slides.html?transition=fast); 
    see also his [uvcombine](https://github.com/radio-astro-tools/uvcombine/) package
  * ssc (Faridani)
* Combining before deconvolution:
  * [tp2vis](https://github.com/tp2vis/distribute)
  * [sdintimaging](https://github.com/urvashirau/WidebandSDINT)
* Combining during deconvolution (Model Assisted Cleaning)
  * [hybrid](https://sites.google.com/site/jenskauffmann/research-notes/adding-zero-spa)


## Data needed

For some example scripts we use 
the M100 ALMA science verification data
as described in [M100 Band3 casaguide](https://casaguides.nrao.edu/index.php?title=M100_Band3)
but since this data is 23 GB, it will take some time and processing to bring
it down to a more manageably size.  We have culled it down to 100MB, which can
be downloaded from http://admit.astro.umd.edu/~teuben/QAC/qac_bench5.tar.gz   
These contain 3 datasets: ALMA 12m, ALMA 7m and ALMA ACA (single dish), each with 70 aligned channels
of 5 km/s width, and the example script how the culling was done.

* ALMA 
* PHANGS-ALMA (CO(2-1))

### Example Processing Steps

You can find these scripts in the dc2019/scripts directory. The Makefile also explains how to run them, and in which order!

0. M100_getdata.sh -  a shortcut script that will get the 23GB data
1. M100_combine1.py - this is the script version of the casaguide, which we cover in class
2. M100_trimdata.py - only needed if you want to reproduce the 100MB 5km/s dataset from the original 23 GB data
3. M100_combine2.py - the QAC version of M100_combine1.py (about 14 min)
4. M100_tp2vis.py - combination using tp2vis
5. M100_combine3.py - combination using sdintimaging (QAC version)
5. M100_combine4.py - combination using tp2vis (QAC version)
6. M100_combine6.py - combination using a Kaufman's model assisted cleaning approach (QAC version)
6. M100_final.py - summarize and plot all M100 experiments (QAC version)

## Software 

* CASA (5.8 or 6.4): https://casa.nrao.edu/
* analysis scripts : https://casaguides.nrao.edu/index.php/Analysis_Utilities
* MIRIAD
* wsclean : https://gitlab.com/aroffringa/wsclean
* tp2vis: https://github.com/tp2vis/distribute  or more experimental, via QAC: https://github.com/teuben/QAC/
* peel: https://iopscience.iop.org/article/10.3847/2515-5172/ab35d5/meta
* Radio Astro Tools:  http://radio-astro-tools.github.io/
* Viz tools:
  * casaviewer (comes with CASA) or the task **imview**
  * CARTA: https://cartavis.org/
  * ds9 


## References

* Vogel et al. 1984 : https://ui.adsabs.harvard.edu/abs/1984ApJ...283..655V

* Jorsater and van Moorsel 1995, AJ, 110, 2037 : http://adsabs.harvard.edu/abs/1995AJ....110.2037J

* Koda et al. 2011, ApJS, 193, 19 : http://adsabs.harvard.edu/abs/2011ApJS..193...19K

* Koda et al. 2019, PASP, 131, 054505 : https://ui.adsabs.harvard.edu/abs/2019PASP..131e4505K

* Faridani et al. 2017, AN, 339, 87 :   https://ui.adsabs.harvard.edu/abs/2018AN....339...87F
 
* Arras et al. 2018 : https://arxiv.org/abs/2008.11435

* CASA reference manual and cookbook : https://casa.nrao.edu/index_docs.shtml
  * casaguides: https://casaguides.nrao.edu/index.php?title=Main_Page
  * Measurement Set: https://casa.nrao.edu/casadocs/latest/reference-material/measurement-set
  * https://casadocs.readthedocs.io/en/stable/notebooks/synthesis_imaging.html :
    [tclean](https://casadocs.readthedocs.io/en/stable/api/tt/casatasks.imaging.tclean.html)
  * https://casadocs.readthedocs.io/en/stable/notebooks/image_combination.html :
    [sdintimaging](https://casadocs.readthedocs.io/en/stable/api/tt/casatasks.imaging.sdintimaging.html) and
	[feather](https://casadocs.readthedocs.io/en/stable/api/tt/casatasks.imaging.feather.html)



* [Improving Image Fidelity on Astronomical Data: Radio Interferometer and Single-Dish Data Combination](https://www.lorentzcenter.nl/improving-image-fidelity-on-astronomical-data-radio-interferometer-and-single-dish-data-combination.html) Lorentz workshop 
and the [github repo](https://github.com/teuben/dc2019) - 12 - 16 August 2019 (Leiden, Netherlands)

* [Submillimetre Single-dish Data Reduction and Array Combination Techniques](https://www.eso.org/sci/meetings/2018/SingleDish2018.html)
and the [github repo](https://github.com/teuben/sd2018) - 15 - 16 March, 2018 (ESO Garching)






