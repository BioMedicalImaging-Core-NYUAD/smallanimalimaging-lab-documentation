nVue-nVision - Best practices
=============================

Intracranial viral injection
----------------------------
- **Use precise stereotaxic targeting**: Accurate targeting is essential for reproducible biosensor expression. Begin by properly securing the animal in the stereotaxic frame and ensure flat skull positioning by aligning bregma and lambda along the same dorsoventral plane. To confirm correct antero-posterior and medio-lateral alignment, measure and compare coordinates from both landmarks, refining head tilt or rotation as needed.
- **Validate biosensor expression:** Optimization of AAV delivery parameters, including viral titer, injection volume, and serotype, is essential to achieve robust yet non-toxic expression of genetically encoded biosensors. This optimization step requires post-mortem assessment of native fluorescent signal intensity in the injected region. Direct visualization of the reporter enables evaluation of expression strength, distribution, and potential off-target effects. If suboptimal expression is observed, adjustments to titer or injection parameters should be made accordingly.
- **Validate and refine injection coordinates:** To ensure accurate delivery of the AAV vector into the intended brain structure, post-mortem analysis is also used to confirm anatomical targeting. Fluorescent reporter visualization in brain sections allows precise verification of needle placement and spread. If signal localization is misaligned with the region of interest, injection coordinates should be refined in subsequent cohorts. This step is particularly critical when targeting small or deep structures, where small deviations can result in non-specific expression or ineffective imaging.

Intracranial lens implantation
------------------------------
- **Use precise stereotaxic targeting**: Accurate targeting is essential for reproducible biosensor expression. Begin by properly securing the animal in the stereotaxic frame and ensure flat skull positioning by aligning bregma and lambda along the same dorsoventral plane. To confirm correct antero-posterior and medio-lateral alignment, measure and compare coordinates from both landmarks, refining head tilt or rotation as needed.
- **Use digital and motorized stereotaxic systems for precision:** Incorporate digital stereotaxic frames to obtain real-time coordinate readouts, increasing targeting reproducibility and reducing operator variability. When available, utilize motorized stereotaxic arms for highly precise coordinate refinement and controlled, programmable injection speeds. These systems allow for stepwise delivery, consistent needle advancement, and reduced mechanical artifacts.
- **Validate implantation depth and alignment:** Confirm lens placement post-mortem using immunohistochemistry. Validate targeting accuracy and adjust coordinates for future experiments as needed.
- **Plan lens depth and trajectory based on imaging target**: Use stereotaxic brain atlases to determine the exact depth and position of the region of interest. To avoid mechanical compression and ensure optimal image quality, adjust the implantation depth by subtracting ~150 μm from the target region's dorsal coordinate. This offset accounts for the focal distance of the GRIN lens, ensuring that the miniscope's imaging plane aligns with the desired neuronal layer, which lies just beneath the lens tip.
- **Perform craniotomy with precision and minimal trauma:** Drill a clean, appropriately sized craniotomy directly above the target site. Use a dental drill at low speed with intermittent irrigation to avoid overheating. Carefully remove the skull flap using fine forceps or a microsurgical hook.
- **Select an appropriate surgical approach:** Choose the surgical technique, whether scalpel incision, guide needle insertion, or tissue aspiration, based on the depth, anatomy, and accessibility of the target brain region, as well as the diameter and length of the GRIN lens.
- **Implant lens slowly and steadily:** Lower the GRIN lens into the brain at a rate of ~100–200 μm per 30–60 seconds.
- **Secure the lens and align the baseplate:** Fix the baseplate-integrated lens in place using UV-curable or quick-setting dental cement, ensuring no movement during curing.
- **Protect the implant post-surgery:** Cover the exposed lens with a protective cap to prevent contamination and damage. Use the removable dummy miniscope for handling habituation and added mechanical protection during recovery.
- **Allow post-operative recovery before imaging:** Provide analgesics and monitor animals closely for 7–14 days post-surgery. Allow for wound healing, inflammation resolution, and glial response attenuation, which are necessary for obtaining stable, high-quality imaging signals.

Image acquisition
-----------------
- **Mount/unmount miniscope carefully:** o reduce stress-related movement artifacts and behavioral variability, habituate the animal to the mounting and unmounting procedure through repeated mock sessions prior to actual imaging. Consistent handling and gradual exposure to the device help minimize stress responses and promote stable behavior during recording.
- **Calibrate imaging parameters per session:** Adjust LED power, sensor gain, exposure time, and focal plane using imaging software. Avoid overexposure and photobleaching.
- **Maintain consistency across animals/sessions:** Use fixed imaging settings for longitudinal comparisons. Log parameters for traceability.
- **Minimize session duration and light intensity:** To reduce the risk of photobleaching and phototoxicity, limit continuous imaging sessions to the minimum duration necessary for data collection. Avoid excessive LED intensity by adjusting the excitation power to the lowest level that provides sufficient signal-to-noise ratio. For extended recordings exceeding 15 minutes, implement brief recovery intervals, 5-minute break every 15 minutes, to allow tissue cooling and fluorophore recovery.
- **Synchronize with behavior:** Integrate video tracking or TTL signals for timestamped alignment of fluorescence data with behavioral events.

Behavioral consistency and environmental control
------------------------------------------------
- **Standardize task timing and design:** Ensure consistency in task type (open field, T-maze), stimulus delivery, and inter-trial intervals.
- **Control for circadian and physiological variables:** Perform imaging at the same time of day. Monitor and account for factors such as satiety, stress, or fatigue.
- **Minimize interference with implant:** Use arenas that reduce risk of the animal bumping, dislodging, or contaminating the baseplate.
- **Protect the implant between sessions:** Use baseplate covers or head-mounted shields to prevent contamination or mechanical damage.

Data processing and quantification
----------------------------------
- **Perform motion correction and preprocessing:** Use IDPS, CaImAn, or CNMF-E for drift correction and background subtraction.
- **Segment ROIs with standardized pipelines:** Apply consistent settings for automated or manual segmentation. Save templates for reuse across sessions.
- **Normalize fluorescence traces:** Calculate ΔF/F using appropriate baselines.
- **Denoise and align to behavior:** Apply filtering, deconvolution (if needed), and align traces to behavior using synchronized timestamps or triggers.
- **Ensure repeatability and transparency:** Document all parameters. Version-control analysis scripts and share as open-source where possible.

Experimental controls and validation
------------------------------------
- **Conduct pilot experiments:** Validate vector efficacy, imaging feasibility, behavior compatibility, and data quality before scaling up.
- **Include matched controls:** Match for age, sex, strain, and condition when comparing across groups or treatment conditions.
- **Perform regular post hoc validation:** Confirm expression pattern, GRIN lens location, and tissue health using IHC, DAPI staining, or confocal imaging.
- **Log comprehensive metadata:** Record animal ID, age, weight, surgical notes, viral info, imaging settings, behavioral metrics, and experiment date/time.