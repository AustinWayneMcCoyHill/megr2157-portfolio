# A7 – [FEA on Bracket]

## Objective - "to develop a deeper understanding of how FEM can be used in the design process" where no-one has FEA'd before
It were begun by reviewing the videos and slides from the class session about Finite Element Analysis.
The assignment is to take the bracket and link parts that we created for assignment 5 and drew up onto prints for assignment 6, and to use finite element analysis software to optimize their designs for strength, stiffness and to reduce component weight as much as possible.

## Files For Reference

[A7 Bracket](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A07/A7Bracket.SLDPRT)

[A7 Link](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A07/A7Link.SLDPRT)

[A7 Tabulation spreadsheet](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A07/A7Tabulations.xlsx)

[A7 Tabulation pdf](https://github.com/AustinWayneMcCoyHill/megr2157-portfolio/raw/main/docs/assignments/A07/A7Tabulations.pdf)


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
The first test was very near abysmal. I believe I neglected a force somewhere or another because there was over a quarter inch of deflection shown in the result of the FEA simulation. The Maximum stress was 184773psi, (well beyond the yeild strength of the 6061 T-6 Aluminum that the part was to be made from. We must, however, verify bad news as well as the good.

###  Bracket Design 1

#### Design 1 Loop 1
<img width="518" height="505" alt="Des1Loop1Stress" src="https://github.com/user-attachments/assets/698aa283-9d91-427b-a7dd-dbd83d2a5e69" />

<img width="616" height="631" alt="D1L1deflection" src="https://github.com/user-attachments/assets/ee7619cc-af3d-4e0d-bd7e-1fb097ad19e8" />

Advancing the mesh to medium resolution, the % difference for stress and deflection were 6% and 3% respectively.
The minimum factor of safety was off by 9% so the fine resolution was used.

#### Design 1 Loop 2
<img width="393" height="466" alt="D1L2 Stress" src="https://github.com/user-attachments/assets/3f11c503-7da0-4e16-b003-2efbd8774811" />

<img width="438" height="493" alt="D1L2 Deflection" src="https://github.com/user-attachments/assets/b573588d-dcab-4523-a9ee-506587f6698e" />

With the finest available standard mesh the maximum stress changed more than between coarse and medium (11%) but the deflection stayed stable (2%)

#### Design 1 Loop 3

<img width="405" height="524" alt="D1L3 Stress" src="https://github.com/user-attachments/assets/26883b9f-d099-4a94-b775-4c708ebaecdc" />

#### Bracket Design 1 Final

<img width="1461" height="795" alt="D1 Deflection" src="https://github.com/user-attachments/assets/9a810489-9d2e-4eb8-8e32-ecd18c9efb0d" />

<img width="1417" height="746" alt="D1 Stress" src="https://github.com/user-attachments/assets/7c6370ac-6a93-4274-ac16-ecc8b37821db" />

The FEA analysis convereged for Stress and Deflection but not exactly for safety factor. This is most likely because there was some miscalculation for the thickness in component "B" of the model causing very high stress concentrated at the junction of component "B" and "A". A finer mesh was created for acedemic rigor resulting in the stress perecent difference being higher between the fine and medium mesh than between the medium and coarse mesh. The deflection, however, was slightly closer. The safety factor was different by the same amount between both tests. The heat maps of stress and deflection were largely blue outside of the maximum locations, therefore the design change will focus there first. The remedy was decided to be mirroring feature B along the y axis. This eliminates the bending moment of the load and reduced stress greatly. Part weight was 0.237 lbs

### Bracket Design 2
After making the changes the design was in much better shape. The minimum safety factor rose (briefly) above 4 only to settle back to just over 1

#### Design 2 Loop 1

<img width="583" height="628" alt="D2L1 deflection" src="https://github.com/user-attachments/assets/d707d047-3c0a-4e23-9bde-d53673b711de" />

<img width="621" height="722" alt="D2L1 Stress" src="https://github.com/user-attachments/assets/15c2f7ed-41d7-4679-bb91-2b4240e34cff" />

#### Design 2 Loop 2

<img width="454" height="525" alt="D2L2 Stress" src="https://github.com/user-attachments/assets/9b63324c-9753-4637-b07c-f82e64978f9d" />

<img width="525" height="576" alt="D2L2 deflection" src="https://github.com/user-attachments/assets/4eb01f4c-286b-4b64-aa20-50ccb231852e" />

#### Design 2 Loop 3

<img width="601" height="558" alt="D2L3 Stress" src="https://github.com/user-attachments/assets/aada1743-4df7-4dc9-90fe-79ffb70e8d54" />

<img width="478" height="539" alt="D2L3 deflection" src="https://github.com/user-attachments/assets/e95e0263-c43f-453e-bd0f-5aedde9f4f13" />

#### Bracket Design 2 Final

<img width="1072" height="698" alt="D2 deflection" src="https://github.com/user-attachments/assets/67a0e7c8-d53f-4a7b-8d96-a555e30fb3b7" />

<img width="1370" height="768" alt="D2 Stress" src="https://github.com/user-attachments/assets/c1d35d0d-a109-47fa-b9bd-2fb1693766fb" />

Convergence was not achieved throughout FEA analysis for Design 2. It is suspected that stress concentrations at sharp corners of model are to blame. As the mesh gets finer and finer, the calculated  stress gets hisgher and higher in the small corners leading to ever ascending readings for stress and safety factor. The design change was very effective reducing the maximum stress by a factor of 129 (2 orders of magnitude), and the  maximum deflection by a factor of 117.6. The next design change will be to fillet the corners of the part in an attempt to get the FEA to converger itself like a good little boy. Additionally through holes will be added to lighten the part and the thickness of component "C" will be reduced to the same end. Part weight was 0.271 lbs

### Bracket Design 3
Nearing the goal of a stable factor of safety greater than 4 the design changes were made and holes added through the part in order to lighten the part as much as possible

#### Design 3 Loop 1

<img width="527" height="495" alt="D3L1 Stress" src="https://github.com/user-attachments/assets/324a9738-19bc-4904-be7a-5a034ccd7389" />

<img width="468" height="554" alt="D3L1 deflection" src="https://github.com/user-attachments/assets/961bf761-b0c9-4417-b7b1-d2e4397a77fb" />

#### Design 3 Loop 2

<img width="420" height="430" alt="D3L2 Stress" src="https://github.com/user-attachments/assets/79c21b24-c778-4487-b957-eef24382ef8c" />

<img width="496" height="573" alt="D3L2 Deflection" src="https://github.com/user-attachments/assets/0ffbe7d7-210c-4aec-99ef-d32782b05de6" />

#### Design 3 Loop 3

<img width="644" height="612" alt="D3L3 Stress" src="https://github.com/user-attachments/assets/b4ee01f7-b9fc-42a2-86fe-d412da78dd23" />

<img width="570" height="610" alt="D3L3 Deflection" src="https://github.com/user-attachments/assets/c9d3ccd3-77ab-42c6-83bf-de1e710cb5ae" />

#### Bracket Design 3 Final

<img width="1388" height="740" alt="A7 Bracket" src="https://github.com/user-attachments/assets/983bafe6-c131-4a62-a81a-6f8a31130c93" />

With all of the filleting complete and the lightening holes in place, the factor of safety and deflection were stable to 3% and 0% (rounded) respectively. The max stress was stable to 5%. 
Not having sharp corners for stress to build up in seemed to go a long way for stability through progressive resolution iterations.

### Link Design 1
Because of the change in part geometry a design change was immediately necessary for the link piece. with the strap holding cylinder feature "A" closed at both ends, a similar diameter hole would not do any potential future-user any good. But, by saving grace and a couple hours of fruitless toil trying to design a titanium "s-hook" about the thickness of a credit card. I gave up and tried something else.
Cleverly, I had placed a lightening hole in the center of the cylinder feature "A". Using a pin it should be possible to mount a link and use it in the manner intended by reducing the bracket size hole to have the same RC4 fit for a smaller diameter. 
The initial FEA simulation was setup as for the follows.

<img width="464" height="783" alt="Link FEA Setup w Origin" src="https://github.com/user-attachments/assets/6a9ae403-7630-4cf8-a9a6-601b3875e26c" />

<img width="527" height="798" alt="Link FEA Setup" src="https://github.com/user-attachments/assets/39f61845-bd9f-4d8f-9b0c-8848b89f7bd5" />

The part origin is at the center of the overall length in Z, because of the minimum cross section width requirements and the two different size holes in the jeezless thing, it is not quite centered between the holes... Thanks Obama.
The X axis is originated on the front plane surface and the Y axis originates down the centerline of the part normal to X and Z. The hole surface that mounts to the bracket was held as the constraint and the load was set to be on the opposide hole surface down the centerline of the part. The material for the link is grade 5 titanium. The initial weight is 0.03 lbs

#### Design 1 Loop 1

<img width="579" height="548" alt="Link D1L1 Stress" src="https://github.com/user-attachments/assets/8382c22a-54a4-4650-81a7-31b6c396d2ca" />

<img width="444" height="466" alt="Link D1L1 Deflection" src="https://github.com/user-attachments/assets/dd2d6689-cf33-448d-b58c-9c5c58b71f15" />


#### Design 1 Loop 2

<img width="360" height="449" alt="Link D1L2 Stress" src="https://github.com/user-attachments/assets/ec4c03ea-68fb-4c57-adc5-8c8265a65dfd" />

<img width="460" height="498" alt="Link D1L2 Deflection" src="https://github.com/user-attachments/assets/a9700104-30a4-4cb6-866e-1c2153f56343" />

### Link Design 2

For the most part the FEA reflected previous calculations and the Factor of safety was upheld at or above 4. There is, however about 0.002" of deflection. In order to remediate The thickness will be increased from 0.050 to 2mm (0.078"). Also, because the "B" component was doubled the link can no longer slide into place. There is now a hole through "A" that can accomodate a pin with a diameter of 0.4542". This is still in the same fit classification and schedule of the previous hole so the diameter of of the bracket side of the link will be decreased to 0.45801. The 2nd outer loop wight was around 0.05 lbs

#### Design 2 Loop 1

<img width="410" height="438" alt="Link D2L1 Stress" src="https://github.com/user-attachments/assets/b5778f9a-6237-493a-a06e-4a4d3ad23e07" />

<img width="512" height="495" alt="Link D2L1 Deflection" src="https://github.com/user-attachments/assets/14607074-bd3d-4635-a86a-d2bc2112246e" />

#### Design 2 Loop 2

<img width="444" height="367" alt="Link D2L2 Stress" src="https://github.com/user-attachments/assets/60fed58f-2c79-4e52-b94b-dca31796597c" />

<img width="419" height="500" alt="Link D2L2 Deflection" src="https://github.com/user-attachments/assets/8cd12227-fc36-42bc-b783-2da297c51bca" />

### Link Desigh 3

The deflection is still do damn high…. Like the rent… and my uncle steve.  Thickening to 2.5mm (0.098")
However the FEA results are convergeing well within limits. The stress and deflection with %difference of 4% and the saftey factor only differing by 2%
#### Design 3 Loop 1

<img width="447" height="445" alt="Link D3L1 Deflection" src="https://github.com/user-attachments/assets/0e1bea70-734a-455e-994f-9f2a758ef255" />

<img width="423" height="423" alt="Link D3L1" src="https://github.com/user-attachments/assets/5ed4820e-c4f8-461d-a8a0-57bc552cce36" />

#### Design 3 Loop 2 

<img width="503" height="383" alt="D3L2 Stress" src="https://github.com/user-attachments/assets/c3e4475b-dca6-40b1-96a3-039325bbaaa3" />

<img width="531" height="430" alt="D3L2 Deflection" src="https://github.com/user-attachments/assets/3523ad81-4adb-451f-8ac0-3b3e570b5508" />

#### Design 3 Final

<img width="1378" height="798" alt="A7 Link" src="https://github.com/user-attachments/assets/77ee6a73-4dc9-45a8-9d5f-64fc23a3ed4d" />

With a weight less than 0.1 lbs, a safety factor of 8.9 and deflection just over 0.001" we call this phase of the design complete.

## Lessons Learned

This project thrust me kicking and screaming, against most better judgment and almost certainly better nightly entertainment options, into the world of Solidworks FEA simulation. There were two parts that gave me pause and/or made me question my understanding of the process. The first is the default scaling of the analyzed distortions.

#### Default Distortion Scale

<img width="360" height="431" alt="why" src="https://github.com/user-attachments/assets/137f4951-be23-4feb-b1ac-9869e41facdf" />

<img width="351" height="192" alt="whaaaaaaieee" src="https://github.com/user-attachments/assets/9f9a64cd-e987-4fd3-a6c8-898fc0f14ad4" />


The scale of what the software distorts the mesh to after simulation is not true-to-life, but instead scaled up 250 times.
If you are of a visual mind and do not know this, panic almost certainly could (read did) ensue. This is more of a personal gripe however. The second is exactly how the safety factor in Solidworks is calculated. It seems to be more related to stress than to deflection but there may be settings somewhere that I did not find. I look forward to being able to apply the FEA analysis tools in future projects with some modicum of earned confidence. This project took about 5 hours.
I give it 6.8459 out of shivty pickles.




