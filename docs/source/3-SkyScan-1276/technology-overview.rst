SkyScan 1276 - Technology overview

In vivo micro-computed tomography (microCT) is a powerful, non-invasive, non-destructive and high-resolution imaging modality
that allows for the **visualization and quantification of anatomical structures and physiological changes** in live animal models.
It operates by acquiring a **series of X-ray projections from multiple angles**. 2D projections are secondly reconstructed
into slice-by-slice cross-sectional images to provide a detailed **3D volumetric datasets** of internal features with micrometer-scale precision.

This technology is particularly advantageous in preclinical biomedical research due to its ability to provide **quantitative
structural information** from live rodents (mice and rats) without the need for surgical intervention or destructive sampling.
By enabling longitudinal studies, microCT allows researchers to follow **anatomical changes** over time in the same animal.
MicroCT excels in imaging **high-density tissues** such as bone, teeth, and implants, and can be extended to soft tissues using
contrast agents. Compared to optical imaging, microCT provides superior anatomical detail and penetration depth, though it
requires careful management of radiation dose for repeated in vivo applications.

Important considerations
------------------------
.. image:: ../_static/Xray_interaction.png
   :alt: *Xray interaction with biological matter*
   :width: 1000px
   :align: center

*Xray interaction with biological matter*

.. raw:: html

In vivo microCT enables high-resolution anatomical imaging in live animals, but its performance is shaped by the interaction
of ionizing X-rays (electromagnetic wavelengths between 0.01 - 10 nm) with biological tissues. These interactions affect
image contrast, radiation dose, and the reliability of longitudinal data, especially in soft tissue and high-resolution studies:

- **Rayleigh scattering**
Rayleigh scattering occurs predominantly at low photon energies, typically below 30 keV. In this process, X-ray photons are
coherently scattered—deflected by atoms without any energy loss or ionization. It is most prominent in low-density biological
tissues, such as fat and soft connective tissue, where loosely bound electron clouds enable elastic scattering through
induced dipole oscillations. Although no energy is transferred, the change in photon trajectory contributes to background
signal and spatial blurring. This effect is particularly noticeable at tissue interfaces and ultimately leads to a reduction
in spatial resolution.

- **Compton scattering**
Compton scattering is the dominant interaction within the typical energy range of in vivo microCT imaging, approximately
30 to 150 keV. It involves an inelastic collision between an X-ray photon and a loosely bound outer-shell electron. A
portion of the photon’s energy is transferred to the electron, which is ejected from the atom as a recoil electron. The
remaining energy is retained by the scattered photon of lower energy and longer wavelength. This ionizing process
is most prevalent in soft, lean tissues such as muscle, liver, and heart, which are primarily composed of low atomic number
elements (like hydrogen and carbon). The resulting recoil electrons additionally ionize surrounding molecules, leading
to the generation of reactive oxygen species and direct DNA strand breaks. These effects are particularly detrimental
in highly proliferative tissues such as bone marrow, gonads, skin, and intestinal epithelium, where they can lead to mutations,
impaired tissue regeneration, or cell death. Additionally, Compton scattering reduces image contrast and spatial resolution
due to photon absorption and angular deviation, ultimately contributing to signal degradation and image noise.

- **Photoelectric effect**
The photoelectric effect is an ionizing interaction that occurs predominantly at lower photon energies, typically between
20 and 60 keV, and is strongly dependent on the atomic number (Z) of the absorbing material. In this process, an X-ray
photon is fully absorbed by a tightly bound inner-shell electron, which is then ejected as a photoelectron. The resulting
shell vacancy is filled by an outer-shell electron, releasing a characteristic (fluorescent) X-ray. This secondary photon
may either escape, be reabsorbed via another photoelectric event, or undergo Compton or Rayleigh scattering, contributing
to localized dose or image noise.
This interaction enhances image contrast and spatial resolution due to the high differential absorption of X-rays by tissues
with varying atomic composition. As a result, large differences in X-ray attenuation arise between structures such as bone,
soft tissue, or contrast-enhanced regions (barium, gold, iodine), producing strong image contrast. Additionally, because
the incident X-ray is fully absorbed (with no scattered photon) there is no redirection of signal away from the detector
axis, minimizing image blurring and improving spatial accuracy. This effect is particularly pronounced at tissue interfaces,
where abrupt changes in density or composition lead to edge enhancement. These transitions enhance boundaries between
adjacent voxels, creating both perceived and true spatial resolution gains in the final image. However, the photoelectric
effect also contributes significantly to radiation dose and localized ionization. The energy deposited by photoelectrons
and subsequent secondary interactions may lead to tissue damage, particularly in radiosensitive organs (bone marrow, osteogenic tissue).
Therefore, its benefits must be balanced against biological risks, especially in longitudinal or high-dose imaging protocols.

.. image:: ../_static/comparison-Xray-interaction.png
   :alt: *Comparative overview of X-ray interactions with biological tissue*
   :width: 1000px
   :align: center

*Comparative overview of X-ray interactions with biological tissue*

.. raw:: html

- **Biological impact of ionizing radiation**
Ionizing radiation occurring during in vivo microCT imaging leads to the formation of ROS and induces direct DNA strand
breaks. These effects directly contribute to genetic mutations, impaired tissue regeneration, and cell death. In highly
proliferative tissues, these outcomes are particularly detrimental. Repeated or excessive exposure in these radiosensitive
regions can significantly increase the risk of tumor formation, developmental abnormalities, and reproductive system
malformations, especially when imaging protocols are not optimized. Importantly, maintaining the lowest possible radiation
dose should be a fundamental priority in in vivo studies, particularly when scans are repeated over short intervals or
conducted during sensitive developmental windows.

MicroCT imaging
---------------
.. image:: ../_static/microCT.png
   :alt: *In vivo microCT*
   :width: 1000px
   :align: center

*In vivo microCT*

.. raw:: html

Xray generation
^^^^^^^^^^^^^^^
X-ray generation is a complex process in which electrons are thermionically emitted from a heated tungsten filament at the
cathode and **accelerated toward the anode under a high-voltage potential**, typically adjustable between 40 and 100 kV. The
accelerated electron beam is directed onto a **tungsten target**, selected for its high atomic number (Z = 74) and high melting point,
which together enable efficient X-ray production (0.01 - 10 nm) through two primary mechanisms:

- **Bremsstrahlung radiation**
Bremsstrahlung radiation is produced when high-speed electrons are rapidly **decelerated or deflected** by the strong electric
field of atomic nuclei within the anode target material, such as **tungsten**. As the negatively charged electrons approach
the positively charged nucleus, their change in velocity results in the **emission of X-ray photons**. The energy of these
photons varies continuously depending on how close the electron comes to the nucleus and how much kinetic energy is lost
during the interaction. This process generates a **broad, continuous spectrum of X-ray energies* ranging from near zero up
to the maximum energy defined by the tube voltage (100 keV for a 100 kV tube). Bremsstrahlung radiation is the dominant form
of X-ray emission in most tubes, particularly at higher tube voltages, and serves as the **primary background radiation** used
in imaging applications.

- **characteristic radiation**
Characteristic radiation only occurs when an incident electron has sufficient energy to **ionize a tightly bound inner-shell**
**electron**, typically from the K-shell, of a target atom. This ejection creates a vacancy, which is then filled by an
electron from a higher-energy shell (L or M shell). The difference in binding energy between these shells is emitted as
**an X-ray photon with a discrete, element-specific energy**. These emissions are referred to as "characteristic" because
they correspond to the unique electronic structure of the target material. For tungsten, the most common target material
in microCT, characteristic peaks are observed at approximately 59 keV (Kα) and 67 keV (Kβ). Unlike Bremsstrahlung radiation,
which is continuous, characteristic radiation appears as **sharp peaks** superimposed on the X-ray spectrum and contributes
to **enhanced contrast** when the tube voltage exceeds the binding energy of the K-shell.

.. image:: ../_static/Xray-generation.png
   :alt: *Mechanisms of X-ray generation in a microfocus X-ray tube*
   :width: 1000px
   :align: center

*Mechanisms of X-ray generation in a microfocus X-ray tube*

.. raw:: html

Alternatively, lower-Z target materials such as copper or molybdenum may be employed in material science applications,
particularly in X-ray diffraction or the imaging of thin or low-density samples where softer X-rays are advantageous. However,
tungsten remains the predominant target material in both preclinical and clinical imaging systems due to its superior X-ray yield,
deeper tissue penetration, and high thermal resilience.

The tungsten target is embedded within a copper stem to facilitate rapid heat dissipation, and the anode assembly is actively
cooled to maintain focal spot sharpness and system stability during prolonged scans. The emitted X-ray beam then exits through
a diaphragm and passes through a motorized filter changer, which enables the **selection of beam-hardening filters** (aluminum,
copper, or Al+Cu combinations) to tailor spectral energy and minimize low-energy artifacts.

This entire process occurs within a **vacuum-sealed glass envelope**, ensuring efficient electron acceleration and minimizing
scattering losses. This configuration enables microCT systems to generate highly stable, low-noise X-ray
beams with adjustable resolution, dose, and energy settings, making them suitable for a **wide range of in vivo and ex vivo**
**biological imaging applications**.

Xray attenuation
^^^^^^^^^^^^^^^^
X-rays are attenuated as they pass through a sample due to their interactions with matter, primarily via **Rayleigh scattering**,
**Compton scattering**, and the **photoelectric effect**. Compton scattering dominates at higher photon energies and in
low-Z materials, while the photoelectric effect is more prevalent at lower energies and in high-Z substances. Rayleigh scattering,
though non-ionizing and elastic, contributes minimally to attenuation but can influence image quality through signal redirection.

The **degree of attenuation** is influenced by multiple factors, including **sample density**, **thickness**, **atomic composition (Z)**,
and the **energy of the incident X-ray beam**. This **partial and differential attenuation** of X-rays as they traverse various
tissues or materials forms the **physical basis of image contrast** in both X-ray radiography and computed tomography (CT).
Differences in attenuation coefficients among adjacent structures enable the visualization and distinction of internal
features, making attenuation a critical determinant of image quality.

Xray projection and detection
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
After passing through the specimen, the transmitted X-rays are incident on a **digital detector**, which converts the attenuated
X-ray intensity into a measurable two-dimensional image, referred to as a **projection**. The detector includes a **scintillator layer**,
a material capable of emitting visible light upon absorption of incoming X-ray photons, effectively converting X-ray energy
into a light signal. This light is subsequently detected by either a **flat-panel detector**, consisting of large-area photodiode
arrays suited for wide-field imaging, or a **scientific-grade CMOS or CCD sensor**, which converts the light into an electrical signal
whose intensity is directly proportional to the intensity of the transmitted X-rays.

These detectors capture the **spatial distribution of transmitted X-ray intensity** across the imaging plane with high
sensitivity and spatial resolution. However, conventional detectors operate in an **energy-integrating mode**, meaning they
accumulate the total signal from all incident photons without distinguishing their individual energies. As a result,
**no spectral or wavelength-specific information** is preserved, and the output reflects only the cumulative X-ray intensity or
**total photon flux**. This limitation reduces the ability to differentiate between materials with similar attenuation coefficients,
particularly when contrast depends on subtle energy-dependent interactions, and it contributes to imaging artifacts such as **beam hardening**.

To address this limitation, emerging technologies such as **spectral photon-counting CT** (SPCCT) enable the energy-resolved
detection of individual X-ray photons, providing **spectral information** in each projection. This capability allows for
improved material decomposition, artifact reduction, and potentially enhanced spatial and contrast resolution—especially
in soft tissue or contrast-enhanced imaging contexts. Although not yet standard in preclinical systems, SPCCT represents
a promising advancement in high-fidelity X-ray imaging.

Another approach to overcoming the limitations of energy-integrating detection consists of using **coherent, monochromatic X-rays**,
in which all photons possess a single, well-defined wavelength (or energy). This is typically achieved using **synchrotron radiation sources**
or advanced laboratory-based monochromators that filter polychromatic beams. By eliminating spectral heterogeneity, **monochromatic X-ray imaging**
minimizes beam hardening artifacts and improves the accuracy of quantitative measurements, especially in materials with
strong energy-dependent attenuation. Although not yet widely available in conventional microCT systems due to the complexity
and cost of monochromatic X-ray generation, this method offers significant advantages in high-precision material analysis and advanced contrast imaging.

Gantry rotation
^^^^^^^^^^^^^^^
The main distinction between X-ray radiography and computed tomography (CT) lies in the acquisition strategy. While conventional
X-ray imaging captures a single 2D projection of the object from a fixed angle, CT imaging acquires **multiple projections**
at **varying angular positions around the subject**. These projections are then **computationally reconstructed** into a three-dimensional
volume, enabling detailed visualization of internal structures with depth and spatial context.
In contrast, 3D fluorescence imaging typically reconstructs volumetric data from a series of 2D surface-weighted images
acquired using a scanning light source and a fixed detector. CT, however, achieves true tomographic imaging through a
**rotational acquisition geometry**, enabling depth-resolved imaging throughout the volume.

Two primary acquisition geometries are employed in CT systems, depending on the application and system design:

- **Rotating Sample Geometry**
Common in material science and ex vivo microCT systems, this configuration maintains a **stationary X-ray source and detector**,
while the sample is mounted on a rotating stage. This setup enables higher spatial resolution, reduced system size, and
greater mechanical stability. It is particularly advantageous for imaging small specimens with minimal motion and maximizing image detail.

- **Rotating Gantry Geometry**
Utilized in in vivo CT systems—including clinical scanners and some preclinical setups—the X-ray source and detector
rotate around a **stationary subject**. This geometry is ideal for live imaging, as rotating a living specimen is impractical
and may induce motion artifacts. Rotating gantry systems also allow for larger field-of-view imaging and faster scan
acquisition times. However, due to their mechanical complexity and reduced geometric magnification, these systems generally
offer lower resolution compared to stationary-source designs.

In both geometries, rotational acquisition is fundamental to tomographic imaging and is essential for accurate 3D reconstruction.
It enables **isotropic resolution** throughout the reconstructed volume, which is critical for quantitative and anatomical accuracy.

Image reconstruction
^^^^^^^^^^^^^^^^^^^^
Following acquisition, the series of two-dimensional X-ray projections (collectively referred to as a **sinogram**) are mathematically
reconstructed into **cross-sectional images** (slices) using algorithms such as **filtered back projection** that demonstrates high
computational efficiency and reconstruction accuracy. In certain cases, particularly under low-dose or noisy acquisition conditions,
**iterative reconstruction algorithms** may be applied to improve image quality and reduce artifacts.

**Pre-processing steps** applied prior to image reconstruction are fundamental for enhancing projection quality and ensuring
the accuracy of tomographic reconstruction. These operations correct for acquisition-related artifacts and optimize the raw
dataset before reconstruction algorithms are applied. Common pre-processing procedures include:

- **Misalignment compensation** corrects for **slight spatial discrepancies between projections** caused by mechanical tolerances or stage instability during rotation, ensuring **consistent alignment** across all angular views.
- **Ring artifact suppression** addresses **radial artifacts** caused by defective or uneven detector pixels that produce constant signals across projections, resulting in **ring-shaped distortions** in reconstructed slices.
- **Beam hardening correction** compensates for the **nonlinear attenuation of low-energy photons** in polychromatic X-ray beams, particularly in dense or high atomic number materials. This correction reduces cupping artifacts and improves the accuracy of grayscale representation in reconstructed images.

Additional steps may include image thresholding, smoothing filters to reduce noise, and pixel binning, which improves signal-to-noise
ratio at the cost of spatial resolution.
The resulting slices represent **sequential planes** through the scanned volume and are subsequently stacked to generate
a **three-dimensional volumetric dataset**. The spatial resolution of this dataset is defined by the **in-plane pixel size**
of the 2D detector and the **slice thickness**, both of which determine the **voxel pitch** (the smallest resolvable unit
of volume in the reconstructed image). In most microCT systems, the slice thickness is typically equal to the in-plane pixel
dimension, leading to the formation of **isotropic voxels**. This isotropic geometry allows for accurate three-dimensional
visualization and quantitative analysis of internal structures with uniform resolution across all spatial axes, depending
on the imaging configuration and acquisition parameters.

Data analysis
^^^^^^^^^^^^^
Data analysis in microCT refers to the **post-processing steps** that follow image reconstruction and involve operations such
as **image segmentation, thresholding, registration, and quantitative extraction of structural and morphological parameters**.
These steps are critical for translating volumetric image data into meaningful biological or material metrics. In in vivo microCT,
data analysis is commonly used to quantify **bone mineral density** (BMD) or **tissue mineral density** (TMD), as well as to
evaluate **tissue volume, microarchitecture, and morphology**. Additional applications include the quantification of
adipose tissue, assessment of implant integrity and stability, and monitoring of tissue regeneration or remodeling over time.
Accurate segmentation is essential for **isolating regions of interest**, and downstream quantification relies on voxel-based
measurements derived from the reconstructed 3D dataset. These analyses form the basis for longitudinal monitoring, phenotyping,
and treatment evaluation in preclinical research.

Advanced techniques for microCT imaging
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Respiratory gating
""""""""""""""""""


Cardiac gating
""""""""""""""


Advantages of microCT
^^^^^^^^^^^^^^^^^^^^^
- **High spatial resolution**
Typical in vivo microCT systems achieve 6–75 µm voxel resolution, enabling precise visualization of small-scale anatomical
structures such as trabecular bone, implants, or calcified tissues.

- **Strong signal-to-noise ratio**
High-quality detectors, X-ray flux optimization, and proper reconstruction filtering contribute to high SNR, especially
in dense and mineralized tissues.

- **High anatomical specificity**
Native tissue contrast in microCT is governed by X-ray attenuation, which depends on both tissue density and effective
atomic number. This makes the modality inherently well-suited for imaging bone, teeth, and other calcified structures,
where attenuation is high and signal contrast is strong. In addition, segmentation of lung, lean tissue, and adipose tissue
is feasible based on their differential attenuation properties and relative composition. Soft tissue visualization can be
further enhanced through the use of exogenous contrast agents, enabling targeted imaging of organs, vasculature, tumors,
or biomaterials.

- **Isotropic resolution**
The reconstruction process produces cubic voxels, ensuring isotropic spatial resolution and allowing for unbiased 3D
measurements in all directions.

- **Quantitative accuracy**
MicroCT enables direct, calibrated measurement of tissue properties such as bone mineral density (BMD), tissue mineral density (TMD),
tissue volume and surface area and trabecular/cortical thickness, porosity, and anisotropy.

- **Moderate soft tissue sensitivity**
Lean tissues show low native contrast. However, with iodinated, gold-based, or nanoparticle exogenous contrast agents, microCT
can visualize and quantify soft tissue morphology, perfusion, or tumor burden.

- **Non-destructive and repeatable**
MicroCT enables longitudinal, non-invasive imaging of the same subject over multiple time points, allowing researchers to monitor
biological processes such as disease progression, healing, or treatment response in vivo. This approach significantly reduces
inter-subject variability, lowers the number of animals required per study, and increases statistical power by enabling
within-subject comparisons across time.

- **High reproducibility**
Fixed geometries and standardized workflows (consistent reconstruction parameters) ensure high reproducibility across scans and studies.

- **3D volumetric output**
MicroCT produces complete, voxel-based 3D datasets suitable for downstream processing such as segmentation, registration,
3D rendering, and quantitative analysis.

- **Standardized grayscale calibration (Hounsfield Units)**
MicroCT systems support grayscale calibration to Hounsfield Units (HU) or equivalent standardized attenuation values using
reference phantoms (air, water, hydroxyapatite). This standardization facilitates direct comparison of scans across different
systems, sessions, or laboratories, and improves the reproducibility of quantitative measurements such as BMD,
tissue composition, and contrast agent uptake. HU calibration also enables co-registration with clinical CT datasets in
translational research workflows.

Limitations of microCT
^^^^^^^^^^^^^^^^^^^^^^
- **Exposure to ionizing radiation**
In vivo microCT involves exposure to ionizing X-rays, which can induce DNA damage and affect radiosensitive tissues such
as bone marrow, gonads, and the intestinal epithelium. This necessitates careful dose optimization, particularly in longitudinal or developmental studies.

- **Radiation-induced biological effects in longitudinal studies**
Even under low-dose protocols, repeated exposure can affect cell viability, tissue regeneration, or tumor response, potentially
confounding biological outcomes in sensitive models.

- **Limited soft tissue contrast (without contrast agents)**
Soft tissues with similar X-ray attenuation cannot be easily distinguished without the use of exogenous contrast agents.
This limits native soft tissue visualization and may complicate interpretation in non-contrast-enhanced protocols.

- **Motion artifacts in live imaging**
Respiration, cardiac motion, or general animal movement can degrade image quality, particularly for soft tissue imaging.
While respiratory and cardiac gating reduce motion blur, these require additional hardware and setup time and may not fully
eliminate motion-induced artifacts.

- **Low molecular specificity**
Unlike optical imaging modalities, microCT does not inherently provide molecular or functional information. It primarily
reflects anatomical and structural characteristics unless combined with specialized contrast agents targeting molecular features.

- **Contrast agent limitations**
Soft tissue imaging often depends on iodinated or nanoparticle-based contrast agents, which introduce variability in uptake,
clearance, and tissue retention. Their use may also raise concerns about toxicity, vascular leakage, or immune response.

- **Limited field of view (at high resolution)**
High-resolution imaging typically comes with a reduced field of view, making whole-body or multi-region scanning impractical
without sequential acquisitions or image stitching, which adds time and complexity.

- **Limited penetration through thick, dense, or high-Z samples**
X-ray transmission is inherently constrained by the energy output of the X-ray source and the attenuation characteristics
of the sample, which depend on its thickness, density, and atomic composition. In large or highly attenuating specimens,
such as obese animals, dense biomaterials, or metal-rich implants, X-ray photons may be excessively absorbed or scattered
before reaching the detector. This results in poor signal transmission, reduced contrast, and increased noise, ultimately
compromising image quality and quantitative reliability. While filters and higher voltage settings can partially compensate,
these adjustments may come at the cost of increased radiation dose or reduced soft tissue sensitivity.

- **Susceptibility to metal artifacts**
High-density materials such as surgical implants or metallic probes cause severe beam hardening and scattering effects,
resulting in streaking, blooming, or signal voids. These metal artifacts can obscure adjacent structures and impair both
visual interpretation and quantitative analysis. Although beam hardening correction and artifact reduction algorithms exist,
they often cannot fully eliminate these distortions, particularly in high-resolution imaging contexts.

- **High acquisition and reconstruction time for high resolution**
Achieving high-resolution imaging (≤10 µm voxel size) requires longer scan durations and slower rotation steps, increasing
anesthesia time in live animals and extending the total experimental workflow.

- **Large data volume and computational requirements**
High-resolution scans generate large 3D datasets, requiring significant storage capacity, image processing time, and specialized
software for reconstruction and quantitative analysis.

Recognizing major CT artifacts
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
- **Ring artifact**

- **Motion artifact**

- **Beam-hardening artifact**

- **Metal artifact**
