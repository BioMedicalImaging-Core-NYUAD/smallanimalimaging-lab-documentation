SAI Study Scheduling
####################

Study General Workflow
**********************
The following outlines the general workflow for initiating a standard study using the SAI Core.

.. mermaid::

   graph TD
    A[Project presentation to Maylis]

    %% Ex vivo branch
    A --> B1[Ex vivo<br>Biological sample<br>Material science]
    B1 --> C1{Project feasibility?}
    C1 --> D1[SkyScan 1276]
    C1 --> D2[IVIS Spectrum]

    %% SkyScan 1276
    D1 --> E1{Radiation safety certificate?}
    E1 --> F1[Project request submission]
    F1 --> G1[SOPs signature]
    G1 --> H1[Calendar invitation]
    H1 --> I1[Data acquisition with Maylis]
    I1 --> J1[Data transfer to SAI folder]
    J1 --> K1[Data analysis]

    %% IVIS Spectrum shares the same flow after Radiation Cert
    D2 --> E1

    %% In vivo branch
    A --> B2[In vivo]
    B2 --> C2{Project feasibility?}
    C2 --> D3{Vivarium access?}
    D3 --> E2{IACUC approved?}
    E2 --> F2{Animals ready?}
    F2 --> G2[KS Endoscope]
    F2 --> G3[nVue-nVision]

    %% KS Endoscope flow
    G2 --> H2[Project request submission]
    H2 --> I2[Schedule training with Maylis]
    I2 --> J2[Training attendance sheet]
    J2 --> K2[SOPs/RAs signature]
    K2 --> L2[Access to equipment booking]
    L2 --> M2[Data acquisition by user]
    M2 --> N2[Data transfer to SAI folder]
    N2 --> O2[Data analysis]

    %% nVue-nVision shares the same flow
    G3 --> H2

    %% Styling
    style A fill:#ffffff,stroke:#000,stroke-width:2px
    style B1 fill:#d6eadf,stroke:#2c662d,stroke-width:2px
    style B2 fill:#d0e7f7,stroke:#005792,stroke-width:2px

    style D1 fill:#fff2cc,stroke:#d89b00
    style D2 fill:#fff2cc,stroke:#d89b00
    style G2 fill:#fdecdc,stroke:#ff5722
    style G3 fill:#fdecdc,stroke:#ff5722


Study Initiation
****************
Initial Consultation
====================
To initiate a research project utilizing equipment from the SAI Core, please contact maylis.boitet@nyu.edu to arrange an
initial consultation and assess project feasibility. The email should include a concise project description and specify
the imaging resource intended for use.

Project Registration
====================
Upon completion of the consultation, please submit the online project registration form (LINK) along with all required supporting documentation.
You will receive an email containing the relevant Standard Operating Procedures (SOPs) for SAI operations, imaging procedures, and material transfer.
These documents must be reviewed and signed during your initial imaging session or training.


Training and Scheduling
***********************
The SAI Core offers both user-operated and staff-assisted imaging services, depending on the type of equipment and the
specific requirements of the study.

User-Operated Imaging
=====================
Equipment Training
-------------------
Users are required to schedule a training session with Maylis Boitet, which will cover equipment utilization, including
a technology overview, data acquisition and analysis procedures, and emergency shutdown protocols. Upon completion of the
training, users must submit the training attendance request form
https://docs.google.com/forms/d/e/1FAIpQLScLW1MOvo-9aAwX2_04FcyLGPR9xtDso9hu9SEixUy2VzuAiw/viewform.
Once the completed attendance sheet is received, the corresponding Standard Operating Procedures (SOPs) and Risk Assessments (RAs)
for equipment use will be shared and must be thoroughly reviewed and signed by the registered individual.
Strict adherence to the SOPs is mandatory when operating the equipment to ensure the safety and security of both the
operator and the animal during imaging sessions.

Equipment Scheduling
--------------------
Once all the required documentation is signed and provided, users will be granted access to the booking system to schedule
their imaging sessions https://corelabs.abudhabi.nyu.edu/.
SAI resources can be accessed through the "Reservations" or "Schedule" sections, as well as from the upper drop-down menu
under "Brain Imaging." Prior to using any equipment, users must schedule their session through the CTP booking system and
adhere to the SAI scheduling policies.

Staff-assisted imaging
======================
When staff assistance is required for an imaging study, please send a Google Calendar invitation to maylis.boitet@nyu.edu,
ensuring that your name and the imaging modality are clearly stated in the subject line.
Before submitting the request, verify the availability of the required resource using the booking system https://corelabs.abudhabi.nyu.edu/.

SAI Room access
===============
All users who require access to the SAI room must have prior access to the vivarium as well as an approved IACUC protocol for live animal imaging.

Daily equipment scheduling strategy
===================================
The NYUAD vivarium houses animals with varying health statuses, including Specific Pathogen-Free (SPF), conventional, and
biohazard categories. To minimize the risk of cross-contamination and maintain the health status integrity of the husbandry
environment, an equipment scheduling strategy has been implemented. This strategy prioritizes sample cleanliness and reduces
contamination risk by adhering to a defined daily imaging order.

Daily Imaging Order (from lowest to highest contamination risk):

    - SPF vivarium animals or biological samples
    - Conventional vivarium animals or biological samples
    - Biohazard vivarium animals or biological samples
    - External samples (fixed biological specimens, materials science samples)

Adherence to this imaging sequence is mandatory to ensure biosafety and preserve the health classification of vivarium environments.


Scheduling Policies
*******************
Equipment booking
=================
Use of any SAI resource must be scheduled in advance through the designated booking system. Users are encouraged to reserve
their imaging timeslots at least one week ahead of time. For staff-assisted imaging, a minimum notice of 24 hours is required,
while user-operated sessions must be booked with at least 4 hours notice. Short-notice bookings should be avoided to ensure proper planning and support.
When reserving equipment, please account for warm-up time and cleaning procedures to ensure optimal performance and adherence to safety protocols.

Cancellation
============
Users must cancel any scheduled imaging sessions as early as possible to allow reallocation of resources. Cancellations
should be made at least 24 hours in advance through the CTP booking system. Repeated last-minute cancellations or no-shows
may result in temporary suspension of booking privileges. Please notify core staff immediately in the event of unavoidable
delays or emergencies.


Required documentation
**********************
All research projects must obtain the requisite regulatory approvals and certifications prior to initiation.

Animal protocol (IACUC)
=======================
All live animal imaging studies must receive prior approval from the Institutional Animal Care and Use Committee (IACUC).
If your study involves in vivo imaging, it is recommended that you amend your existing IACUC protocol as early as possible
to ensure compliance and avoid delays.
The SAI Core maintains an approved IACUC protocol encompassing standard imaging procedures, which may be utilized
to initiate small pilot studies, provided the proposed procedure falls within the scope of this core protocol.

For assistance with incorporating live animal imaging into your IACUC-approved protocol, please contact Dr. Maylis Boitet. For
inquiries related to IACUC protocol submission or regulatory matters, please reach out to William Pressley wd1@nyu.edu.

Biosafety protocol (IBC)
========================
All research involving the use of hazardous materials, including tumor cell lines and adeno-associated viral (AAV) vectors,
must obtain prior approval from the Institutional Biosafety Committee (IBC) before initiation.

For any assistance, please contact Mir Hussain Nawaz hussain@nyu.edu.

Radiation Safety Certificate
============================
Researchers seeking access to the microCT scanner must submit a valid Radiation Safety Certificate and comply with the
NYUAD Radiation Safety Program.
The online Radiation Safety Training can be accessed at: https://moodle.abudhabi.nyu.edu/course/view.php?id=72.















