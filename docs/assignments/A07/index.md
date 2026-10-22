# A7 – [FEA on Bracket]

## Objective - "to develop a deeper understanding of how FEM can be used in the design process" where no-one has FEA'd before
It were begun by reviewing the videos and slides from the class session about Finite Element Analysis.
The assignment is to take the bracket and link parts that we created for assignment 5 and drew up onto prints for assignment 6, and to use finite element analysis software to optimize their designs for strength, stiffness and to reduce component weight as much as possible.

## Files For Reference


## Analyze
Starting with the bracket, the first thing I did was to set up the static simulation study.
For reference, the origin of my bracket design  is as follows:

<img width="319" height="382" alt="A7 Origin Front" src="https://github.com/user-attachments/assets/03483dfd-2664-40b9-9897-626559398546" />

Y and Z are centered in the axis of the cylindrical component "A".

<img width="290" height="372" alt="A7 Origin Left" src="https://github.com/user-attachments/assets/23e786de-a876-408a-9ff4-33d071cd4850" />

X originates at the junction plane between feature B and feature A.

After starting the simulation setup, I was left to decide which faces would be considered "fixed" or constrained from movement under load. Given that the design intent is for the bracket to hold on a "t-bar", I decided to constrain all of the eligible contact faces. It is possible for the bracket to rack or twist within a thousandth of an inch inside of it's tolerance but it is equally likeyly to spin one way or another so constraining all contact faces is a reasonable path to take.
I also chose the cylindrical surface of component "A" as the face to take the load and the direction to be normal to the bottom face of the bracket component "C".

<img width="599" height="582" alt="A7 Fixture Planes" src="https://github.com/user-attachments/assets/1577410f-b337-43c5-b9c3-3e41b95ced51" />

The force I calculated for assignment 5 was 750 lbs and I saw no reason other than sheer spite to change it now.
I decided to start at the most coarse setting of mesh counts and move to medium/default, then, if needed, ramp the slider all the way up to "foine".
The first test was very near abysmal. I believe I neglected a force somewhere or another because there was over a quarter inch of deflection shown in the result of the FEA simulation. The Maximum stress was 184773psi, (well beyond the yeild strength of the 6061 T-6 Aluminum that the part was to be made from.

<img width="518" height="505" alt="Des1Loop1Stress" src="https://github.com/user-attachments/assets/698aa283-9d91-427b-a7dd-dbd83d2a5e69" />

<img width="616" height="631" alt="D1L1deflection" src="https://github.com/user-attachments/assets/ee7619cc-af3d-4e0d-bd7e-1fb097ad19e8" />







We must, however, verify bad news as well as the good.
Moving the slider 




## Decide


## Communicate

