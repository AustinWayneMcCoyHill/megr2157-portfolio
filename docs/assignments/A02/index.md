
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

### Pin Force Analysis
In order to find the applicable cross-section area for the pins that will hold our truss together at points A,B,C and, D, a free body diagram was revisited upon point B (with great vengance and furious anger)

<img width="875" height="633" alt="FBDP" src="https://github.com/user-attachments/assets/4d78f8f0-3698-4f16-baff-c970d1edd613" />

Initially the value of V (shear force on the Pin) was thought to be equivalent to the tension force of the truss element.
This thought was burned as a heretic and it family name was stricken from the record.



https://en.wikipedia.org/wiki/ASTM_A500









## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate

