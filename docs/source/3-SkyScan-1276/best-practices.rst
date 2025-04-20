SkyScan 1276 - Best practices
=============================


Improving image resolution
--------------------------
Imaging Preparation
Minimize motion artifacts: Use appropriate anesthesia to reduce breathing and movement. Isoflurane gas anesthesia is preferred for its controllability and rapid recovery. Ensure consistent induction and maintenance levels across subjects.

Support thermoregulation: Place animals on a heated bed or use warming pads during imaging to prevent hypothermia, which can alter physiology and image quality.

Maintain hydration: Provide subcutaneous saline before or after anesthesia in longer scans (>30 min) to mitigate dehydration, especially during longitudinal studies.

Standardize animal positioning: Securely position animals in the same anatomical orientation using positioning beds or molds. Consistent posture is essential for reproducibility in longitudinal or comparative scans.

Remove metal artifacts: Ensure the animal is free from any metallic tags or implants in the region of interest, as these can introduce significant artifacts.

Acquisition Settings
Use standardized scan parameters: Fix voltage (kVp), current (µA), integration time, and exposure settings across scans to enable reliable comparisons. Avoid using automatic exposure settings when quantification is needed.

Optimize resolution vs. dose: Choose a resolution that balances image quality with radiation exposure. High-resolution scans (e.g., ≤10 µm voxel size) significantly increase radiation dose and may not be necessary for all applications.

Minimize radiation dose in longitudinal studies: Use low-dose protocols when tracking changes over time to avoid affecting biological processes or animal health.

Use respiratory gating for thoracic imaging: For lungs or heart imaging, respiratory (or cardiac) gating improves image clarity by synchronizing acquisition with the breathing cycle.

Calibration and Controls
Perform scanner calibration regularly: Use phantoms to calibrate for Hounsfield units, density, or BMD (bone mineral density) depending on application. Recalibrate if scan quality degrades or after hardware changes.

Include internal or external phantoms: When quantifying density or structure (e.g., bone), use calibration phantoms in the field of view or perform concurrent scans for normalization.

Use age- and sex-matched controls: MicroCT outcomes can vary significantly with age, sex, and body size. Matching across groups is essential for valid comparisons.

Data Processing and Quantification
Apply consistent reconstruction parameters: Use the same reconstruction algorithm, voxel size, and filters to avoid introducing variability during image processing.

Segment using standardized thresholds: When segmenting structures (e.g., bone, lung, tumor), use predefined and validated Hounsfield Unit thresholds to ensure consistency across scans and subjects.

Use 3D ROI placement for repeatability: Define volumes of interest (VOIs) using anatomical landmarks in 3D software. Save templates to reuse across subjects and time points.

Specify quantitative endpoints: Clearly define whether using volume, density, trabecular thickness, porosity, etc., and always report units and calculation methods.

Avoid partial volume effects: Especially in small structures, ensure resolution is sufficient to avoid under- or over-estimation due to voxel averaging.

General Recommendations
Pilot scan before full study: Run a small test cohort to define scan parameters, anesthesia tolerability, and analysis workflow.

Schedule imaging consistently: Perform scans at the same time of day to control for circadian effects on physiology and biodistribution.

Document all scan parameters and animal metadata: Include anesthesia protocol, positioning details, scan settings, and animal weight/condition in each imaging session log to enable accurate interpretation and troubleshooting.