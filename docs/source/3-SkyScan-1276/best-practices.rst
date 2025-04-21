SkyScan 1276 - Best practices
=============================

Imaging preparation
-------------------
- **Minimize motion artifacts:** Use appropriate anesthesia to reduce breathing and movement. Minimize animal motion by gently taping the legs and securing the body. This reduces motion blur and improves image sharpness.
- **Support thermoregulation:** Maintain the scanner gantry warm during in vivo scans Place animals on a heated bed or use warming pads during imaging to prevent hypothermia, which can alter physiology and image quality.
- **Standardize animal positioning:** Securely position animals in the same anatomical orientation using positioning beds, molds and tape. Consistent posture is essential for reproducibility in longitudinal or comparative scans.
- **Remove metal artifacts:** Ensure the animal is free from any metallic tags or implants in the region of interest, as these can introduce significant artifacts.

Acquisition settings
--------------------
- **Use standardized scan parameters:** Fix voltage, current, filters, integration time, and exposure settings across scans to enable reliable comparisons. Avoid using automatic exposure settings when quantification is needed.
- **Use flat field correction to improve image uniformity:** Apply flat field correction during or prior to reconstruction to compensate for spatial sensitivity variations across the detector and uneven X-ray illumination. This reduces ring artifacts and gradient shading across the image, especially important for high-precision or quantitative applications.
- **Optimize resolution versus dose:** Choose a resolution that balances image quality with radiation exposure. High-resolution scans (≤10 µm voxel size) significantly increase radiation dose and may not be necessary for all applications.
- **Minimize radiation dose in longitudinal studies:** Use low-dose protocols when tracking changes over time to avoid affecting biological processes or animal health.
- **Use respiratory gating for thoracic imaging:** For lungs or heart imaging, respiratory/cardiac gating improves image clarity by synchronizing acquisition with the breathing cycle.

Calibration and controls
------------------------
- **Perform scanner calibration regularly:** Use phantoms to calibrate for Hounsfield units, density, or BMD depending on application. Recalibrate if scan quality degrades or after hardware changes.
- **Include internal or external phantoms:** When quantifying density or structure (bone), use calibration phantoms in the field of view or perform concurrent scans (with same settings) for normalization.
- **Use age- and sex-matched controls:** MicroCT outcomes can vary significantly with age, sex, and body size. Matching across groups is essential for valid comparisons.

Data processing and quantification
----------------------------------
- **Apply consistent reconstruction parameters:** Use the same reconstruction algorithm, voxel size, and filters to avoid introducing variability during image processing.
- **Use a consistent image segmentation and analysis pipeline across individuals:** Standardize the entire workflow, from image segmentation to quantitative analysis, using fixed parameters and methods across all animals. This includes thresholding, filtering, ROI/VOI placement, and feature extraction. Consistency minimizes variability, improves reproducibility, and ensures valid comparisons between individuals, groups, or time points.
- **Segment using standardized thresholds:** When segmenting structures, use predefined and validated Hounsfield Unit thresholds to ensure consistency across scans and subjects.
- **Use 3D ROI placement for repeatability:** Define volumes of interest (VOIs) using anatomical landmarks in 3D software. Save templates to reuse across subjects and time points.
- **Specify quantitative endpoints:** Clearly define whether using volume, density, trabecular thickness, porosity, and always report units and calculation methods.
- **Avoid partial volume effects:** Especially in small structures, ensure resolution is sufficient to avoid under- or over-estimation due to voxel averaging.

General recommendations
-----------------------
- **Pilot scan before full study:** Run a small test cohort to define scan parameters, and analysis workflow.
- **Schedule imaging consistently:** Perform scans at the same time of day to control for circadian effects on physiology and biodistribution.
- **Document all scan parameters and animal metadata:** Include anesthesia protocol, positioning details, scan settings, and animal weight/condition in each imaging session log to enable accurate interpretation and troubleshooting.

Ex vivo sample hydration and stabilisation
------------------------------------------
- **Immobilize the sample inside the tube**
    - Wrap the sample in a moist gauze, sponge, or soft foam soaked with 70% ethanol or PBS.
    - Alternatively, embed delicate tissues in 1–2% agarose gel (excellent support and hydration) or low-melting-point paraffin (scanning after dehydration).
    - This combination of hydration and mechanical stabilization prevents drift during scanning.
    - Use only low-density, X-ray transparent materials (polystyrene foam, Kapton) to avoid imaging artifacts.
- **Use custom or sealed containers**
    - Place the sample in sealed tubes or containers (microcentrifuge tubes, Kapton tubing...) or when using Falcon tubes, add a custom insert (3D-printed or foam) to cradle the sample snugly.
    - **Limit liquid volume:** Use only enough to cover the sample, and fill air gaps to minimize turbulence.
    - Ensure a tight fit to eliminate sample floating or shifting during rotation.
- **Seal and maintain a moist environment**
    - Seal containers with parafilm or caps to prevent evaporation.
    - If scanning without full sealing, place a moist cotton or sponge pad nearby inside the chamber to maintain humidity.
    - Minimize scan time for sensitive tissues to reduce dehydration risk.

Image resolution
----------------


Understanding major CT artifacts
--------------------------------
Ring artifact
^^^^^^^^^^^^^
Ring artifacts are visual anomalies that appear in reconstructed 2D slices of CT data as **circular or concentric rings**
centered on the rotation axis. These rings can vary in intensity and thickness and may appear across many or all reconstructed slices.
They are an **artifact of the detector system and acquisition geometry**, not actual features of the scanned object.
Ring artifacts are a result of the fixed detector geometry in cone-beam CT systems and inconsistent detector pixel responses.
In a in vivo microCT, which use a rotating gantry design where the X-ray source and detector rotate around a fixed sample,
these artifacts typically originate from **inconsistencies in the detector's pixel response**. If certain pixels are overly
sensitive, under-responsive, or noisy, they introduce systematic intensity errors in every projection image acquired
during the scan. As the source-detector pair rotates, these fixed-pattern inconsistencies are projected through the
stationary sample at different angles. When the 2D projections are reconstructed into cross-sectional images, the **consistent**
**pixel-based errors** from the rotating detector manifest as **ring-shaped patterns**. These artifacts do not correspond
to real structures in the sample and can obscure or distort important details, especially in homogeneous or low-contrast regions.
Mitigation strategies include detector calibration, proper flat-field correction, and post-scan ring artifact suppression
during reconstruction.

Principal causes
""""""""""""""""
- **Detector pixel inhomogeneity:** Each pixel has a slightly different gain and response. Over time (or with aging), these differences can grow—especially if not properly gain-corrected or flat-field corrected.
- **Defective or noisy pixels:** "Hot pixels" (pixels stuck at a high value) and "cold pixels" (unresponsive) will leave consistent trails across projections. These linear inconsistencies become concentric rings after reconstruction.
- **Beam instability:** Small fluctuations in the X-ray tube output (thermal drift, voltage instability) during scan acquisition can cause projection variability.
- **Scintillator imperfections:** The scintillator screen may accumulate dust, have aging patches, or develop minor defects that translate to signal bias. These local inconsistencies cause persistent error lines in projections.
- **Misaligned center of rotation:** Even slight errors in aligning the rotation axis with the reconstruction center will exaggerate rings or cause them to shift position.
- **Sample centering errors:** If the sample is far off-center, it can result in shadowing that affects how individual pixels respond, leading to localized rings in the reconstruction.

Minimizing ring artifact
""""""""""""""""""""""""
- Acquisition (prevention)
    - **detector warm-up**: Always allow 10–20 minutes warm-up before scanning to stabilize detector response.
    - **Flat-field correction**: Take new bright-field (X-ray on, no object) reference images regularly.
    - **Beam stability:** Ensure X-ray source is warmed up and consistent—use high-quality power supply and avoid rapid scan starts/stops.
    - **Sample centering:** Keep the sample aligned to the rotation axis. Avoid mounting near the edges of the field of view.
    - **Use Frame Averaging:** Averaging 3–5 frames per projection reduces random noise and softens minor detector differences.
- Reconstruction (correction)
    - **Misalignment correction:** Corrects off-axis rotation to apply if ring centers drift or tilt
    - **Ring artifact correction:** Removes consistent circular bands
    - **Smoothing:** Blurs out sharp ring edges	to apply cautiously

Motion artifact
^^^^^^^^^^^^^^^
Motion artifacts are **distortions** in microCT images caused by voluntary or unvoluntary **sample movement during scanning**.
Instead of appearing as clear structures, the reconstructed image shows blurring, double edges or ghosting, radial streaks.
These artifacts compromise image sharpness, morphometric accuracy, and interpretability.

Principal causes
""""""""""""""""
- **Physiological movement (in vivo):** Breathing, heartbeat, or spontaneous muscle twitches during animal scans.
- **Sample instability or shifting:** Loose mounting, dehydration, or improper securing of the sample in the holder.
- **High-resolution scans:** Ssmall voxel size amplifies even small movements.

Preventing motion artifact
""""""""""""""""""""""""""
- Ex vivo
    - **Immobilize the sample*
        - Wrap in moist gauze, sponge, or low-density foam to physically stabilize it.
        - Embed in 1–2% agarose or low-melt paraffin for soft tissues.
    - **Secure mounting**
        - Use tight-fitting holders or custom inserts.
        - Avoid loose placement in Falcon or Eppendorf tubes without internal support.
        - Eliminate free-floating in liquid: minimize liquid volume or fill air gaps to prevent sloshing.
    - **Minimize vibrations**
        - Place scanner on a vibration-damped bench.
        - Ensure scanner doors are closed securely during operation.
    - **Optimize scan settings**
        - Use frame averaging (3–5) to reduce the effect of small vibrations.
        - Avoid ultra-long scans if mounting is not extremely secure.
- In vivo
    - **Use proper anesthesia**
        - Use isoflurane gas anesthesia with controlled delivery and monitoring.
        - Maintain low, steady respiration rate throughout the scan.
        - Minimize scan time to reduce physiological stress.
    - **Positioning and restraint**
        - Use a custom animal bed or cradle with: bite bar or nose cone, body supports, tape and/or foam pads to reduce movement
        - Avoid tight compression that could trigger discomfort or reflex movement.
    - **Temperature and monitoring**
        - Maintain normothermia using a heating pad or warm air flow.
        - Monitor respiration and vital signs to detect restlessness or shallow breathing.
    - Use Respiratory gating (if available)
        - If scanning organs affected by motion (lungs), use gated acquisition to synchronize image capture with the breathing cycle.

Windmill artifact
^^^^^^^^^^^^^^^^^
Undersampling in microCT occurs when the **rotation step size between consecutive projection images is too large**, resulting
in an **insufficient number of angular projections** collected over 180° or 360° of rotation. This violates the Nyquist sampling
criterion, which requires that the object be sampled with **enough angular resolution** to faithfully reconstruct its
smallest structural details. The rotation step directly determines how many projection images (views) are acquired: a
smaller step size yields more projections and higher angular sampling density, while a larger step reduces the number of
projections, increasing the risk of undersampling. A simple approximation to estimate the rotation step is to divide the rotation range (360°)
by the detector width (512, 1024...) to ensure that each detector pixel samples the object from a unique angle.
When undersampling occurs, fine anatomical or material structures cannot be accurately resolved, leading to image artifacts
such as blurring, **aliasing**, or the **characteristic “windmill” artifact**. To prevent this, the number of projections
should be chosen based on the object's size and the desired voxel resolution, ensuring adequate coverage of angular space
for precise reconstruction.

Main causes of undersampling
""""""""""""""""""""""""""""
- **Excessive rotation step size:** Using a large angular increment between projections (1.0° instead of 0.3°) leads to not enough projections to satisfy the Nyquist criterion for the object’s detail level.
- **Inadequate number of projections for object size:** Fewer projections than required for the object's diameter and voxel size generates fine structures (like trabeculae or implants) are undersampled in angular space.
- **Mismatch between Vvxel size and angular sampling:** Choosing high resolution (small voxel size) but not increasing the number of projections accordingly results in geometric information is angularly under-represented, despite fine spatial sampling.
- **Shortened scan range:** Scanning over <180° instead of a full 180° or 360° range leads to incomplete projection data which increases interpolation artifacts during reconstruction.
- **Time-saving scan settings:** Reducing projection count to shorten scan time (in vivo imaging) is acceptable for low-resolution overviews but results in undersampling for fine structures.
- **Over-reliance on averaging or filtering:** Using frame averaging or smoothing instead of improving angular resolution might reduce noise, but doesn’t replace the need for adequate projection sampling.

Reducing windmill artifact
""""""""""""""""""""""""""
- **Use a small enough rotation step:** The rotation step determines how many views you collect during the scan and directly affect the angular resolution.
- ** Use 360° rotation:** Full rotation provides redundant and more uniform sampling for dense samples, irregular geometries and low-constrast soft-tissues and helps avoiding asymmetric undersampleinss the object.
- **Avoid reducing projections to save time:** Don't sacrfice angular resolution for faster scans, redue frame averaging if needed instead of projection count.
- **Match angular sampling to spatial resolution:** For high voxel resolution a fine angluar sampling is crucial. A mismatch between high spatial resolution and low angular sampling results in aliasing and windmill artifacts.

Beam-hardening artifact
^^^^^^^^^^^^^^^^^^^^^^^
Beam hardening is an X-ray imaging artifact that arises from the **polychromatic (multi-energy) nature of the X-ray beam**.
As the beam passes through a dense material, the **lower-energy (softer) X-rays are absorbed** more readily than the
higher-energy (harder) ones. This **selective attenuation** alters the energy spectrum of the beam, causing the transmitted
beam to have a **higher average energy than the incident beam**, a process referred to as **"beam hardening"**. Because
most CT reconstruction algorithms assume a monochromatic beam, this change in energy distribution leads to **non-linear attenuation errors**.
The resulting artifacts can manifest as **cupping effects** (where the center of dense objects appears artificially dark),
**edge brightening**, or **streaks between dense regions**. Beam hardening is particularly pronounced in scans of bone,
metal, or high-density materials, and is commonly corrected using a combination of pre-filtering, optimized scan settings,
and beam hardening correction algorithms during reconstruction.

Main causes of beam-hardening
"""""""""""""""""""""""""""""
- **Polychromatic Xray beam:** Standard microCT systems polychromatic (broad-spectrum) X-ray beams. As the beam passes through matter, low-energy photons are preferentially absorbed. This shifts the energy distribution toward higher average energy and the beam becomes “hardened".
- **High-density or thick material:** Materials with high atomic number (Z) or mass density (bone, metal, contrast agents) cause significant attenuation of low-energy photons.
- **Absence or improper use of filter:** Without metal filtr to pre-harden the beam, a large portion of low-energy X-rays reaches the sample. This increases the intensity of beam hardening effects, especially at lower voltages. Using the wrong filter type or thickness can fail to adequately shape the beam.
- **Low tube voltage settings:** Low-voltage scans (40–50 kV) produce a spectrum with more low-energy X-rays. These soft X-rays are easily absorbed, increasing differential attenuation and beam hardening. Higher voltages (>70 kV) generate harder beams that are less susceptible to this effect.
- **Improper sample positioning:** If dense regions are off-center, they may skew the beam non-uniformly. This can exaggerate the hardening effect on one side and lead to asymmetric streaking or cupping.

Limiting beam-hardening
"""""""""""""""""""""""
- **Use appropriate Xray filters:** Use physical metal filters that pre-harden the beam as absorb low energy Xrays before they reach the sample. The resulting beam becomes more uniformin energy reducing the artifact formation.
- **Increase source voltage:** Higher voltage are inherently harder and more penetrating.
- **Apply beam hardening correction:** Apply beam hardening correction factor during reconstruction of 20-40% for bone and 10-20% for soft tissues. The correction adjusts for the attenuation curve to better approximate the polychromatic beam's behavior.
- **Calibrate with phantom:** Use known-density phantom to calibrate the greyscale to density curve that will improve the beam hardening modeling for quantitative BMD analysis.

Metal artifact
^^^^^^^^^^^^^^
Metal artifacts are **imaging distortions** that occur when X-rays interact with very dense or highly attenuating materials,
such as metal implants, screws, dental restorations, or surgical clips. these artifacts appear in reconstructed images as **streaks**,
**starbursts**, **dark bands and shadows** and **bright overshoots at interfaces**.

Main causes of metal artifact
"""""""""""""""""""""""""""""
- **Beam hardening:** Metal absorbs low-energy X-rays very strongly. Only high-energy photons pass through, resulting in a "hardened" beam. This creates dark bands or cupping near and behind the metal.
- **Photon starvation:** When metal is very thick or dense, almost all X-rays are absorbed, and very few photons reach the detector. This leads to low signal-to-noise, especially in projections passing through the metal. This results in streaks and noise radiating from the metal called starburst effect.
- **Scattering:** X-rays scatter off metal surfaces, contributing to detector signal from non-direct paths. This adds noise and ghost-like effects near the metal.
- **Undersampling and angular inconsistency:** If angular sampling isn’t high enough, the sudden intensity drop near metal edges can cause reconstruction errors. This is worsened by motion or if metal is not fully within the field of view.

Reducing metal artifact
"""""""""""""""""""""""
- **Use high tube voltage:** This increases phton energy so more Xrays can penetrate the metal 80–100 kV for bone with implants.
- **Apply a beam-hardening filter:** Use 1 mm Al or Cu filters to pre-harden the beam which reduces differential absorption and softens artifact severity.
- **Apply beam-hardening correction in reconstruction:** Set correction to 30–60% for metal-bearing samples. Adjust iteratively based on visual artifact reduction.
- **Increase frame averaging:** Reduces random noise and improves signal uniformity in high-attenuation regions.
- **Use ROI scanning or masking:** If metal is localized, focus scan or crop region to exclude non-relevant artifact-heavy areas.
