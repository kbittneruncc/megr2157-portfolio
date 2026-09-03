# A2 - Truss Stress Analysis

## Objective

The objective of this project was to design a lightweight planar truss capable of supporting two opposing 25 kN loads. The truss members were designed using ASTM A500 Grade C steel with a required safety factor of 3.5. The connecting pins were designed using hardened tool steel with a required safety factor of 4. Hand calculations were used to determine the internal forces, required member area, pin dimensions, and approximate weight before the design was modeled in Fusion 360.

## Analyze

### Design Requirements

A load of 25 kN was selected from the permitted range of 20 kN to 30 kN. The required horizontal dimension was a = 0.4 m, and the required vertical dimension was b = 0.3 m. Every truss member was required to have the same cross-sectional area, and every connecting pin was required to have the same diameter.

Point A was modeled as a pin support, while point B was modeled as a roller support. The truss, excluding its pins, was required to be represented as one continuous CAD part. The assignment also allowed the assumption that members in compression would not fail through buckling.

### Truss Geometry

A four-joint, five-member truss was selected. The members were AB, BC, CD, DA, and BD. This arrangement formed two connected triangular regions and provided a simple, stable geometry.

The joint coordinates used in Fusion 360 were:

B = (0 mm, 0 mm)

C = (400 mm, -300 mm)

D = (800 mm, -300 mm)

A = (1200 mm, 0 mm)

Moving point B to the origin did not change the required dimensions or geometry.

![Selected truss geometry](truss-geometry.png)

### Static Determinacy

The truss contained five members, four joints, and three support-reaction components. The planar-truss determinacy equation was used to verify that the structure could be solved using the equations of static equilibrium. The complete determinacy calculation is shown below.

![Static determinacy calculation](determinancy-calculation.png)

The calculation showed that the truss was statically determinate.

### Entire-Truss Free-Body Diagram

An entire-truss free-body diagram was created before the individual joints were analyzed. The pin at A produced horizontal and vertical reactions, while the roller at B produced one vertical reaction. The reactions were found by applying the horizontal-force, vertical-force, and moment equilibrium equations.

![Entire-truss FBD and support-reaction calculations](truss-fbd-reaction.png)

The horizontal reaction at A was 0 kN.

The vertical reaction at A was 8.333 kN upward.

The vertical reaction at B was 8.333 kN downward.

The downward reaction at B means the support must be capable of resisting uplift. A captured roller or similar support would be necessary in a physical version of the design.

### Joint Free-Body Diagrams

A separate free-body diagram was created for each joint. Every unknown member force was initially assumed to be in tension and was drawn pointing away from its joint. A negative result indicated that the actual force direction was opposite the assumed direction and that the member was in compression.

![Joint C & D free-body diagram](joint-cd-fbd.png)

![Joint A and B free-body diagrams](joints-ab-fbd.png)

### Internal Member Forces

The method of joints was used to calculate the force in each truss member. Joint C was analyzed first because it contained only two unknown member forces. The remaining joints were analyzed after the forces in BC and CD were known.

The force in member AB was 11.111 kN in compression.

The force in member BC was 41.667 kN in compression.

The force in member CD was 33.333 kN in compression.

The force in member DA was 13.889 kN in tension.

The force in member BD was 47.467 kN in tension.

Member BD contained the largest internal force. Therefore, 47.467 kN was used to design the common cross-sectional area of all five members.

### Truss Member Cross-Sectional Area

The minimum member area was determined using the largest internal force, the yield strength of ASTM A500 Grade C steel, and a safety factor of 3.5. A yield strength of 345 MPa was used. The known quantities, unknown quantities, symbolic solution, and numerical solution are shown in the following hand calculations.

![Member-design knowns and unknowns](member-knowns-unknowns.png)

![Numeric & symbolic member-area calculation](member-area.png)

The calculated minimum cross-sectional area was 481.546 square millimeters.

A rectangular member measuring 49 mm wide and 10 mm thick was selected. This produced a cross-sectional area of 490 square millimeters.

The selected cross section produced an actual safety factor of 3.561. Since this value was greater than the required safety factor of 3.5, the selected cross section satisfied the design requirement.

### Analytical Truss Weight

The total length of the five truss members was 3.45440 m. The selected area of 490 square millimeters and a steel density of 7850 kilograms per cubic meter were used to estimate the volume, mass, and weight of the truss. The complete calculation is shown below.

![Analytical truss-weight calculation](truss-weight-calculation.png)

The approximate truss volume was 0.001692656 cubic meters.

The approximate truss mass was 13.2864 kg.

The approximate truss weight was 130.296 N.

This analytical calculation treated each member as a complete prism. Therefore, it counted some overlapping material at the joints more than once.

### Pin Design

The connecting pins were designed using the largest transmitted force of 47.467 kN. The pins were made from hardened tool steel with a shear yield strength of 170 ksi and a density of 0.278 pounds per cubic inch. The pins were analyzed as single-shear connections using a safety factor of 4.

The known quantities and unknown quantities are shown below.

![Pin-design knowns and unknowns](pin-knowns-unknowns.png)

A free-body diagram was created for the pin carrying the largest force. The diagram contained two equal and opposite forces and one shear plane.

![Critical-pin free-body diagram](pin-fbd.png)

The symbolic and numerical pin calculations are shown below.

![Numerical & symbolic pin calculation](pin-area.png)

The minimum required pin area was 0.251081 square inches.

The minimum required pin diameter was 0.565408 inches.

A standard 5/8-inch pin was selected. This was equivalent to a diameter of 0.625 inches or 15.875 mm.

The selected pin area was 0.306796 square inches. The selected pin produced an actual safety factor of 4.888, which exceeded the required safety factor of 4.

Four pins were used in the completed model. Their approximate combined weight was 0.59749 N.

### Failure Modes

ASTM A500 steel was treated as a ductile material because it can undergo plastic deformation before fracture. If a tension member were overloaded, yielding would be expected before tensile fracture. Member BD was the most highly loaded tension member and was therefore the most likely member to experience tensile yielding.

Members AB, BC, and CD were in compression. Buckling would normally be an important failure mode for slender compression members. However, the assignment specifically allowed the assumption that the compression members would not fail through buckling. With buckling excluded, compressive yielding was considered the expected failure mode for the compression members.

The likelihood of member failure could be reduced by increasing the member cross-sectional area, shortening the unsupported member lengths, adding lateral bracing, or using a material with a greater yield strength. Increasing the area would reduce the normal stress but would also increase the weight of the truss.

The connecting pins were loaded in single shear. If a pin were overloaded, shear yielding across the single shear plane would be the expected failure mode. The likelihood of pin failure could be reduced by increasing the pin diameter or redesigning the joint as a double-shear connection.

## Decide

### Load Selection

A load of 25 kN was selected because it was at the midpoint of the permitted 20 kN to 30 kN range. This provided a representative loading condition without using either extreme of the permitted range. All member and pin calculations were based on this selected load.

### Geometry Selection

A four-joint, five-member truss was selected because it formed stable triangular regions and satisfied the equation for a statically determinate planar truss. The simple arrangement reduced the number of members required to carry the loads. Using fewer members also helped reduce the total material and weight.

### Member-Size Selection

A 49 mm by 10 mm rectangular cross section was selected instead of using the exact minimum area of 481.546 square millimeters. The selected dimensions produced an area of 490 square millimeters and were easier to model in Fusion 360. This area provided a safety factor slightly greater than 3.5 without adding a large amount of unnecessary material.

### Pin-Size Selection

A 5/8-inch pin was selected because the calculated minimum diameter of 0.565408 inches was slightly greater than 9/16 inch. The selected diameter produced a safety factor of 4.888. A larger pin was not selected because it would add unnecessary material and weight.

### Joint-Pad Selection

Circular joint pads with diameters of 70 mm were added around the pin locations. The 16 mm pin holes would have reduced the net cross-sectional area below 490 square millimeters if the original 49 mm member width had been maintained through the joint. The enlarged pads left an approximate net area of 540 square millimeters around each hole.

Because 540 square millimeters was greater than the selected member area of 490 square millimeters, the joint areas satisfied the cross-sectional-area requirement.

## Communicate

### Fusion 360 Model

The complete truss was created in Fusion 360 as one continuous part rather than five separate member components. Each member was modeled with a width of 49 mm, and the complete truss was extruded to a thickness of 10 mm. Circular joint pads with diameters of 70 mm were added at points A, B, C, and D.

![Dimensioned Fusion 360 sketch](fusion-sketch.png)

![Completed Fusion 360 truss part](fusion-truss.png)

A 16 mm through-hole was cut at the center of each joint pad. One separate pin component was created with a diameter of 15.875 mm and a length of 10 mm. Four occurrences of the pin were inserted into the assembly and positioned in the four joint holes.

![Fusion 360 pin model](fusion-pin.png)

![Completed truss assembly](truss-assembly.png)

### Material Properties

A custom ASTM A500 Grade C steel material was assigned to the truss. The material density was set to 7850 kilograms per cubic meter. The Young’s modulus was set to 200 GPa, the Poisson’s ratio was set to 0.30, and the yield strength was set to 345 MPa.

A custom hardened tool-steel material was assigned to the pins. The pin density was set to 0.278 pounds per cubic inch. The provided shear yield strength of 170 ksi was used in the hand calculations instead of being entered as Fusion’s tensile yield strength.

![Fusion 360 material properties](material-properties.png)

### CAD Mass Properties

Fusion 360 was used to determine the predicted mass of the completed truss and pin assembly. The material properties were assigned before the assembly properties were measured. The Fusion 360 mass-properties result is shown below.

![Fusion 360 mass properties](mass-properties.png)

The CAD assembly mass was 12.690041 kg.

The corresponding CAD assembly weight was 124.447 N.

The analytical truss mass was 13.2864 kg. After adding the approximate pin mass, the complete analytical assembly mass was 13.3473 kg.

The percent difference between the analytical and CAD assembly masses was 4.925 percent. The CAD value was lower because the analytical calculation counted the complete length of every member, including overlapping regions. Fusion 360 merged the intersecting members into one body and removed the material cut from the pin holes.

### Engineering Lessons Learned

This project demonstrated that the initial direction assumed for a member force affects how the final result is interpreted. A negative force did not mean the calculation was incorrect. It indicated that the member was in compression instead of the initially assumed tension.

The project also demonstrated that a pin hole reduces the available cross-sectional area at a connection. The original member area was large enough away from the joints, but additional material was required around the holes. Enlarging the joint pads prevented the pin holes from becoming the weakest cross sections.

The CAD model demonstrated how overlapping geometry affects weight calculations. The analytical method counted overlapping member material more than once, while Fusion 360 counted the merged material only once. This produced a reasonable difference between the analytical and CAD weight predictions.

### Mistakes and Revisions

During the first CAD extrusion, Fusion 360 filled the triangular openings because all closed sketch profiles were selected. The unwanted triangular material was removed using an extrude cut through the complete thickness. This created the intended open truss structure.

The pins initially moved together because they were copied as bodies instead of being inserted as separate component occurrences. The pin was converted into a component and inserted four separate times. This allowed each pin to be positioned independently.

The first joint design did not account for the material removed by the pin holes. Circular 70 mm pads were added around the joints to maintain the required net cross-sectional area. This revision prevented the connection regions from being weaker than the main members.

### Failure Modes of the Truss Members

The truss members were modeled using ASTM A500 Grade C steel. This material has a yield strength of approximately 345 MPa and an ultimate tensile strength of approximately 427 MPa. Because the yield strength is lower than the ultimate tensile strength, the steel is considered ductile and will generally begin yielding before it fractures under gradually applied axial loading.

The normal stress in each member was calculated by dividing the absolute value of its internal internal force by the selected cross-sectional area of 490 square millimeters. All calculated stresses were below the yield strength of 345 MPa. The following sections identify the most likely failure mode for each member if the loading were increased.

#### Member AB

Member AB carries 11.111 kN in compression. Its normal compressive stress is approximately 22.676 MPa, which is below the 345 MPa yield strength of the steel.

Because AB is the longest compression member at 1200 mm, its most likely realistic failure mode is buckling rather than material yielding or fracture. Long compression members can become unstable and bend laterally before reaching the material’s compressive yield strength. The assignment permits buckling to be ignored in the original sizing calculations, but buckling remains the most likely physical failure mode for this member.

ASTM A500 Grade C steel is ductile, but ductility does not prevent a long compression member from buckling. Buckling is controlled mainly by member length, end conditions, modulus of elasticity, and the smallest moment of inertia. The Euler buckling equation shows that the critical buckling load decreases as member length inrch2"]}}

The likelihood of failure could be reduced by adding lateral bracing, decreasing the unsupported length, or increasing the 10 mm weak-axis thickness of the member.

#### Member BC

Member BC carries 41.667 kN in compression. Its normal compressive stress is approximately 85.034 MPa, which is below the 345 MPa yield strength.

The expected realistic failure mode is buckling because the member is relatively slender and is loaded in compression. Although BC is shorter than AB, it carries a considerably larger compressive force. This combination makes buckling more likely than yielding or fracture unless the member is properly braced.

The material is ductile, but the member could become geometrically unstable before the material yields. The assignment assumption allows buckling to be excluded from the sizing calculation, so the member satisfies the required axial-yield safety factor under that assumption.

The likelihood of buckling could be reduced by increasing the weak-axis thickness, adding out-of-plane bracing, or reducing the unsupported member length.

#### Member CD

Member CD carries 33.333 kN in compression. Its normal compressive stress is approximately 68.027 MPa, which is below the 345 MPa yield strength.

The expected failure mode is buckling because CD is a compression member. However, CD is only 400 mm long, making it less susceptible to buckling than members AB and BC. If adequate bracing prevented buckling, the next expected failure mode would be compressive yielding.

The material is ductile, and the calculated stress is well below its yield strength. Fracture is unlikely to occur before yielding under a gradually applied axial load.

The likelihood of failure could be reduced by increasing the member thickness, adding lateral support, or increasing the cross-sectional moment of inertia.

#### Member DA

Member DA carries 13.889 kN in tension. Its normal tensile stress is approximately 28.345 MPa, which is below the 345 MPa yield strength.

The expected failure mode is yielding. Buckling is not applicable because the member is in tension, and fracture is less likely to occur first because the ductile A500 Grade C steel has a yield strength below its ultimate tensile strength.

The member would begin permanently deforming if its stress reached the yield strength. Fracture would require the stress to increase closer to the ultimate tensile strength of approximately 427 MPa.

The likelihood of failure could be reduced by increasing the cross-sectional area, using steel with a greater yield strength, or reducing stress concentrations near the pin holes.

#### Member BD

Member BD carries 47.467 kN in tension and has the largest internal force in the truss. Its normal tensile stress is approximately 96.871 MPa, which is below the 345 MPa yield strength.

The expected failure mode is yielding because BD is in tension and the A500 Grade C steel is ductile. Buckling cannot occur under tensile loading, and yielding would occur before tensile fracture because the yield strength is lower than the ultimate tensile strength.

Member BD is the most highly stressed member and therefore controls the cross-sectional area used for the entire truss. Its calculated stress is also below the allowable stress of 98.571 MPa obtained using the required safety factor of 3.5.

The likelihood of failure could be reduced by increasing the cross-sectional area of the members, reducing the applied load, or selecting a material with a greater yield strength.

### Summary of Truss-Member Failure Modes

Member AB is expected to fail through buckling because it is the longest compression member.

Member BC is expected to fail through buckling because it carries a large compressive force and is relatively slender.

Member CD is also expected to fail through buckling, although its shorter length makes buckling less likely than in AB or BC. If buckling is prevented, it would eventually fail through compressive yielding.

Member DA is expected to fail through tensile yielding.

Member BD is expected to fail through tensile yielding and is the most highly stressed member.

The original strength calculations followed the assignment instruction to assume that compression members would not fail through buckling. Under that assumption, the compression members would be checked for yielding. In a real truss, a separate buckling analysis and adequate out-of-plane bracing would be necessary.

### Pin Connection Failure

The pins were designed as single-shear connections. In single shear, the complete connection force is carried across one cross-sectional area of the pin, and the average shear stress is calculated by dividing the shear force by the prch0"]}}

The largest pin force was 47.467 kN, or 10.671 kip. The selected 5/8-inch pin had a cross-sectional area of 0.306796 square inches. Dividing the force by the pin area produced an average shear stress of approximately 34.782 ksi.

The hardened tool steel had a given shear yield strength of 170 ksi. Applying the required safety factor of 4 produced an allowable shear stress of 42.5 ksi. Since the calculated stress of 34.782 ksi was below the allowable stress, the pin satisfied the design requirement.

The expected pin failure mode is shear yielding across the single shear plane. If the loading continued to increase after yielding, the pin could eventually experience complete shear fracture. The calculated pin safety factor was approximately 4.888, which was greater than the required value of 4.

The likelihood of pin failure could be reduced by increasing the pin diameter. Another effective modification would be changing the connection from single shear to double shear, which would create two resisting shear planes and reduce the force carried by each plane.

### Time Required

Geometry selection and initial sketch: 30 minutes

Free-body diagrams: 1 hour

Static calculations: 20 minutes

Member and pin design: 2 hours

Fusion 360 modeling: 30 minutes

CAD revisions and mass properties: 20 minutes

Portfolio documentation: 5 hours

Total time: 9 hours 40 minutes

### CAD File Download

The completed Fusion 360 truss and pin assembly can be downloaded below.

[Download the A2 truss CAD files](a2-truss-assembly.zip)

### References

Oberg, E., Jones, F. D., Horton, H. L., and Ryffel, H. H. Machinery’s Handbook, 31st edition. Industrial Press. “Stress and Strain/Working Stress,” page 212, and “Simple Stresses,” pages 216 through 218.

ASTM International. “ASTM A500/A500M: Standard Specification for Cold-Formed Welded and Seamless Carbon Steel Structural Tubing in Rounds and Shapes.”
[ASTM A500/A500M](https://store.astm.org/a0500_a0500m-23.html)

American Institute of Steel Construction. “Steel Availability and Material Specifications.” Modern Steel Construction, June 2022.
[AISC publication](https://www.aisc.org/globalassets/modern-steel/archives/2022/june2022.pdf)
