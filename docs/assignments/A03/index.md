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





  




  



## Decide


## Communicate

