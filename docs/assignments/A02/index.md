
# A2 – Truss Stress Analysis

## Objective
The objective for assignment 2 is to design a truss assembly that meets the following requirements.

1) Lightweight (minimum material usage) truss made of ASTM A500 steel or similar
2) Size to meet factors of safety given (3.5 for truss members and 4 for truss pins)
3) All truss members must have the same cross sections

This was achieved by hand sketching Free Body Diagrams, calculating cross-section area for pins and trusses and, using CAD software to design and model the proposed structure.

The weights of the truss and the corresponding pins was calculated by hand and verified in the CAD software

The failure modes of the truss structure and pins was also identified with design revisions proposed to mitigate risk.



## Analyze

### Truss Force Analysis

The first step was to analyze the assigned structure:

<img width="437" height="208" alt="Given structure geometry" src="https://github.com/user-attachments/assets/b99f1507-8163-4873-aff5-ab559ce106fe" />

The support at point B is to be a vertically supporting roller support, The support at point A is a Pin Support.
This means that there will be reaction forces in the X and Y directions for support A but only reaction forces in the Y direction at support B.
The following value were assigned:

a = 0.4m

b = 0.3m

P = 20 - 30 kN

A value of 25kN was selected for this assignment.

The first calculation was to find the length of the diagonal truss members via the Pythagorean theorem.

<img width="342" height="109" alt="pythag" src="https://github.com/user-attachments/assets/953f5448-0014-43b7-b96a-71a99685d333" />


In order to begin analyzing the reaction forces and the resulting internal forces of the truss, a free body diagram was drawn. The symbolic values for the internal forces for members BA, DC, BD, and AC were calculated using the sum of forces in the X and Y directions. It was discovered that because there is no X reaction force at B, there won't be any reaction force in X at point A.  This means the structure is symmetrical and, internal force BD will be equal to AC.

<img width="907" height="619" alt="FBD" src="https://github.com/user-attachments/assets/628c13ec-b8f5-44bc-b6ea-cefec7992b2b" />

By calculating these forces it was noted that the downward force of P induces tension into diagonal members BD and AC and compression in members AB and DC.

### Truss Force Calculations

Next came everyone's favorite part of engineering, the long beloved and oft maligned " plug-and-chug™ ".
Inputting the known values for P, a, b, and the derived d, the forces were calculated.
The truss members BD and AC were in tension of magnitude 41.67 kN and the truss members BA and DC were in compression of magnitude 33.3 kN.

<img width="790" height="230" alt="force_calculations" src="https://github.com/user-attachments/assets/64b9480b-bcc8-4f9e-a283-47f3ab8d830a" />

### Truss Stress Analysis

The next step in the design was to calculate the cross sectional area required.
In order to achieve this step, outside information were required.
Research was done in order to find the yield stress of ASTM A500 steel.
source : Alliance Tubular Products:
https://www.alliancetubularproducts.net/resources/blog/applications-and-advantages-of-astm-a-500-structural-tubing/
The yield stress for ASTM A500 Grade B steel was found to be greater than or equal to 315 MPa
(The decision to use grade B will be further discussed under the "Decide" header)


Using the equation for axial stress ( σ = F / A ) and solving for A, ( A = F / σ) then applying the saftey factor, the equation to find the cross sectional area were derived upon:

( A = 3.5F / σ ).

<img width="918" height="369" alt="SymbolicStressT" src="https://github.com/user-attachments/assets/c4357b32-c74e-4204-b1e0-db7dc7f89bc7" />

### Truss Stress Calculation
Applying the tried, true, red-white-and-blue, back-bending, world-ending, foul smelling and, patent-pending method of " plug-and-chug™ "
the known vales for yield stress(σ), maximum force(F) (Tension at BD/AC), and the prescribed factor of safety of 3.5; the cross sectional area was found to be 0.00046296 square meters.

<img width="770" height="327" alt="StressCalculationT" src="https://github.com/user-attachments/assets/c8b0e359-a8d4-4280-8588-28951c95b638" />

For purposes that will become all too clear in the very near future, the units were converted into square inches (0.718 in sq.)

### Pin Shear Force Analysis
In order to find the applicable cross-section area for the pins that will hold our truss together at points A,B,C and, D, a free body diagram was revisited upon point B (with great vengance and furious anger)

<img width="875" height="633" alt="FBDP" src="https://github.com/user-attachments/assets/4d78f8f0-3698-4f16-baff-c970d1edd613" />

Initially the value of V (shear force on the Pin) was thought to be equivalent to the tension force of the truss element.
This thought was burned as a heretic and it family name was stricken from the record.
Further analysis yielded a formula for the magnitude of the shear force on the pin (V)
Using the formula for shear stress ( τ = V/A ) and solving for A results in an equation for the cross section area of the pin
Applying the given safety factor of 4, the equation becomes:

( Apin = 4V/τ)

<img width="284" height="154" alt="SymbolicShearP" src="https://github.com/user-attachments/assets/c58d4b52-905b-420e-9d56-7333b27c8b0f" />

### Pin Shear Force Calculation
The material to be used for the pin was given in the assignment detail:

<img width="593" height="87" alt="GivenPinParameters" src="https://github.com/user-attachments/assets/fb479911-c29b-4942-a0bd-1a6c66b14788" />

given the necessary parameters for yield shear stress (τ), using the formula to calculate the shear force (V) and, applying the given safety factor of 4.
The cross section of the pin was calculated " plug-and-chug™ ":

The units given were in imperial units and were thusly converted into metric. 
Also, for designing the pin it was necessary to calculate the diameter from the calculated area.

<img width="891" height="457" alt="ShearCalculationP" src="https://github.com/user-attachments/assets/4460e2a8-2e5e-4144-8879-ad1e36feff57" />

The necessary diameter of the pin was found to be 14.356mm which was rounded up to 14.5mm.
It is somewhat close to 9/16" so if metric material is not readily available, 9/16" dia. pin material can easily be substituted.

### Weights

Searching the internet for the density of ASTM A500 grade B steel yielded a result of 0.305 lbs / cubic in.

source:
https://en.wikipedia.org/wiki/ASTM_A500

Applying the lengths from the given geometry and multiplying by the cross sectional area provided the volume of the truss.
Multiplying the Volume of the truss by the density, an approximate weight was estimated at 29.55 lbs

<img width="845" height="617" alt="TrussWeight" src="https://github.com/user-attachments/assets/e1426d73-c568-4c3f-aac8-389aba8e4e9d" />

For the Pins, the density was given to be 7695 kg / cubic meter.
The pins were designed at 4 inches long
Using the same method  of Area * Length * Density the weight of a single pin is calculated in kg.
There are 4 pins in the truss so the wight is multiplied by 4, then multiplied by a conversion factor of 2.2 (lb/kg) to approximate the weight of the pins at about 1.114 lbs

<img width="859" height="896" alt="PinWeight" src="https://github.com/user-attachments/assets/66315319-52bd-489e-bce1-1a92e2915b1d" />


## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

All research into ASTM A500 steel led to the conclusion that it is generally used in America and is sold almost exclusively in Freedom Units (inches and lbs).
Scouring the internet for suppliers, that sold tubular sections (only ship builders sell it in plates, and nobody want's to deal with maritime people).
This was the primary factor in the decision to construct the truss members from square tubing.
The challenge then became to find a tubular section that closely matched the calculated cross section area.
The best match found online was from alliance tubular products:

https://www.alliancetubularproducts.net/assets/files/atp-line-cards-2026-june.pdf

They have square tubing in ASTM A500 grade b that is 2" by 2" square OD and 0.095 (13 ga) wall thicness.
This provides a cross section area of 0.7239 sq. in.
For those of you keeping score at home, that only exceeds our nominal cross section area by 0.88%

<img width="869" height="311" alt="Material Selection" src="https://github.com/user-attachments/assets/3fe1c39d-ac9f-4b2a-9492-fdc81a2248bf" />

Given the assignment directive of "keep it simple", a side by side joint configuration was chosen for the model.
This also allows the truss members to maintain their cross section area throughout their respective spans
Autodesk Fusion was used for 3d modelling of the truss and pins.

<img width="712" height="550" alt="Model_ISO" src="https://github.com/user-attachments/assets/2d67675c-6e1d-46bd-9ccd-e05a5177e5ba" />

<img width="424" height="557" alt="Model Right" src="https://github.com/user-attachments/assets/c2f3349a-3b7d-4e95-9be6-03da9151e910" />

<img width="1033" height="411" alt="Model Front" src="https://github.com/user-attachments/assets/8e001606-fc67-4c5a-9b76-7dd3c7fdc4d8" />

In order to maintain adequate support all around the pin, some length must be added to the truss members.
This resulted in some added weight from the earlier approximation.

<img width="793" height="635" alt="Model Weight" src="https://github.com/user-attachments/assets/e3065d30-b773-44cd-8406-20e90fc5357f" />

This discrepancy is minor however (29.799 model vs 29.5544 calculated , overage of 0.84%).

Models Can be downloaded here

[TRUSS (STEP)](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A02/A2TRUSS.step)




## Communicate

### Failure Modes (Truss)

Given that the greatest force experience by the truss is tensile, the most likely failure mode should be yielding.
If the primary force was compression then some buckling could be anticipated.
Fracturing in this case is unlikely unless the truss is subject to an excessively corrosive environment that could seriously weaken the structure.
An internet search for the ductility characteristic of ASTM A500 grade B found the website metalzenith.com

https://metalzenith.com/blogs/steel-properties/a500-steel-properties-and-key-applications-in-construction

which describes the material as having "good ductility" so it is safe to classify the material as more ductile than brittle.
This is typically true of low carbon structural steels.

One modification to mitigate yield failure is to thicken the walls of the tube. While costing some weight, this would reduce the axial stress on the truss members.

### Failure Modes (Pins)

The pins on the other hand are hardened and are in fact more brittle than ductile.
A research paper in International Journal of Civil and Structural Engineering Research (ISSN 2348-7607) was found at
researchpublish.com

https://www.researchpublish.com/upload/book/FATIGUE%20ANALYSIS%20OF%20TRUSS-2169.pdf

The article from 2015 by J B Geetha Shree at the East Point College of Engineering and Technology, Bangalore India (Titled Fatigue Analysis of Truss) indicates that "joint failure in steel structure is generally due to bolt failure". 
The paper describes how cyclic loading and un-loading cause small cracks which propagate stress concentrations through the material.
This will eventually lead to shearing fracture and the failure of the truss at the joint.
One design change to mitigate this failure mode would be to develop an assembly to put the pins in a 2 plane shear configuration. This would cut the net shear stress in half.

