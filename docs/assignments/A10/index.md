# A10 – Lead Screw Translating System

## Objective

![](instructions(1).png)


![](instructions(6).png)


![](instructions(4).png)


![](instructions(3).png)


![](instructions(2).png)


## Leadscrew Diameter (Kadin Bittner)


Minimum Diameter-

![](leadscrew_diameter(4).png)


![](leadscrew_diameter(3).png)


![](leadscrew_diameter(2).png)


![](leadscrew_diameter(1).png)


![](initial_leadscrew.png)


Rotational Speed Range-


![](Rotational_speed(1).png)


![](Rotational_speed(4).png)


![](Rotational_speed(3).png)


![](Rotational_speed(2).png)


Max Torque-


![](torque_evaluation(1).png)


![](torque_evaluation(4).png)


![](torque_evaluation(3).png)


![](torque_evaluation(2).png)



Leadscrew Selection-


![](updated_leadscrew(1).png)



## Nut and Flange Selection (Kadin Bittner)

![](updated_leadscrew(2).png)


## Crosshead Design (Taylor Rockefeller)

Beam Stress Analysis-


![](crosshead_fbd.png)


![](crosshead_knowns.png)


![](symb_stress(1).png)


![](symb_stress.png)


![](numeric_stress.png)


Beam Deflection Analysis-


![](crosshead_fbd.png)


![](crosshead_knowns.png)


![](symb_defl(1).png)


![](symb_defl.png)


![](numeric_defl.png)


Multiview Sketch-

![](multiview_crosshead.jpg)

## Tabulating Costs (Taylor Rockefeller)

| Item Number | Quantity | Name | Cost($)/Item | Cost($) | Purchase Link |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | 2 | Lead Screw | 18.20 | 36.40 | [Lead Screw](https://www.roton.com/product/acme-steel-screw-right-59284/) |
| 2 | 2 | Nut | 23.57 | 47.14 | [Nut](https://www.roton.com/product/acme-bronze-threaded-mount-nut-right-90222/) |
| 3 | 2 | Flange | 49.63 | 99.26 | [Flange](https://www.roton.com/product/flange-steel-flange-89838/) |
|  |  |  | Total Cost: | 182.80 |  |


## Parametric Modeling (Kadin Bittner)

Crosshead-

![](crosshead_build(1).png)


![](crosshead_build(2).png)


![](crosshead_build(3).png)


![](crosshead_build(4).png)


![](crosshead_build(5).png)


![](crosshead_build(6).png)


![](crosshead_build(7).png)


![](crosshead_build(8).png)



Assembly-

![](Assembly(1).png)


![](Assembly(2).png)


## Lessons Learned (Taylor Rockefeller)

Throughout the project, there have been many opportunities to utilize newly learned formulas to develop relationships between the desired load on the tensile tester and the dimensional/material requirements of the components to make the system functional and safe.

Leadscrew Selection: I learned how to determine the minimum leadscrew diameter using axial stress and a factor of safety. I also learned that selecting a leadscrew requires considering thread pitch, rotational speed, torque, and the load capacity of the matching nut.

*Leadscrew Torque and Speed: I learned how the lead of an Acme screw affects the torque and rotational speed required to move a load. Increasing the screw lead increases the linear distance traveled per revolution but generally requires more torque for the same axial load and efficiency.

*Nut and Flange Selection: I learned how to evaluate the bearing stress on the internal threads of a bronze nut and verify that commercially available nuts and flanges can support the required axial load. I also learned the importance of checking mounting dimensions before selecting components.

Crosshead Design: I learned that calculating beam bending and deflection through standard beam bending formulas can leave components smaller than required when tested more accurately with FEA. Selecting a simple beam bending equation gives a good starting point to test and further develop the design.

*Assembly Constraints: I learned the differences between Rigid, Revolute, Cylindrical, and Slider Joints in Fusion 360. I initially had difficulty positioning the leadscrews because the existing joints restricted their movement. Using As-Built Joints and temporarily suppressing conflicting joints helped resolve the problem.

*Frame Design: I learned how to select and assemble T-slot aluminum framing around an existing mechanical assembly. I also learned that the frame must provide enough clearance for the crosshead while maintaining proper alignment between the two leadscrews.

*Teamwork and Design Integration: I learned the importance of coordinating component dimensions between team members. Integrating my partner's crosshead design with commercially available leadscrews, nuts, flanges, and framing required checking dimensions and adjusting the assembly to ensure the components fit together.


## 2157 Portion

## FEA (Kadin Bittner)


Model Setup-


![](FEA_setup.png)


Results to Report-


![](FEA_trialOne(1).png)


![](FEA_trialOne(2).png)


![](FEA_trialOne(3).png)


Optimization Pass #1-

Crosshead thickness was increased to 2 inches.


![](FEA_trialTwo(1).png)


![](FEA_trialTwo(2).png)


![](FEA_trialTwo(3).png)


Optimization Pass #2-

Crosshead thickness was increased to 4 inches.


![](FEA_tiralThree(1).png)


![](FEA_tiralThree(2).png)


![](FEA_tiralThree(3).png)

## Multiview Drawing (Taylor Rockefeller)

Crosshead Drawing-

Crosshead drawing seen below is available in this link for download.

https://github.com/Taylor-Rockefeller-Portfolio/megr2157-portfolio/raw/refs/heads/main/docs/assignments/A10/A10_crosshead_drawing.SLDDRW


![](crosshead_drawing.png)

**[DOWNLOAD CAD FILES AND DRAWINGS](TensileTester.zip)**


## Resources

### Tensile Tester Design References

- [Design, Manufacturing, and Testing of an Open-Source Universal Testing Machine – TU Wien (2024)](https://repositum.tuwien.at/bitstream/20.500.12708/200949/1/Demmel%20Stella%20-%202024%20-%20Design%20manufacturing%20and%20testing%20of%20an%20open-source...pdf)
  - Reference for tensile tester design, mechanical components, and testing methods.

- [Low-Cost Universal Tensile Testing Machine – Hackaday](https://hackaday.io/project/192166-low-cost-universal-tensile-testing-machine)
  - Reference for developing an affordable tensile testing system.

- [FreeLoader – Creative Machines Lab](https://www.creativemachineslab.com/freeloader.html)
  - Reference for the mechanical arrangement of an open-source tensile tester.

### Leadscrews, Nuts, and Flanges

- [Roton – Acme Leadscrew Engineering Data](https://www.roton.com/products/acme-lead-screws-nuts/engineering-data/)
  - Used for leadscrew dimensions, torque calculations, efficiency, and load capacity.

- [McMaster-Carr – 1/2"-10 Acme Steel Leadscrew (99030A405)](https://www.mcmaster.com/99030A405)
  - Reference for the leadscrew specifications and CAD geometry.

- [McMaster-Carr – Bronze Acme Nut (95072A109)](https://www.mcmaster.com/95072A109)
  - Reference for the bronze nut used in the crosshead assembly.

- [McMaster-Carr – Steel Mounting Flange (95082A642)](https://www.mcmaster.com/95082A642)
  - Reference for the mounting flange dimensions and geometry.

### Frame and Structural Components

- [80/20 – 40-4080 T-Slot Aluminum Extrusion](https://8020.net/40-4080.html)
  - Used for selecting the structural frame material and dimensions.

- [80/20 IdeaBuilder](https://ideabuilder.io/)
  - Used for creating and evaluating the T-slot frame layout.

### Engineering Calculations

- [MechanicalC – Column Buckling](https://mechanicalc.com/reference/column-buckling)
  - Reference for evaluating leadscrew buckling under axial compression.

- Machinery's Handbook, 31st Edition
  - Reference for Acme thread geometry, bearing stress, and mechanical design calculations.

- Engineering Mechanics – Screws, Chapters 6/5
  - Course reference for leadscrew loading, torque, and rotational motion.

### Load Measurement

- [OMEGA – LC103B Load Cell Specifications](https://assets.dwyeromega.com/spec/DS-LC103B.pdf)
  - Reference for load cell specifications and force measurement.

