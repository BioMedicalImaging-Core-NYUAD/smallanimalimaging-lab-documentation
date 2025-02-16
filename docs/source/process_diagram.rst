SAI project Workflow
=============================

Below is a flowchart describing a typical project initiation workflow when using the Small Animal Imaging Core data acquisition process:

.. mermaid::

   graph TD
       A[Patient Registration & Scheduling] --> B[Screening for Contraindications]
       B --> C[Patient Preparation & Consent]
       C --> D[Patient Positioning]
       D --> E[Localizer/Scout Scans]
       E --> F[Pulse Sequence Selection]
       F --> G[MRI Data Acquisition]
       G --> H[Image Reconstruction]
       H --> I[Quality Control & Post-Processing]
       I --> J[Diagnostic Interpretation]
       J --> K[Reporting & Archiving]

