SAI Study Scheduling
####################

Study General Workflow
**********************
The following outlines the general workflow for initiating a standard study using the SAI Core.

.. mermaid::

  graph TD
    %% Styles
    classDef white fill=#ffffff,stroke=#000000,color=#000;
    classDef green fill=#eaf4e0,stroke=#436f29,color=#000;
    classDef yellow fill=#fceec0,stroke=#c58e00,color=#000;
    classDef blue fill=#e4f1fb,stroke=#0367a6,color=#000;
    classDef orange fill=#ffe5d5,stroke=#d46900,color=#000;
    classDef dashed stroke-dasharray 5 5;

    %% Nodes
    A["Initial Consultation"]
    B["Ex vivo\nBiological sample\nMaterial science"]
    C["In vivo"]

    D["Project feasibility?"]
    E["Staff-Assisted imaging"]
    F["Project request submission"]
    G["SOPs signature"]
    H["Calendar invitation"]
    I["Data acquisition with Maylis"]
    J["Data transfer to SAI folder"]
    K["Data analysis"]

    L["Project feasibility?"]
    M["Vivarium access?"]
    N["IACUC/IBC approved?"]
    O["Animals ready?"]
    P["User-Operated imaging"]
    Q["Project request submission"]
    R["Schedule training with Maylis"]
    S["Training attendance form"]
    T["SOPs/RAs signature"]
    U["Access to equipment booking"]
    V["Data acquisition by user"]
    W["Data transfer to SAI folder"]
    X["Data analysis"]

    %% Flow
    A --> B
    A --> C

    B --> D
    D --> E
    E --> F --> G --> H --> I --> J --> K

    C --> L --> M --> N --> O --> P
    P --> Q --> R --> S --> T --> U --> V --> W --> X

    %% Styling
    class A white
    class B green
    class D,F,G,H,I,J,K yellow
    class E yellow
    class C,L,M,N,O blue
    class P,Q,R,S,T,U,V,W,X orange
    class H,I,J,K dashed
    class V,W,X dashed


Study initiation
****************
Initial consultation
====================
To initiate a research project utilizing equipment from the SAI Core, please contact maylis.boitet@nyu.edu to arrange an
initial consultation and assess project feasibility. The email should include a concise project description and specify
the imaging resource intended for use.

Project registration
====================
Upon completion of the consultation, please submit the online project registration form https://forms.gle/d3xRyphopVUj6PwW6.
You will then receive an email containing the relevant Standard Operating Procedures (SOPs) for SAI operations, imaging
procedures, and material transfer. These documents must be reviewed and signed during your initial imaging session or training.


Training and scheduling
***********************
The SAI Core offers both user-operated and staff-assisted imaging services, depending on the type of equipment and the
specific requirements of the study.

User-operated imaging
=====================
Equipment training
-------------------
Users are required to schedule a training session with Maylis Boitet, which will cover equipment utilization, including
a technology overview, data acquisition and analysis procedures, and emergency shutdown protocols. Upon completion of the
training, users must submit the training attendance request form
https://docs.google.com/forms/d/e/1FAIpQLScLW1MOvo-9aAwX2_04FcyLGPR9xtDso9hu9SEixUy2VzuAiw/viewform.
Once the completed attendance sheet is received, the corresponding Standard Operating Procedures (SOPs) and Risk Assessments (RAs)
for equipment use will be shared and must be thoroughly reviewed and signed by the registered individual.
Strict adherence to the SOPs is mandatory when operating the equipment to ensure the safety and security of both the
operator and the animal during imaging sessions.

Equipment scheduling
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

SAI room access
===============
All users who require access to the SAI room must have prior access to the vivarium as well as an approved IACUC protocol
for live animal imaging.

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


Scheduling policies
*******************
Equipment booking
=================
Use of any SAI resource must be scheduled in advance through the designated booking system. Users are encouraged to reserve
their imaging timeslots at least one week ahead of time. For staff-assisted imaging, a minimum notice of 24 hours is required,
while user-operated sessions must be booked with at least 4 hours notice. Short-notice bookings should be avoided to ensure proper
planning and support. When reserving equipment, please account for warm-up time and cleaning procedures to ensure optimal
performance and adherence to safety protocols.

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

Radiation safety certificate
============================
Researchers seeking access to the microCT scanner must submit a valid Radiation Safety Certificate and comply with the
NYUAD Radiation Safety Program.
The online Radiation Safety Training can be accessed at: https://moodle.abudhabi.nyu.edu/course/view.php?id=72.















