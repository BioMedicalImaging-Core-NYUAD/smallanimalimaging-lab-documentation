In vivo Optical Imaging
#######################

Technology overview
*******************
In vivo optical imaging is a versatile, non-invasive, non-destructive modality that enables the visualization and quantification of biological
processes in living organisms through the detection of emitted light generated from within the biological system.
This approach offers unique advantages for small-animal imaging, including high sensitivity, real-time monitoring, and
longitudinal assessment under physiological conditions.

In the context of preclinical biomedical research, in vivo optical imaging systems have become widely adopted for whole-body
imaging in small animal models such as mice and rats. Operating in the visible to far-red spectral range (450-900nm), these
systems provide an effective balance between spatial resolution, tissue penetration, high sensitivity, and minimal physiological disruption.
Their ability to conduct non-invasive, high-throughput, and longitudinal imaging makes them indispensable tools for monitoring
molecular and physiological events over time.

Two major emission-based imaging modalities dominate this field: fluorescence imaging and bioluminescence imaging.

Challenges
==========
.. image:: ../_static/light_interaction.png
   :alt: *Light interaction with biological matter*
   :width: 400px
   :align: center

.. raw:: html

  <br>

Non-invasive in vivo optical imaging provides a powerful platform for tracking biological processes in live animals.
However, it faces several important challenges that can impact imaging performance, accuracy, and data interpretability:

- **Limited tissue penetration:** Both excitation and emission photons are subject to significant absorption and scattering by biological tissues.
This dramatically restricts photon penetration depth, particularly for visible-wavelength fluorophores or reporters,
thereby limiting the modality’s utility for imaging deep anatomical structures. To mitigate this limitation, far-red
fluorescent reporters with high brightness should be prioritized, as far-red signals (650–900 nm) penetrate more deeply
into tissues (brain, lung, and liver). Despite substantial progress in fluorescent protein engineering—shifting emission
spectra toward the far-red for improved in vivo imaging—bioluminescence imaging remains limited by the availability of
bright far-red-emitting luciferases.

- **Limited spatial resolution:** Optical imaging systems offer whole-body imaging but with relatively low spatial resolution due to photon diffusion and
scattering in tissue. These effects lead to signal blurring and poor localization accuracy, especially when imaging deep-seated
organs. The deeper the emission source, the more pronounced the scattering. Three-dimensional fluorescence molecular tomography
(FMT) has emerged as an alternative approach, enabling improved signal localization and quantitative probe distribution in 3D.

- **Autofluorescence and background noise:** In fluorescence imaging, endogenous tissue autofluorescence,primarily from skin, fur, and dietary components, can significantly
reduce the signal-to-noise ratio. Mitigating autofluorescence is essential for reliable in vivo fluorescence imaging.
This can be achieved by using albino mouse strains to minimize melanin absorption, employing hairless strains or shaving
prior to imaging, and implementing an alfalfa-free diet to reduce chlorophyll-induced gut fluorescence. Although bioluminescence
imaging inherently avoids autofluorescence, it remains susceptible to signal attenuation due to tissue scattering and often
exhibits low photon output.

- **Quantitative limitations:** Optical signal intensity is influenced by a range of variables including reporter expression level, brightness, tissue depth,
inter-animal and positional variability. As a result, both fluorescence and bioluminescence imaging are typically semi-quantitative,
requiring rigorous normalization and the inclusion of standardized controls to support meaningful comparisons.

- **Substrate and probe delivery issues: Bioluminescence imaging requires systemic delivery of substrates (D-luciferin, coelenterazine), and is affected by variability
in injection efficiency, biodistribution, metabolism, and tissue perfusion. Moreover, luciferase activity is dependent on
intracellular ATP and oxygen availability, rendering the signal sensitive to hypoxic or necrotic environments and potentially
leading to variability across tissues or in disease states. Similarly, fluorescent probes may suffer from non-specific distribution,
poor bioavailability, or off-target accumulation, all of which can compromise signal specificity. Optical signal propagation
is further influenced by tissue pigmentation, vascularization, and hydration.

- **Restricted multiplexing (bioluminescence): While fluorescence imaging enables multiplexing through the use of spectrally distinct fluorophores and spectral unmixing
algorithms, bioluminescence imaging is more limited in this regard. Overlapping emission spectra and the shared substrate
requirements of common luciferases restrict the number of distinct reporters that can be simultaneously imaged, complicating
multi-parametric experimental designs.


Fluorescence imaging
********************
Fluorescence imaging relies on the use of fluorophores—synthetic dyes, nanoparticles, or genetically encoded fluorescent
proteins—which are molecules capable of emitting light upon the absorption of photons at specific excitation wavelengths.
These fluorophores absorb light at a defined excitation wavelength and subsequently emit light at a longer wavelength due
to energy dissipation.

.. image:: ../_static/fluorescence.png
   :alt: *Principle of fluorescence*
   :width: 400px
   :align: center

.. raw:: html

  <br>

In in vivo imaging systems, excitation light is typically delivered using spectrally filtered light-emitting diodes (LEDs),
(AMI HT system), or via broadband white-light sources combined with excitation filters (IVIS Spectrum).
These illumination strategies enable selective excitation of fluorophores at their optimal wavelengths, enhancing specificity
and minimizing off-target activation. The resulting fluorescent photons are captured by highly sensitive, cooled charge-coupled
device (CCD) cameras after passing through wavelength-specific emission filters, which selectively isolate the desired signal.
This approach, employing narrow-band excitation and emission wavelengths, effectively minimizes background noise originating
from tissue autofluorescence and reduces spectral overlap between multiple fluorophores.

This modality enables the targeted visualization of specific biological structures or molecular events through the use of fluorophores conjugated to targeting moieties such as antibodies, peptides, or receptor ligands. The use of near-infrared (NIR) fluorophores—typically within the 650–900 nm spectral range—enhances imaging performance by increasing tissue penetration and reducing signal interference from endogenous tissue autofluorescence.

Advantages
==========


Disadvantages
=============

2D versus 3D tomography
=======================

Bioluminescence imaging
***********************

.. image:: ../_static/bioluminescence.png
   :alt: *Principle of bioluminescence*
   :width: 400px
   :align: center

.. raw:: html

  <br>


Advantages
==========


Disadvantages
=============


2D versus 3D tomography
=======================


Quick tips for in vivo optical imaging
**************************************
