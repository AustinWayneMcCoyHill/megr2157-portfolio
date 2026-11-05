# A9 – Pulleys

## Objective
Design a pulley system given the following parameters.

<img width="828" height="557" alt="Parameters" src="https://github.com/user-attachments/assets/3ac863f4-ef61-4107-a541-72033541bde2" />

The force chosen was 5lb

The RPM : 1500

The span (distance between pulley centers): 5in

The pulley material: 6061-T6 Aluminum

I decided to try to rely only on pin and paper, machinery's handbook and our benevolent lord and savior McMaster-Carr for this assignment.

### AI disclaimer

The only searching I had to do was to find the coefficient of friction for aluminum on rubber (strange how absent this is on any list I could find. Aluminum pulley sheaves are definitely a thing.)
Prompt: Coefficient of friction between aluminum and steel, Belt and Pulley Application, Request for references
Result: 0.6, literally just should have chosen steel and gotten through with it given that this was the last time the pulley material was of any consequence.

### AI Screenshots

<img width="823" height="648" alt="Prompt" src="https://github.com/user-attachments/assets/5f4d6dae-eeba-41a6-b00a-2b45fa8e8bca" />

<img width="746" height="108" alt="Result" src="https://github.com/user-attachments/assets/fb1e9114-63e9-4062-8a18-edf8ccb8bc89" />

<img width="807" height="638" alt="Prompt Reference" src="https://github.com/user-attachments/assets/08378df7-8b9e-4228-a7e5-a9be126f51d5" />




## Analyze

###Pulley and Belt Calculations
To derive the minimum belt thickness the formulae discussed in class were used.

The minimum belt diameter was calculated at just over 1/4".

This left an enginerd decision for the ages.  Do I skimp on safety factor, or do I overbuild and give my self a silent pat-on-the-back.

In your heart of hearts, you know the answer.

The closest belt diameter offered by McMaseter-Carr is 5/16" raising the relative safety factor past 3 and giving everyone the warm and fuzzies.

The pulley circumference was calculated by adding the pulley diameter to twice the belt diameter, multiplying by pi (yummmy) and adding twice the span.

This left us with a outer circumference of just over 21-3/8". Ready-Made belts are not available in this particular circumference so a custom length, or shop made-belt will be in order.


#### P and B - FBD

<img width="649" height="512" alt="PandBFBD" src="https://github.com/user-attachments/assets/dcc82208-bddf-4960-8b93-c2e470c14640" />


#### P and B calculations

<img width="674" height="807" alt="PandBcalc" src="https://github.com/user-attachments/assets/f96579ca-9e3b-437b-9ef8-3b6ff038d13e" />

There was a typo in my hand calculations, missing a factor of 2 in the circumference calculation.

#### Correction

<img width="729" height="235" alt="circumference" src="https://github.com/user-attachments/assets/e516c7f3-a7f4-437b-b091-10fa2cf03fcf" />


### Shaft Calculations

Using 1060 Hardened Steel.

I looked up the Yield strength of hardened 1060 in Machinery's handbook (32nd Edition)

Yield Strength = 113,000 psi.
I found a factor of 0.577 for deriving shear strength from yield strength.

Using this and standard T-over-Zp calculations to derive shaft minimum diameter, it was found to be roughly 0.17".
In any practical case 3/16" (0.1875") will be used

#### Shaft (you damn right) FBD and Calculations

<img width="620" height="752" alt="Shaftydr" src="https://github.com/user-attachments/assets/a834d116-34aa-4ed7-baf2-1b8d9e8ecc3e" />

### Bearings

Using Force/Area for pressure and basic SFM from shaft diameter and RPM:

Pressure was found to be 313.3 psi.

Linear velocity was found to be 67.9 sfm

PV was found to be 21,284 (pv's , unitless, sam-elliots?, smf*psi seems awkward)

Porous Bronze fits the bill nicely and McMaster-Carr p/n#: 6381K408 will more than suffice

https://www.mcmaster.com/6381K408/

#### Bearing FBD and Calculations

<img width="608" height="400" alt="Bearing ONly" src="https://github.com/user-attachments/assets/09465c9d-96a4-4863-a019-4b3bb3dfb4c7" />

### Frame (I'm gonna spin forever)

Taking the simplicity given in the assignment resources as a sterling example of brutal efficiency, I followed suit with a straight bar design.
Some calculations were made but given that my chosen material is A36 steel with a yield strength of 36,000 psi and a half inch of thickness just to support the bearing,
I don't think that strength will be too much of an issue.

#### Frame Calcs

<img width="609" height="415" alt="Frameboatloadsoffram" src="https://github.com/user-attachments/assets/29828ff4-81d3-46fd-9a98-e733190dae7e" />

## Lessons Learned

1) Keep it simple as much as you can. The complications will come.
   This is more a general sense of what I'm taking away from this class and the the first half of my education in engineering. Overthinking and trying to fit everything perfectly together from the start will waste a lot of time and willpower

2) Just because I've used aluminum pulley sheaves in the past doesn't mean that the information is as readily available as I would like. I probably spent more time on this project trying to find a table with a discreet value of friction coeff. for polyurethane  rubber on aluminum than any other part of the exercise. This is what I meant by the complications will come.

### Time spent.
I spent about four hours on this assignment.

