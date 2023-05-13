---
permalink: /research/
title: ""
---

# Gravitational Waves

Gravitational Waves are a prediction of Einstein's General Relativity (i.e, his theory of gravitation). GR stitches together space and time into a single fabric called spacetime. Unlike Newtonian physics where spacetime is a passive canvas on which the dynamics of the Universe plays itself out, GR asserts that spacetime is in fact an active participant. Agglomerations of matter and energy warp and curve the fabric of spacetime, and the geometry of spacetime determines the trajectory of objects in the vicinity of these agglomerations.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/curvature.jpg" alt="">
<figcaption>Matter/massive objects curve spacetime. The trajectories of particles and light rays in the vicinity of the massive object are determined by the geometry of spacetime in the object's neighborhood. Image Credit: nature.com</figcaption>

If that is not amazing enough, GR further predicts that spacetime can also "ripple". When massive objects accelerate, they produce these ripples in spacetime that we call gravitational-waves (GWs). They are, however, extremely weak, and therefore notoriously difficult to detect. For example, binary black holes orbiting their mutual centre of mass produce GWs. 

{% include video id="I_88S8DWbcU" provider="youtube" %}
<figcaption>Simulation of a binary black hole coalescence event. Orbiting black holes have a time varying mass quadrupole moment. They therefore emit GWs, which carries away the orbital energy and angular momentum of the binary. As a result, the binary inspirals, and eventually merges. Gravitational lensing effects have also been incorporated here, causing the stars in the background to appear magnified -- as if seen through a magnifying glass. Video Credit: The SXS Project. </figcaption>

These GWs travel billions of light years (the exact distance depends on the location of the source) before they reach the Earth. Their effect on a kilometer long object is to stretch and squeeze it by an amount that's smaller than the radius of the nucleus of an atom!

{% include video id="S2vp7iVWrkE" provider="youtube" %}
<figcaption>Animation of a binary black hole coalescence event, with the GW strain polarizations plotted below. Notice the small values of the strains on the y-axis. These correspond to a change in length of a kilometer long object of less than the radius of the nucleus of an atom. Video Credit: SXS Project. </figcaption>

Detecting GWs is therefore a monumental challenge. 

{% include video id="tQ_teIUb3tE" provider="youtube" %}
<figcaption>The LIGO-Virgo detectors are the most sensitive rulers to have ever been made. Nevertheless, the fundamental principle/technique used to measure the tiny changes in length -- interferometry -- is the same as what was used famously by the Michelson-Morley experiment -- the experiment that confirmed the constancy of the speed of light and could not find evidence of an all-pervading aether. Video Credit: LIGO Lab Caltech/MIT </figcaption>

Nevertheless, the LIGO-Virgo network of ground-based interferometric detectors observed the merger of two black holes in September 2015 (GW150914). A new window to the Universe was thus opened, and a new branch of Astronomy was born, viz., GW-Astronomy.

{% include video id="QyDcTbR-kEA" provider="youtube" %}
<figcaption> Coalescing binary black holes produce a GW chirp signal: the inspiral of the binary emits GWs with continuously increasing frequency. Curiously, the frequency range detectable by the LIGO-Virgo network falls within the range of frequencies audible to the human ear. Thus, an audio readout of the GW strains detected can actually be heard. With some (or a lot of) imagination, the sound of merging black holes is reminiscent of singing birds. Make sure to have your speaker system switched on when watching the video. Video Credit: LIGO Lab Caltech/MIT </figcaption>

The vast majority of the GW events detected so far (as of May 2022) have been binary black hole mergers, although merging binary neutron stars and neutron star black hole binaries have also been observed. In fact, arguably the most spectacular detection so far occurred in August 2017 (GW170817), when the merger of a binary neutron star produced both GWs and light (Electromagnetic Waves across a range of frequencies). LIGO-Virgo detected the GWs, and announced this detection to astronomers worldwide, who then followed it up with various telescopes. If memory serves, this is the most followed-up astronomical transient event in recorded history.

{% include video id="e7LcmWiclOs" provider="youtube" %}
<figcaption> A binary neutron star coalescence event is rich with science. With GW170817, the GWs and electromagnetic emissions detected, in tandem, enabled some of the most exciting results in GW astronomy so far. These include confirming the provenance of energetic events such as short gamma-ray bursts and kilonovae, novel tests of GR, a measurement of the Hubble constant that determines the expansion rate of the universe, clues about the nature of matter in the densest of regimes, and much more. Video Credit: NASA Goddard. </figcaption>

Other sources of GWs are also predicted, but remain to be observed (as of May 2022), including (but not limited to) a stochastic GW background produced by unresolved compact binary merger events, continous GWs from isolated spinning neutron stars, and bursts of GWs from exploding stars called supernovae.

# Gravitational-Wave Data Analysis

Extracting GWs from detector data is a highly non-trivial exercise. GWs manifest themselves as strains, change in length divided by length, of extended objects. These strains are minute, smaller than one part in a thousand million trillion. Such minute strains are notoriously difficult to measure, even for extended 4 Km long arms in interferometric detectors. Not surprisingly, the GW strain is buried deep in the noise of the detectors. There are many sources of noise, including seismic noise, thermal noise, photon shot noise, etc. Nevertheless, sophisticated data analysis techniques exist to extract the GW from the noise. These techniques essentially use a filtering process that involves cross-correlating the detector data with a theoretical template of the GW. This specific kind of filtering process is called Matched Filtering. Matched filtering can be shown to be the optimal method if the noise is well modelled as a stationary Gaussian random process, and if the signal buried in the noise is well modelled by the template used for matched filtering. 

GW signals carry with them imprints of the sources that produced them. Thus, the masses and spins of a compact binary that inspirals and merges governs the shape of the GW. 

{% include video id="gmmD72cFOU4" provider="youtube" %}
<figcaption> The shape of the GW depends on the parameters of the compact binary that produced them. In particular, the masses and spins of the components of the binary imprint themselves on the GW. The animation illustrates the changing shape of the GWs for the different detected GW events. The background score is quite peaceful too, so do keep your speaker system turned on while watching! Video Credit: The SXS Project. </figcaption>

Since these parameters are not known a-priori, it is not clear which GW template should be constructed for filtering the data. To mitigate this, a template bank is constructed, consisting of hundreds of thousands, or even millions, of GW templates, covering a targeted space of masses and spins. All these templates are cross-correlated with the detector data, and a signal-to-noise ratio (SNR) statistic is constructed. The template that provides the largest SNR is expected to be the template that best matches the signal in the data, at least for stationary Gaussian noise.

{% include video id="bBBDR5jf9oU" provider="youtube" %}
<figcaption> Matched filtering is the method by which which GW signals are extracted from noise. The method relies on cross-correletating a GW template with the detector data to produce an SNR statistic. In stationary Gaussian noise, the SNR is expected to be the optimal statistic. In the animation above, a template is used to matched-filter detector data strain represented as a time series. The template is slid across the time axis, since the time of arrival of the signal is not known a-priori. When the template perfectly aligns with the signal, the SNR time series produces a peak. Video Credit: Alexander Nitz. </figcaption> 

# My Research

Text to appear soon. For now, please click on the Publications tab on the top right corner of this page to check out my publications.
