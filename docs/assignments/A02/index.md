
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

Next came everyone's favorite part of engineering, the long beloved and oft maligned "plug-and-chug".
Inputting the known values for P, a, b, and the derived d, the forces were calculated.
The truss members BD and AC were in tension of magnitude 41.67 kN and the truss members BA and DC were in compression of magnitude 33.3 kN.

<img width="790" height="230" alt="force_calculations" src="https://github.com/user-attachments/assets/64b9480b-bcc8-4f9e-a283-47f3ab8d830a" />

### Truss Stress Analysis

The next step in the design was to calculate the cross sectional area required 










## Decide
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate

