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
 
  plugging in our known values and solving for L left us with a maximum length of 35.370 in

  <img width="861" height="258" alt="L numcalc" src="https://github.com/user-attachments/assets/7ca676bb-c830-4cd4-8685-e874fac4c84b" />

  ## Model
  With some calculations done and formulae in hand, confidences were nearing an all time high...

  Then we opened solidworks


## Decide


## Communicate

