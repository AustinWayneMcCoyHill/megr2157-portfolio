# A3 – Parametric and FEA Modeling

## Objective
The objective is to gain experience in designing for a given factor (design for x), using parametric and FEA (finite element analysis tools.
Given the following constraints:

    Circular cross section
    
    Aluminum material with Modulus of Elasticity between 8.5 and 11.5 mega-psi
    
    Bar subjected to only axial tension
    
    Tensile force to be between 350 and 500 lbs
    
    Chosen cross sectional area
  
    The maximum length of the bar is to be determined by the software by way of equations input into 3d Modeling (CAD) software

## Analyze
Before jumping into the software, some hand calculations were completed using the following formula from p218 of Machinery's Handbook


### Hand Calculations

  (17) e = FL/AE (from handbook)
  where
  
  e = elongation (deflection)
  
  F = axial force

  L = part length

  A = cross sectional area

  E = modulus of elasticity

  solving for L, we find that L = (e * A * E) / F
  
  <img width="814" height="183" alt="L Hand Calc" src="https://github.com/user-attachments/assets/73cf4f48-e537-4ec0-bea3-09cdcba91568" />

  NOTE: to make parametric design simpler (pi/4)*d^2 is substituted for A

### Numerical Calculation
  
  Choosing 6061 - T6 Aluminum (Common, relatively cheap, strong enough), give a Modulus of elasticity of 10.007604E6 which is well with constraints.
  
  A diameter of 0.5 in was selected making the cross-sectional area (A) 0.1964 sq in

  as well as the largest allowable force of 500 lb.
 
  plugging in our known values and solving for L left us with a maximum length of 35.370 in

  <img width="861" height="258" alt="L numcalc" src="https://github.com/user-attachments/assets/7ca676bb-c830-4cd4-8685-e874fac4c84b" />

## Model
  With some calculations done and formulae in hand, confidences were nearing an all time high...

  Then we opened Solidworks™

### Setting parameters and material

  Material was configured,
  
  <img width="856" height="623" alt="Material Tab" src="https://github.com/user-attachments/assets/e0325571-f1d3-4fb1-ab78-bcbfc64e1cda" />

  and formulae were formulated in the formula tab.

  <img width="1230" height="562" alt="Screenshot 2026-09-09 220615" src="https://github.com/user-attachments/assets/404c8c4d-4cc9-4c65-8147-596b8cc2da1c" />

  When designing by parameter you can input the paramter directly into a dimension as long as it is in quotation marks (ie. "length" or "diameter").

  It will still populate as the numerical value but with little globe symbol beside it (indicating a global variable)

  <img width="242" height="496" alt="lenf" src="https://github.com/user-attachments/assets/85184e41-a01c-4aa9-a1ae-406b82da5d09" />

  <img width="594" height="478" alt="diameter" src="https://github.com/user-attachments/assets/04dd8e8a-5013-43b6-becd-b0cfc7d2e49e" />

### Model Link
[A3 bar (sldprt)](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A03/A3.SLDPRT)

### The finest of element analysis

  Solidworks makes the FEA segment somewhat trivial.
  
  Using the highest resolution mesh,

  <img width="1103" height="613" alt="mesh" src="https://github.com/user-attachments/assets/e64b54a1-000d-44c3-96c8-20dbf94151e4" />

  setting a fixed face,

  <img width="639" height="465" alt="Fix at Face" src="https://github.com/user-attachments/assets/d3741a0c-9dee-4219-85a8-e87844007812" />

  and setting a normal face for the 500lb force, the simulation is ready to run.

  <img width="562" height="466" alt="use teh forse" src="https://github.com/user-attachments/assets/d94ff719-630e-4803-ad08-d016805c5810" />

## FEA results

### vonMises 

<img width="1689" height="873" alt="A3-Static 2-Stress-Stress1" src="https://github.com/user-attachments/assets/029f142e-c6ca-47cc-97e0-80237c9b650c" />

### displacement

<img width="1689" height="873" alt="A3-Static 2-Displacement-Displacement1" src="https://github.com/user-attachments/assets/cd1158c9-a78f-49dd-a8f7-7138d9b0cbed" />

### strain

<img width="1689" height="873" alt="A3-Static 2-Strain-Strain1" src="https://github.com/user-attachments/assets/908b2040-73f2-4d66-acc3-5eb9a0f9c531" />
### Safety factor
The maximum stress from the von Mises stress map is 2.942 ksi.

This represents a safety factor of just about 13.5 (Yield strength / max stress)

#### "But what if we put a hole in it?"

First of all .... don't.... but if you have to it's probably fine.

According to what I could find on Kt factor for a transverse hole in a bar under uniaxial tension

(https://mechcodex.com/learn/strength-of-materials/stress-concentration)

The stress at the edge of the hole perpendicular to the line of force is 3 times the stress at the edge of the hole along the line of force.

<img width="842" height="292" alt="mechcodex" src="https://github.com/user-attachments/assets/8b3b818a-88c0-47c6-99d0-1513b23a5b84" />


If we consider the hole to be situated where the stress is highest on the bar (2.942 ksi) and triple that the maximum stress becomes 8.826 ksi.

This would drop the safety factor from 13.5 to 4.5 but would still be acceptable.

## Modifying Design Parameters - Predictions

### Changing Area or Load
Changing any of the geometric parameters will have an effect on the length per the earlier equation:

L = (e * A * E) / F

This equation is linear so adjusting cross-sectional area (A) will be directly proportional, and adjusting load (F) will be inversely proportional. 


### Modifying diameter
Given that the cross-section is circular and solid, the only geometric property to adjust for area will be the diameter. Because the formula for Area of the cross section involves squaring the diameter, adjustments to the diameter will have a quadratic effect on the length (double the diameter and the length goes up by a factor of four).

### Modifications Results
Doubling Diameter:

Prediction: Length will quadruple from 35.37in to 141.47

Result: The parametric formulae and FEA simulation both show the prediction to be true

<img width="219" height="181" alt="diaModEqRes" src="https://github.com/user-attachments/assets/bb11326f-c17a-4c15-8326-8ae20675e04d" />

<img width="1407" height="638" alt="modDiaDisp" src="https://github.com/user-attachments/assets/9dbe2269-b555-4e1d-8852-d9f6b79920c6" />

Dropping load from 500 to 300 lbf (diameter returned to original 0.5in):

Prediction:  Length will increase by factor of (F original  / F new) = (5/3) because the length is inversly proportional to load (force go down, length go up)

Result: The parametric formulae and FEA simulation both show the prediction to be true

<img width="1199" height="522" alt="modFEq" src="https://github.com/user-attachments/assets/51be683a-0b01-4b40-8146-ba992f276b8c" />

<img width="1343" height="646" alt="modFDisp" src="https://github.com/user-attachments/assets/e0ea2777-8c6e-4f4a-a012-d2ac83662f13" />




## Conlusions

While the formulae are fairly straight forward in this instance, it is always surprising just how resilient metals are in tension. even a small cross section of aluminum only deflects by 0.0254% Length at 500 lbf.
Time spent: 4 hours

