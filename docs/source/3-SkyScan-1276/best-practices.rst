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

Image quality
-------------
In microCT, achieving high image quality involves balancing multiple factors that influence spatial resolution, signal-to-noise ratio,
and artifact suppression. Below is an integrated overview of how each parameter contributes to overall image quality.

- **Pixel/Voxel size**
    - Smaller voxel size improves spatial resolution, allowing finer detail to be captured.
    - Small pixel size reduces the number of X-ray photons per voxel, potentially lowering SNR unless compensated by longer exposure or averaging.
    - Optimize by choosing the smallest voxel size that still provides sufficient SNR for your sample.
- **Rotation step (angular increment)**
    - Smaller angular steps yield more projection images per rotation.
    - Low rotation step improves image consistency and reconstruction quality, reduces noise, and helps minimize artifacts.
    - Very large steps can cause undersampling, degrading both resolution and SNR.
    - Use finer steps (<0.5°) for high-detail samples; larger steps for faster scans where ultra-fine detail isn’t needed.
- **Frame averaging**
    - Averaging multiple frames per projection reduces random noise and enhances SNR.
    - Particularly valuable when scanning at lower voltages or with small voxel sizes.
    - Typically, 3–5 frames per projection (ex vivo) offer a good SNR improvement without excessive scan time.
- **Filter selection**
    - Filters (Al, Cu) remove low-energy X-rays that contribute to noise and beam hardening.
    - This hardens the X-ray beam, improving penetration and contrast uniformity, indirectly enhancing image quality and SNR.
    - Use filters to improve image consistency, especially for dense samples like bone or metal.
- **Tube voltage (kV)**
    - Higher voltage increases X-ray energy, improving penetration and SNR, especially in dense materials.
    - Lower voltage enhances contrast in low-density samples but may reduce penetration and increase noise.
    - Match voltage to sample type: low kV for soft tissue, high kV with filters for dense samples.
- **Source-to-sample distance (geometric magnification)**
    - Bringing the X-ray source closer increases magnification, reducing effective voxel size and improving spatial resolution.
    - Increased magnification may amplify motion artifacts and reduce SNR if photon flux is not adjusted.
    - Use for high-resolution scans of small features, ensuring other parameters (exposure, averaging) support good SNR.
- **Non-binning versus inning (detector settings)**
    - Non-binning retains full detector resolution, capturing maximum spatial detail.
    - It collects fewer photons per pixel, resulting in lower SNR.
    - Binning (2×2) combines adjacent pixels, improving SNR at the cost of spatial resolution.
    - Use non-binning when high detail is essential and SNR can be managed through other settings.

.. image:: ../_static/Skyscan-image-quality.png
   :alt: *Imaging parameters affecting microCT quality*
   :width: 1000px
   :align: center

*Imaging parameters affecting microCT quality*

.. raw:: html