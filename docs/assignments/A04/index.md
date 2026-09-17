# A4 – [Motor Mount]

## Objective

The objective for A4 is to design a motor mount that is capable of supporting a given motor with a load applied to the shaft. Per assigned specifications there can be no more deflection than 0.3mm in the mount.

<img width="164" height="149" alt="A4 force" src="https://github.com/user-attachments/assets/e0b5c34e-317c-4978-982c-6005b94ad61a" />

The design consists of two features, the first focuses on the flange mounting of the motor, the design is focused on sufficient strength or stiffness to support the described load of 300N.
The second feature focuses on the attachment to wall A focusing on sufficient strength or stiffness to support the motor and load.

The assigned factor of safety of 3 was specified in the assignment.


## Analyze

## Decide
### Material Selection

The first step taken was to select a material for the motor mount. 
The options given were ABS, PETG, and PLA plastics.
ABS plastic was chosen for its mechanical strength and chemical stability.
The Youngs Modulus of ABS was found to be 1.6-2.4 GPa and the yield strength was found to be 29.6-48 MPa.
To allow for maximum safety, the lowest values were used for all dimensional calculations.
(see link in Appendices for material data reference)

### Motor Details

The motor for which the mount is designed is designated PA28-28245800.
It features a bolt circle for flange mounting consisting of 4 M3 bolt holes on a 22mm bolt hole circle

<img width="1343" height="953" alt="Motor Drawing" src="https://github.com/user-attachments/assets/718d1047-753b-40e6-bcf3-7b5e6943b4dc" />

### Feature one FBD and SMD
The next step in the design process was to draw up a free body and shear-moment diagram for the section of the mount that motor will attach to at the flange. The maximum moment imparted by the load was found to be 5.43Nm

<img width="905" height="911" alt="Feature 1 FBD and SMD" src="https://github.com/user-attachments/assets/7d172ad2-4b1f-4b55-9bcc-2aa6c82dc7a9" />

The next step is to calculate the polar moment of inertia needed to keep deflection within its allowable parameters.
This led to the first (but not last) design reflection. 

#### Design Reflection 1 (Determining Length and motor body clearance)
The motor mount can deflect as much as 0.3mm in operation, therefor there must be sufficient clearance between the body of the motor and the wall attachment of the mount to avoid interference. 
Using some basic trigonometry the Length from the wall mount surface to the shaft was 15.605mm. This allows 2mm of clearance in addition to the maximum deflection at the ODE (opposite drive end) of the motor/gearbox housing at its maximum length of 75.6mm.
It was also decided to give 5mm of material to each side of the motor body (on all sides facing free space).
This set the the width of the mount a 38mm. 
For future calculations the served as the base dimension for the beam cross-section area for both features.

Using this as the beam length, Feature one was calculated as a cantilever beam, fixed at the surface of the wall mount opposite wall A.

<img width="912" height="909" alt="F1 Beam Calculations" src="https://github.com/user-attachments/assets/721859a3-3449-4323-8d9c-7cd9e65dca85" />

### F1 Calculated Cross section
Using the beam tables found in and around page 254 of Machinery's Handbook, The deflection of a beam with a singular moment load.












## Communicate

