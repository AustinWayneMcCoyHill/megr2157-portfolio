# A5 – [Bracket Design]

## Objective
The objective for A5 is to design a bracket used to support a load from a nylon web towing style strap.
The bracket needs to attach to a perscribed "t-bar" (Fig 1)

### Fig 1

<img width="417" height="313" alt="Fig 1" src="https://github.com/user-attachments/assets/9adb0ba9-b925-4480-8185-a4c13f5ee029" />


Three materials were given as viable options.
The internet were consulted for mechanical properties of all three

Material option 1 - 6061 T6 Aluminum

https://www.modulusmetal.com/aluminum-6061-t6-mechanical-properties/

Material option 2 - ASTM A36 Steel

https://langhe-industry.com/astm-a36-carbon-steel/

Material option 3 - ASTM Grade 5 Titanium

https://www.aerospacemetals.com/wp-content/uploads/2023/07/Titanium-Ti-6Al-4V-Grade-5-STA-Data-Sheet.pdf

The strap in question will support a load of 750lbs

https://www.uline.com/Product/Detail/S-12925/Poly-Cord-Strapping/Heavy-Duty-Polyester-Cord-Strapping-3-4-x-2500?pricode=WA9239&gadtype=pla&id=S-12925


## Analyze

### Feature A (business end)
Feature A will be where the strap meets the designed bracket.
A simple cylinder is assumed to suffice and we are resting comfortable in our assigned assurance that under direct shearing force, no part shall fail.
Per suggestion the forces and reactions were calculated as though the cylinder were a cantilever beam with the load distributed along the length of the strap.
For the first feature, calculations were conducted to find the minimum diameter for the cylinder in all three materials. 
The calculations were used to find the minimum diameter to keep the stress on the part inside the elastic limit (with a safety factor of 4) and, the minimum diameter to keep the deflection in the part less than the prescribed 0.005" limit for maximum deflection.
The free length of feature A was made just a little longer (0.050 in) than the width of the strap to accommodate for some shifting during use.

<img width="609" height="793" alt="Feature A" src="https://github.com/user-attachments/assets/d9434389-aba9-480d-8b3d-cab28432accc" />

## Decide
### Material Selection sidebar

At this point it was time to select a material.
Given the calculated diameters, it seemed like the Titanium was the strongest choice and could be made using the least quantity of materials.
This seemed like a good idea until the prices were inspected.
Per metal prices today, the titanium, even accounting for using less material, would still be ten times the cost of making the bracket from aluminum.

https://www.materialpricebook.com/prices

<img width="591" height="506" alt="cost comparison" src="https://github.com/user-attachments/assets/886a724e-7dfc-43b7-b30d-c0d5843e4750" />

For this reason, and maybe a few personal ones, Aluminum was chosen as the material for the bracket.
This concludes the sidebar.

## Analyze 2 (everyones favourite sequel)

### Feature B

Moving right along, Feature B was determined to be best approximated as a rectangular bar under axial load.
The process for calculating the minimum cross section for Feature B was similar to feature A with changes made to Section Modulus and Moment of Inertia because of the change in geometry.

<img width="603" height="742" alt="image" src="https://github.com/user-attachments/assets/69de1667-e470-4bda-bb99-3d4aba70325a" />

The length of feature B is left to our own designing. Just for a grand fancy, it was set at the material limit for the maximum material deformation.

### Feature C

Feature C was calculated as a supported beam with a point load equal to the reaction force in feature B.
The governing component was the stiffness, requiring a minimum thickness of 0.6446 in. to maintain deflection less than maximum vs 0.5428 in. for stress.
The depth of Feature C, along with the remaining features was designed as the sum of the free length of feature A and the thickness of feature B (0.9106 in.)

<img width="599" height="789" alt="Feature C1" src="https://github.com/user-attachments/assets/c47b938d-afc6-4837-874b-da26c2bdf164" />

<img width="362" height="379" alt="Feature C2" src="https://github.com/user-attachments/assets/5a96c53e-2b89-448d-9cdf-a5a01e460105" />

### Feature D

Feature D was calculated as a rectangular bar under axial load with magnitude equal to reaction force from feature C, this force was half of the original load as there are two of the D's.


<img width="593" height="791" alt="Feature D" src="https://github.com/user-attachments/assets/e29a9bf4-6877-432c-bd0d-e3e3c867e0ae" />

### Feature E

Feature E was approximatiftied as a supported beam with an overhang, the load for feature E was calculated as the reaction force from feature D.
The formula for the beam calculation was not ripped straight from the searing pages of Machinery's Handbook (gasp), rather searched for and found upon said internet.

https://www.structx.com/Beam_Formulas_025.html

<img width="600" height="791" alt="Feature E1" src="https://github.com/user-attachments/assets/40919b1c-4d05-443a-b5c7-b244ab96e38d" />
<img width="603" height="788" alt="Feature E2" src="https://github.com/user-attachments/assets/df36947b-f419-411a-84de-d72a1ad44006" />

### LinkityLink

A Link were designed per specification to slip fit onto the shaft at Feature A.
This link is to be assembled by "light pressure" onto a 1" shaft.

Hole for slip fit onto shaft A determined by consult to machinery's handbook page 654, RC Table, Class RC4 column.
Shaft minimum diameter is 0.662 in. so shaft max diameter is 0.6627 in.
To match fit classification, hole diameter will be  0.6633 (+0.0010 / -0.0000).

The Hole for the 1 inch nominal shaft was determined by consult to machinery's handbook page 659, FN Table, FN1 Column.
Shaft diameter is 1.0010 in. (+/- 0.0002 in.), hole diameter is 1.0000 (+0.0005 / -0.0000) in.

Using a thickness of 0.050" to correspond the the excess length designed into shaft A, The Width was calculated for Stress and Stifness, with the stiffness being the governing factor.
Overall Width at Length 2.5 and thickness 0.050" will be 2.875 inches.

Manufacturing of the outer profile can be achieved by laser or waterjet so long as length and thickness are called out as minimum material condition.
The holes themselves will need to be achieved through reaming to achieve desired precision.

## Communicate

### Sketch Compiled

Overall sketches were compiled after dimensions calculated.

<img width="631" height="805" alt="Sketch1" src="https://github.com/user-attachments/assets/3697a2ba-e7c3-46ac-af07-131f1a5f6e5b" />

<img width="618" height="786" alt="Sketch 2" src="https://github.com/user-attachments/assets/00e9d9cc-604c-4963-93da-0f3eddd878c6" />




