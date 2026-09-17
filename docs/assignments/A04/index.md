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

## Design Feature 1 (Flange Attachment)

### Feature one FBD and SMD
The next step in the design process was to draw up a free body and shear-moment diagram for the section of the mount that motor will attach to at the flange. The maximum moment imparted by the load was found to be 5.43Nm

<img width="905" height="911" alt="Feature 1 FBD and SMD" src="https://github.com/user-attachments/assets/7d172ad2-4b1f-4b55-9bcc-2aa6c82dc7a9" />

The next step is to calculate the polar moment of inertia needed to keep deflection within its allowable parameters.
This led to the first (but not last) design reflection. 

#### Design Consideratoin 1 (Determining Length and motor body clearance)
The motor mount can deflect as much as 0.3mm in operation, therefor there must be sufficient clearance between the body of the motor and the wall attachment of the mount to avoid interference. 
Using some basic trigonometry the Length from the wall mount surface to the shaft was 15.605mm. This allows 2mm of clearance in addition to the maximum deflection at the ODE (opposite drive end) of the motor/gearbox housing at its maximum length of 75.6mm.



Using this as the beam length, Feature one was calculated as a cantilever beam, fixed at the surface of the wall mount opposite wall A.

#### F1 Beam Calculations (Symbolic)
<img width="912" height="909" alt="F1 Beam Calculations" src="https://github.com/user-attachments/assets/721859a3-3449-4323-8d9c-7cd9e65dca85" />


### F1 Calculated Cross section
Using the beam tables found in and around page 254 of Machinery's Handbook, The deflection of a beam with a singular moment load.
It should be noted that the original Length of 15.605 was calculated for the deflection allowed but, for safety, it was increased to account for the full specified deflection (redundant safety factors)
The L used for calculations was 16.1mm.
With M, E, and v allowed known, the calculation for I (polar moment of inertia) was made (refer to F1 Beam Calculations for symbolic solutions)

#### F1 Beam Calculations (Numeric)

<img width="741" height="947" alt="F1 Beam Calculations N" src="https://github.com/user-attachments/assets/f8640ff3-0fbc-46b0-81e2-5826d873815d" />

#### Design Consideration 2 (whas my b be... b?)
It was decided to give 5mm of material to each side of the motor body (on all sides facing free space).
This set the the width of the mount a 38mm.
For future calculations the served as the base dimension for the beam cross-section area for both features.

With I calculated and b known, the critical thickness of the beam was calculated for stiffness.
It was found to be close to 11.25mm.

### Now for the Strengths

Calculations for the critical thickness of the Feature 1 with regards to strength were then made

#### F1 Beam Calculations (for strength)

<img width="702" height="897" alt="F1 Beam Calc Stremf" src="https://github.com/user-attachments/assets/56f03f33-c571-4286-af1e-3db00f9f6c34" />

The critical thickness of the beam with regards to strength was calculated to be around 9.32mm

The larger of the two was chosen for more safety in the design.

## Design Feature 2 (Wall attachment)

The process for Feature two was performed in a similar sequence to design feature 1.

The first step was sketching diagrams (FBD and SMD).
This led to the next design consideration.

#### Design consideration 3 (How long am it really necessary to be?)
Simply for the thrill of it, the length of the wall attachment feature was set at 75.6mm ( the entire length of the motor body).

#### Feature 2 Diagrams

<img width="609" height="807" alt="F2 Diagrams" src="https://github.com/user-attachments/assets/38f03cb5-4cd5-48ba-9b55-8d5699942f50" />

### Feature 2 Calculations

Using the same procedure as F1 the moment of inertia (I) was calculated.
(see Feature 2 Diagrams for Symbolic calculations)

#### Feature 2 Numerical Calculations

<img width="647" height="493" alt="F2 Numerical Calculations" src="https://github.com/user-attachments/assets/8353ffb2-3a3d-46c6-99c4-a29e1fcad147" />

The critical thickness for Feature 2 was found to be over 50mm.
This seemed excessive so the design consideration for length was revisited.
Because Feature 2 is bolted to the wall, the beam length was revised to the length from the last bolt position to the end surface of Feature 1.
For optimal load distribution, the spacing of a 4 bolt square pattern was spaced to cut the span length of the Feature 2 length into even thirds.
This left the "beam length" of feature 2 at about 25mm.

#### Feature 2 Revisited

<img width="616" height="551" alt="The Revisiting" src="https://github.com/user-attachments/assets/2d6e2c63-5337-4162-ba12-851f00130b39" />

With the new parameter for L established, the critical thickness of Feature 2 was re-calculated at 11mm with respect to strength and 17mm with respect to stiffness.
Using the same logic as Feature 1, the larger of the two was carried through to the design.

## Communicate (Let's get digital)

Before digging into the Solidworks, an Isometric sketch was done by hand.
Just for laughs I suppose.

#### Isometric hand sketch

[A4 iso hand sketch.pdf](https://github.com/user-attachments/files/32318540/A4.iso.hand.sketch.pdf)

<img width="838" height="841" alt="iso handy" src="https://github.com/user-attachments/assets/3e898c98-280c-4b7c-a26f-aa76c81a5bc2" />

### If it's solid, it works

[A4 Motor Mount Solid Model](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A04/A4.SLDPRT)

[A4 Motor Mount Drawing PDF](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A04/A4_Austin_Hill.pdf)








