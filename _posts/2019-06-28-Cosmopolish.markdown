---
title:  "Cosmopolish"
date:   2019-06-28 15:14
categories: [research, cosmology]
tags: [research, astropy, cosmology, kepler]
---
**Project KillBlue:**

I have to take photos of the blue sky and find stars in post-processing. I asked a dozen of my professional photographer friends (dime a dozen in Bushwick) and they all say this is impossible. It isn't, but it is quite difficult. I need photons from stars 60+ light years away to hit the lens of my phone's camera without getting mogged by all the Rayleigh Scattered blue photons all over the place. Phone cameras use a CMOS, not a CCD (more on that later) so it's not so much a matter of your skills in post but whether or not those 60+ year old photons have touched the inefficient photoreceptor on the camera. 

About a week ago, I thought I had seen a miracle. The moon, the blue twilight, and a bright star that turned out to be Jupiter. I spoke to Big Boss Hogg about this, and I think he accepts using it as a star because the next steps for me are stacking and creating software that will find Jupiter in each image. 

I've experimented with stacking this morning - you basically take thousands of images of something and stack them atop one another so as to increase the flux and depth of that object. As for the 'software', my background in ML makes me think 'image classifier' but maybe it'd be easier to just plot lightcurve histograms and look for spikes in white (or orange) wavelength light. Better white and make all the images monochromatic. 

Only obstacle so far in this project is the camera. I'm going to need a telephoto lens. I'm also going to have to play with exposure times to make out light trails, even though this will cause the blue sky to saturate. I'm not too worried about the rest of the sky though, since it is essentially blue screen. 

**Project $550 Million Dollar Thermometer:**

This project is a trip. The Kepler spacecraft uses CCD's as photoreceptors which have a 95+% quantum efficiency, meaning that pretty much any photon that hits it is captured. I think it's something like 7% for an ordinary camera. However, these CCD's must be kept at a hypercool temperature (-85C last time I checked), or else something called 'dark currents' occur. These are the quantum equivalents of phosphenes. They produce pixels as if touched by light, except not requiring a single photon. This contributes to noise, particularly Nyquist noise, which can be observed in the light curves that Kepler regularly produces. 

The idea behind the project is that the Kepler spacecraft's production of light curves (ie. measurement of changes in flux of stars) is so precise (as to detect exoplanets) that one could hypothetically make sense of whatever noise occurs and deduce the temperature of the CCD's. This is in comparison to the actual sensors that measure the temperature of the CCD's and associated electronics. 

According to the official sources, Kepler has 29.5% noise error, and 9.5% of that is due to on-board electronics. That is higher than they had expected, and good news for those who want some meat to bite into and analyze. I spent this morning trying to get sensor data from the "ancillary engineering data" which is basically like 1000+ FITS files that (I hope I'm wrong about this) you can only get through their anonymous FTP server. Though, I did see 'curl' and 'wget' somewhere on the page for MAST so that may help me get these files by the batch. 

But the FITS files are still rather confusing. It isn't just the photographic image like most FITS files that are relevant. It's like a hundred different parameters and data readings all for one quarter I believe. I'm not sure how to approach this yet. 

But overall, I believe I have to first choose a planet (I'll choose my old sweetheart KIC 8462852), and plot hundreds of lightcurves over one another to have a solid foundation. Then I'll start to analyze the noise. 

I did a bit of that here: 

![](https://prettypositron.github.io/minimal/images/Screenshot_20190609-161837.jpg)
![](https://prettypositron.github.io/minimal/images/Screenshot_20190609-161834.jpg)
![](https://prettypositron.github.io/minimal/images/Screenshot_20190609-161830.jpg)

Except I removed variability basically randomly, and so I have to be able to identify the right type of noise first. 

Then I have to be able to look at the corresponding sensor data and build a model for it. Don't even know how to go about that yet. 

---

**Project Talent Epicenter**

REDACTED.

---

That's it for now. 
