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