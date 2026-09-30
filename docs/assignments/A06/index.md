# A6 – [Bracket Drawings]

## Objective
The objective for assignment A6 was to create parametric solid models and 2d drawings for the parts designed in assignment A5.
To achieve this task Solidworks (SW) design software was used in the following steps.

## 3D Models
### 1) Designate Materials
This step was carried over from the design decisions of A5.
6061-T6 Aluminum was chosen for the bracket.
Ti-6Al-4V Titanium was chosen for the link.
The only change to materials was the use of the Solidworks Library values for the modulus of elasticity and yield strength of the materials.

<img width="820" height="609" alt="Bracket Materials" src="https://github.com/user-attachments/assets/f671c361-bf25-4aeb-ac93-4b43bd343429" />

<img width="820" height="605" alt="Link Materials" src="https://github.com/user-attachments/assets/e0eb2ab2-44d4-4733-a4ff-13419512da8e" />

### 2) Establishing the parameters and materials
Once a SW session was opened. The material was selected from the SW material library.
The modulus of elasticity and yield strength was noted for the equations.
After the materials were applied, the equations were entered using the equation manager.

#### A6 Bracket Equations
The first entries for the equations were the constant values (the ones not dependent on anything else).
This included the material properties, the clearance dimensions calculated per the T-Bar diagram, and the few dimensions that were left to the designer.
The dimensions left to the designer include the length of cylinder feature A and rectangular feature B.
After the independent dimensions and properties were entered, the equations were entered for the minimum diameters of the various part features.
For all features except the cylindrical feature A, the minimum dimension calculated for stiffness was greater than the minimum dimension for strength.
In all cases the greater of the two dimensions was chosen. 
In some cases multiple equation parameters were combined for a new dimension, for example the overall length of the part "OAL" used the input length of Feature A and the equation driven thickness of Feature B in it's calculation.

<img width="1199" height="774" alt="Bracket Equations" src="https://github.com/user-attachments/assets/204a8304-34db-4191-8cd9-f620d362d550" />

#### A6 Link Equations
The process for entering equations for the link model was the same as the bracket but simper because there was only one part to model.
The material properties were entered first.
The thickness of the part was set as 0.050" in order to guarantee that the part hangs completed on the cylindrical Feature A.
The most critical dimension calculated was the minimum cross section width, denoted "csx" (cross section in x).
this will be used to govern the length as well as the width of the link by guaranteeing there is no section of the part that is less than "csx" wide.

<img width="1202" height="782" alt="Link Equations" src="https://github.com/user-attachments/assets/b25e78dd-5dbd-4f0f-a326-7be1a99b869b" />

### 3) Etching the sketching
With our equations in hand, true as the North-Star, we move forward bravely into the world of the sketch.
By deftly selecting the front plane and, cleverly, clicking on the "create sketch" icon, our process is underway.

#### A6 Bracket Sketch
Because of the relative simplicity of the part, all of the features of the bracket were contained in one sketch.
The sketch was started by drawing a centerline from the origin, up to the top of the T-Slot opening.
The origin was chosen as the center of the cylinder feature (Feature A from project A5).
A circle was placed at the origin and it's diameter was set as the global variable for the calculated feature value "dA"
the "dynamic mirror" feature was used to construct the remaining profile in a rough fashion.
The dimensions were added from the equation sheet and a good time was had by all.

<img width="757" height="767" alt="Bracket Sketch" src="https://github.com/user-attachments/assets/5a3ce066-6033-47ff-8203-e6ab51f9b0d1" />


#### A6 Link Sketch
For the link sketch the center point slot tool was used for the main body. 
The origin point was the midpoint of the centerline of the slot.
The Holes were placed on the centerline of the slot and dimensioned according to their perscribed fit clearances.
The dimensioning for the length and width of the slot was fully driven by "csx" by setting it as the distance between the terminal radii of the slot and the hole circles.
This gave us a fully defined sketch and a renewed sense of purpose and well being.

<img width="796" height="693" alt="Link Sketch" src="https://github.com/user-attachments/assets/79d8dae6-a9bb-46c7-869e-239c19c5d051" />

### 4) 3D'ing the model
Our sketceh are in place and we have little left to do but get on with things so, I suppose we shall.

The 3d part of the modeling became nearly trivial, simply extruding the correct features in the correct directions according to the correct calculated or designed dimension.

This meant that, despite all of our better efforts, we have let our selves become what our family and friends all feared...
Severely inexperienced CAD designers.

[A6 Bracket](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A06/A6Bracket.SLDPRT)

[A6 Link](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A06/A6Link.SLDPRT)

### 5) Putting in all down on paper ... digitally
The last step in our tumultuous sojourn into modern design and everyday life left us transforming our magnificent three-dimensional models into stoic two-dimensional prints.
I was surprised to find that nowadays the prints are no longer blue.
By opening the file menus and selecting "make drawing from part" we were heaved, headlong and somewhat concerned, into the dark forest of sub-menus and flop sweat that is printmaking.
The video for making a projection angle symbol were followed and the title blocks were modified to the specefications of the assignment.
A quick check into the document and drawing properties verified that we were in fact using the correct system of units and third angle projection.
The "standard 3 view" button was used to ensure that the correct projection angle were followed through upon.

#### Dimensioning
For the Bracket, every dimension that was a contact surface to the "T-Bar" was given in max\min "limit" format with a notation marker indicating what face/dimension it was in reference to.
All of the Feature (A-E) Dimensions were given bi-lateral tolerances of -0.000 / +0.010.
The designer designated dimension were left as title-block reference dimensions to two decimal places.
The dimensions that could be derived by adding already noted dimensions together but, would be more convenient for manufacturers to be given, were shown as reference dimensions (in parenthesis).
The only exception to this was the diameter for feature A which, because of the link, needed a clearance fit callout for an RC 4 slip fit.
This tightened it's bi-lateral tolerance from +0.01 / - 0.00 to +0.0007 / -0.0000, keeping it's minimum value protected.
Notation markers were also added to features of symmetry on the part where it was deemed appropriate.
Finally a "Notes" block was added for the utmost in clarity and care.
Because of it's relative simplicity, the link drawing did need an entire "Notes" section and only got the one not it needed arrowed directly to its feature.
This was the RC4 clearance hole corresponding to the RC4 pin fit from the bracket drawing.
The actual dimensions were still given as limit tolerances for the pin/hole fits and a note for the "csx" dimension to be followed throughout the entire part as the minimum width at any section.
For manufacturer convenience, the center to center distance of the two holes was also added.

#### Print Links

[A6 Bracket Drawing (SW)](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A06/A6BRACKET.SLDDRW)

[A6 Bracket Drawing (PDF)](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A06/A6BRACKET.pdf)

[A6 Link Drawing (SW)](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A06/A6Link.SLDDRW)

[A6 Link Drawing (PDF)](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A06/A6Link.pdf)


## Lessons Learned

The primary lesson that I learned is that no matter how many times you double check, there is always one thing that you can find on a print that could be tweaked "just a little bit" to make it look neater/better/more complete.
In my experience, the modelling component is far easier and faster than the print making specifically because the print is a form of communication. In many ways it's the worst form of communication because it only really goes one way and one time in many cases. If you were to send a flawed but technically viable print to a manufacturer they MAY call you and ask for clarification, but they could just as easily make the parts to the print and ship them (and the invoice) to you without saying anything at all.
What I found with print making, both in this assignment and others, is that it's best to start with the most critical information. Get that on the page, make sure it is clearly communicated, then build the rest of the print around it. Specific to this project, the clearance features on the T-Bar seem excessively tight in too many directions but, I didn't design that part so I can only ensure that it is clear to whoever gets the parts that those dimensions are to be held, for whatever reason. From a quality standpoint, the fit and finish of consumer product significant to sales. Parts that feel and look better will usually sell better and be able to demand higher prices. In industrial and automotive parts, poor fitting means production stops or massive assemblies have to be delayed because a part technically was made "to-print" but the print allowed the physically impossible to be made real.

My name is Ausitn Hill and I spet about 7 hours on this project.
1 making models.
3 making prints.
3 compiling this nonsensical website arrangement.

614 out of 743.2 stars.

