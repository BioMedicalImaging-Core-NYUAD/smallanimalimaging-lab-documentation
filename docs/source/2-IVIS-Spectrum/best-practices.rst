IVIS Spectrum - Best practices
==============================

Imaging preparation
-------------------
- **Reduce light absorption by tissue:** Use hairless or albino animals to minimize melanin-associated photon absorption. If using hairy or pigmented strains, fully shave the imaging area before acquisition to reduce photon loss due to melanin and hair scattering. If using chemical depilation, rinse thoroughly to avoid skin irritation that could impact signal
- **Limit tissue autofluorescence:** Feed animals an alfalfa-free (chlorophyll-free) diet for at least 1 week prior to imaging. This minimizes gastrointestinal autofluorescence
- **Standardize physiological conditions:** Use consistent anesthesia protocols and a heated stage to prevent hypothermia, which can affect probe biodistribution and signal intensity
- **Ensure consistent animal positioning:** Position animals in the same orientation across imaging sessions to allow accurate and reproducible ROI placement

Signal acquisition
------------------
- Avoid auto-exposure for raw signal quantification:
    - When working with uncalibrated photon counts, disable auto-exposure
    - Keep all camera settings (exposure time, binning, f/stop) constant for comparability
- Use radiance (bioluminescence) or radiance efficiency (fluorescence) for calibrated, cross-study comparisons:
    - Exposure-independent quantification: Radiance is normalized for exposure time, making it robust to minor variations in acquisition settings
    - Enables cross-animal and group comparisons: Because it accounts for imaging variables, radiance allows for reliable signal comparison between animals, groups, and imaging sessions, even if ROI sizes or exposures differ
    - Improves reproducibility in longitudinal studies: Ideal for tracking biological changes over time in the same subject, since it removes technical bias from repeated measurements
    - Essential for multi-center or multi-operator studies: Radiance allows for standardized data interpretation across labs using same systems, assuming proper calibration

Imaging optimization
--------------------
- **Start with a pilot experiment:** Define signal kinetics and substrate/probe timing, especially for bioluminescence imaging
- **Avoid imaging during circadian fluctuations:** Image animals at consistent times of day to reduce variability in metabolism and gene expression
- **Allow imaging system warm-up:** Let CCD cameras and optics stabilize thermally for consistent sensitivity and minimal signal drift

Fluorescence-specific tips
--------------------------
- **Use far-red fluorophores:** Prefer fluorophores emitting 650–900 nm for better tissue penetration and reduced autofluorescence
- **Apply spectral unmixing and background subtraction:**
    - Use reporter-negative control animals to characterize tissue autofluorescence
    - Define background ROIs in non-targeted regions (contralateral tissue) for subtraction
    - Ensure consistent ROI placement and size across background and target areas
- Ensure proper controls for multiplex imaging:
    - Include single-reporter control animals for each fluorophore to establish accurate spectral fingerprints and avoid cross-channel bleed-through
    - Use contralateral tissue or a background ROI within the same animal as internal reference region to estimate and subtract non-specific signal
    - Use reporter-negative animals imaged with all channels to define baseline autofluorescence across filters

Bioluminescence-specific tips
-----------------------------
- Use freshly prepared substrate
- Store luciferin/coelenterazine at -80°C in the dark, and avoid repeated freeze-thaw cycles
- Optimize substrate administration route: Choose IP or IV injection based on timing and biodistribution needs
- Account for metabolic and physiological variability: Luciferase signal depends on ATP and oxygen availability, consider how disease state, perfusion, and tissue viability may affect interpretation

Data quantification
-------------------
- **Define consistent ROIs:** Use anatomical landmarks to apply identical ROI shape and placement across animals and time points
- Use average or total signal appropriately:
    - Use total signal when ROIs vary in size (growing tumors)
    - Use average signal when ROIs are consistent in size/shape, especially in comparative studies
    - Always specify which metric is used to ensure interpretability
- Never quantify signal from saturated ROIs:
    - Saturated signals are clipped, meaning they do not represent true photon flux, and should be excluded from quantitative analysis
    - To prevent saturation: Use a shorter exposure time, increase the f/stop to reduce the aperture and hence reduce the light and reduce binning
- Always keep your signal well within the dynamic range of the detector
