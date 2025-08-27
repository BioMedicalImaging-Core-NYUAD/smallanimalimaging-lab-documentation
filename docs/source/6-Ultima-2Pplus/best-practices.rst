Ultima 2Pplus - Best practices
==============================

Imaging preparation
-------------------
- **Surgical preparation and window clarity:** Ensure high-quality cranial window or thinned-skull preparation for stable optical access. Avoid dura bleeding or cloudy bone, as scattering reduces excitation efficiency and emission signal. Apply cover glass properly to minimize motion and improve optical clarity.
- **Minimize motion artifacts:** Use proper head-fixation with a titanium headplate or stereotaxic clamps to prevent drift. Consider light anesthesia or awake head-fixed paradigms depending on experiment needs. When under anesthesia, monitor depth carefully as it affects vascular tone and neural activity.
- **Thermoregulation:** Maintain body temperature with a heating pad or feedback-controlled stage, as hypothermia alters metabolism and neural physiology.

Signal acquisition
------------------
- **Laser power management:** Use the minimum laser power that provides sufficient signal-to-noise ratio (SNR) to reduce photobleaching and phototoxicity.
- **Distribute power across depth:** Deeper structures require higher power, but increase gradually to avoid surface damage.
- **Excitation wavelength tuning:** Match the laser wavelength to the absorption peak of the chosen fluorophore. For dual-color imaging, optimize compromises between fluorophore excitation and bleed-through.
- **Frame rate vs field-of-view:** Adjust scan speed depending on temporal vs spatial resolution needs. Use resonant scanning for fast dynamics, and galvanometric scanning for high-resolution structural imaging.
- **Z-stack acquisition:** Use optimal step sizes to resolve 3D structures. Avoid repeated rescanning of the same planes to minimize bleaching.

Imaging optimization
--------------------
- **Pilot imaging sessions:** Run test sessions to assess fluorophore brightness, expression pattern, and signal stability before committing to large-scale studies.
- **Avoid circadian effects:** Perform imaging at consistent times of day to reduce variability in neural activity patterns.
- **System warm-up:** Allow laser and detectors to stabilize thermally for consistent output and sensitivity.


Image quality
-------------
- **Laser alignment and calibration:** Regularly align the laser beam path and check dispersion compensation for optimal excitation.
- **Objective considerations:** Use high NA, water-immersion objectives for deep tissue penetration. Ensure proper immersion medium without bubbles or drying.
- **Depth penetration:** Expect imaging depths of 500–800 μm in cortex depending on tissue scattering, fluorophore brightness, and preparation quality.
- **Motion correction:** Use frame-by-frame registration during preprocessing to reduce residual motion artifacts, especially in awake animals.

Data quantification
-------------------
- **ROI consistency:** Define ROIs consistently across sessions. Use anatomical landmarks or reference vasculature patterns.
- **ΔF/F normalization:** For functional imaging, calculate ΔF/F relative to baseline to normalize across sessions and animals.
- **Bleaching and drift:** Correct for slow baseline drifts due to bleaching or phototoxicity in analysis pipelines.
- **Statistical comparisons:** Match controls by age, sex, and experimental conditions. Always specify ROI definition method and quantification metrics.

Experimental controls and validation
------------------------------------
- **Single-fluorophore controls:** Validate spectral separation in multi-color experiments using singly-expressing animals or tissue.
- **Histological verification:** Confirm expression patterns, cranial window placement, and tissue health post hoc with immunohistochemistry or confocal imaging.
- **Pilot groups:** Test surgical success rate, expression variability, and imaging stability before scaling up.