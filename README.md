# Data Combination notes 

For lecture 10 (November 2, 2021) of https://github.com/anand0xff/FourierOpticsJHU2021


## Combination Techniques


* [feather](https://casa.nrao.edu/casadocs/casa-5.4.1/image-combination/feather)  - [talk by Ginsburg](https://keflavich.github.io/talks/FeatheringPresentation/FeatheringPresentation.slides.html?transition=fast); see also the [uvcombine](https://github.com/radio-astro-tools/uvcombine/) package
* [tp2vis](https://github.com/tp2vis/distribute)
* [hybrid](https://sites.google.com/site/jenskauffmann/research-notes/adding-zero-spa)
* [sdintimaging](https://github.com/urvashirau/WidebandSDINT)
* ...


## Data needed

We use the M100 data set as described in CASA's wiki, but since this data is 23 GB, it can be culled down to 100MB, which can
be easily downloaded from ....    These are 3 datasets: ALMA 12m, ALMA 7m and ALMA ACA (single dish), each with 70 channels
of 5 km/s width.

## Software 

* CASA (5.8 or 6.4): https://casa.nrao.edu/
* tp2vis: https://github.com/tp2vis/distribute  or more experimental, via QAC: https://github.com/teuben/QAC/
* peel: https://iopscience.iop.org/article/10.3847/2515-5172/ab35d5/meta
* Radio Astro Tools:  http://radio-astro-tools.github.io/
* CARTA: https://cartavis.org/

## References

* Jorsater and van Moorsel 1995, AJ, 110, 2037 : http://adsabs.harvard.edu/abs/1995AJ....110.2037J

* Koda et al. 2011, ApJS, 193, 19 : http://adsabs.harvard.edu/abs/2011ApJS..193...19K

* Koda et al. 2019, PASP, 131, 054505 : https://ui.adsabs.harvard.edu/abs/2019PASP..131e4505K

* CASA reference manual and cookbook : http://casa.nrao.edu/docs/cookbook/
  * Measurement Set: https://casa.nrao.edu/casadocs/latest/reference-material/measurement-set

* [Improving Image Fidelity on Astronomical Data: Radio Interferometer and Single-Dish Data Combination](https://www.lorentzcenter.nl/improving-image-fidelity-on-astronomical-data-radio-interferometer-and-single-dish-data-combination.html) Lorentz workshop 
and the [github repo](https://github.com/teuben/dc2019) - 12 - 16 August 2019 (Leiden, Netherlands)

* [Submillimetre Single-dish Data Reduction and Array Combination Techniques](https://www.eso.org/sci/meetings/2018/SingleDish2018.html)
and the [github repo](https://github.com/teuben/sd2018) - 15 - 16 March, 2018 (ESO Garching)






