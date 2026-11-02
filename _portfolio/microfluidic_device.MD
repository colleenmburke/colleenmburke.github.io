---
title: "Microfluidic Device"
excerpt: "Enhanced pinch flow fractionation device for particle separation."
header:
  image: /assets/img/pliers_final.jpeg
  teaser: /assets/img/final_pliers_w_inserts.jpeg
---

## Project Overview

This project focuses on the design and fabrication of a microfluidic device for separating particles by size using enhanced pinch flow fractionation (EPFF). The device is designed to separate two particle-size ranges and collect them through separate outlet streams. The device mold is created using resin printing, then used to cast a PDMS microfluidic device that is bonded to a glass slide.

## Introduction

Pinched flow fractionation (PFF) is a microfluidic technique used to control the flow of particles with varying sizes to sort them into distinct outlets. It works by using two fluid streamlines to align particle positions to known locations in a pinch segment, then amplifying differences in position in a broadening segment to separate the particles. This approach is particularly advantageous for separating particles since it is passive and continuous. It eliminates the need for external (electrical, magnetic, or acoustic) fields, which can be expensive, relies on external equipment, and can harm biological cells. It also eliminates the need for membrane filters, which can cause clogging, impact flow, and require replacement as particles accumulate on the surface. While the most simple PFF use case separates particles of two distinct sizes, it can also be used to separate particles of several distinct sizes.

To accomplish this, two fluid streams – a particle-containing solution and a buffer solution – are introduced through distinct inlets and flow rates using laminar flow. The buffer solution is introduced at a higher flow rate, which essentially presses the particles in the other solution against the microfluidic channel wall as the two streams pass through the pinch segment. In this segment, the particle’s location is known, defined by its center of mass, which is one radius away from the channel wall. The narrow channel then feeds into an open broadening segment, where small differences in particle positions are amplified and the particles spread out. The final particle locations can be estimated and collected by individual outlets for processing.

While PFF can be effective, adequate separation of particles can be hard to achieve and/or require excessively large broadening segments. To amplify separation of particles, enhanced pinch flow fractionation (EPFF) follows the same principles but also includes a geometric modification in the broadening segment. This snakelike structure impacts the distribution of hydraulic resistance and has the potential to increase particle separation distance by up to 70%. This modification further increases separation without increasing the overall size of the broadening segment or introducing external forces.

Some applications that may use PFF and/or EPFF include hematology analysis, to separate the components of [whole blood (red blood cells, white blood cells, and platelets)](https://www.sciencedirect.com/science/article/pii/S1383586626029758), [cancer detection, to separate cancerous cells from non-cancerous cells](https://pubmed.ncbi.nlm.nih.gov/26510401/), and [water quality analysis, to separate microplastics and pollutants suspended in water](https://www.nature.com/articles/s41598-021-89960-4).

## Design

The first set of design choices focused on the overall device geometry. I chose to set the channel height at 240 µm. Using this height prevents more than two of the larger particles from passing through the device at one time, even with the smallest large particles having a diameter of 125 µm. This may improve the accuracy of estimated particle flow using the relevant equations, since each equation generally predicts the flow of a single particle, and particles stacked on top of each other could disrupt the expected results. The possible disadvantage of this choice is that it may make the device more susceptible to clogging and increase resistance; however, since flow is induced at both ends of the device using two inlet pumps and three outlet pumps, this risk may be mitigated under high flow conditions. While this solution still allows the smaller particles to stack on top of each other, with the largest small particles having a diameter of 63 µm, further decreasing the channel height to prevent this would make it impossible for even one larger particle to pass through. Therefore, the current height is still an improvement. This choice guided the selection of the pinch width at a 2:1 ratio, as recommended, and the broad section width at 19 mm to take up the entire device width and exceed the 10:1 ratio. I chose to keep the pinch section 3 mm long.

The next set of design choices focused on the positioning of the snake. I chose to set the beginning of the snake 7.5 mm from the end of the pinch section in the x-direction. This value is in the middle of the recommended 5-10 mm range and serves as a middle benchmark for future studies. I chose to set the beginning of the snake at the maximum particle position plus 7% as a conservative buffer. The maximum possible particle position corresponds to the largest large particle, which has a diameter of 150 µm. Although the error was smaller in some cases, the paper showed differences between measured and calculated particle positions ranging from -4.29% to 5.39% for particles with diameters of 15 and 30 µm. Because of this, I chose to add a somewhat arbitrary 7% buffer to the calculated maximum particle position to account for possible differences between the calculated and actual positions and ensure that all particles are captured. This resulted in a distance of the entrance of the snake of 3.177 mm from the top edge of the device.

I then made additional design choices to maximize the resistance of the enhanced segment (Re) and minimize the resistance of the sink segment (Rs). Overall, the only parameter that can be changed to impact the resistance ratio between the enhancing segment, including the narrow and wide regions, and the sink segment is the width, since the sections have the same overall length. Width has an inverse relationship with resistance, so to maximize Re, I wanted to keep the width of the enhancing section small and the width of the sink section large. Therefore, I chose to make the vertical part of the snake section only 2 mm long as a somewhat arbitrarily small value. Resistance is directly proportional to length, which affects the enhancing and sink sections in the same way, so I chose to make the overall section relatively long, ending 7.5 mm from the outlets. This leaves room for the outlets and allows for possible merging of the flow streams near the end of the device, which may help pull the different particle sizes apart.

The remaining choices involved selecting the lengths of the individual narrow and wide enhancing segments. If the sink section is divided into two zones, the sink section beneath the narrow enhancing segment has a lower resistance than the sink section beneath the wide enhancing segment because the narrow enhancing segment has a larger corresponding sink width. To minimize the resistance of the sink section and maximize the resistance of the enhancing segment, the narrow enhancing section should therefore be longer than the wide enhancing section. However, it cannot be too long, since the particles in the enhancing segment need distance to diffuse apart. To balance these requirements, I chose to place the vertical section of the snake halfway along the length of the segment. Finally, I chose to make the snake section 0.3 mm wide to match the pinch size and ensure accurate and consistent printing. I chose to taper the end of the snake closest to the pinch to a point at a 20° angle to help prevent particles from getting stuck on that surface.

Overall, the experimental variables being most closely observed in this iteration are the position and geometry of the snake segment. These choices deviate from prior iterations and guidance by increasing the length of the narrow section, decreasing the distance of the narrow section from the top of the device, decreasing the channel height so that multiple large particles cannot pass through at once, and tapering the beginning of the snake section. Variables that largely remain unchanged from prior models include the pinch-section size and the distance from the pinch to the snake, which serve as constant variables that may be adjusted later. The exact design of the inlet flows was also not modified, since it was assumed that the particles would be aligned appropriately. The design choices were largely made to maximize Re/Rs and can be compared with other student models who may have prioritized different aspects of the microfluidic device design.

Using these parameters to calculate the resistance gave an Re/Rs value of 2.721. However, this value may be slightly underestimated. The resistance was calculated as if the entire enhancing segment had the width of the wide section, which fails to account for the additional resistance caused by the narrow section of the enhancing region. Including the narrow section would increase Re, and the resulting resistance ratio would therefore be greater than 2.721.

## Interactive Fusion 360 Model

The interactive Fusion 360 model of the assembly is embedded below:

<iframe src="https://a360.co/4BG4py3"
        width="800"
        height="600"
        allowfullscreen="true"
        webkitallowfullscreen="true"
        mozallowfullscreen="true"
        frameborder="0">
</iframe>

## Design Parameters

The current design parameters are shown below with a drawing of the critical parameters.

| Parameter | Value |
|---|---:|
| Minimum small-particle diameter | 53 µm |
| Maximum small-particle diameter | 63 µm |
| Minimum large-particle diameter | 125 µm |
| Maximum large-particle diameter | 150 µm |
| Channel height | 0.24 mm |
| Pinch width | 0.48 mm |
| Broad-section width | 19 mm |
| Pinch length | 3 mm |
| Total snake length | 40 mm |
| Narrow section length | 20 mm |
| Wide section length | 20 mm |
| Narrow section width | 3.177 mm |
| Wide section width | 5.177 mm |
| Resisatnce of enhanced segment | 6.91 $\dfrac{\text{Pa} \cdot \text{s}}{\text{mm}^3}$ |
| Resistance of sink segment | 2.54 $\dfrac{\text{Pa} \cdot \text{s}}{\text{mm}^3}$ |
| Ratio of resistances (Re/Rs) | 2.721 |

## Instructions

The overall steps for creating a microfluidic device with resin printing are:

1. Design the mold in CAD.
2. Resin print the mold.
3. Post-process the mold.
4. Cast PDMS over the mold.
5. Cure the PDMS.
6. Remove the PDMS replica.
7. Bond the PDMS to a glass slide.
8. Connect tubing to the inlet and outlet ports.
9. Prime the device.
10. Test particle separation.

There are some important considerations in this process. First, the mold must be oriented properly in Preform such that the bottom of the mold sits parallel to the build plate since it is the surface associated with the final PDMS bonding surface, which must avoid any roughness to prevent leakage after bonding to glass. Second, the mold must not be over-washed or over-cured, which can decrease dimensional accuracy by absorbing IPA or causing warpage. Finally, the PDMS casting and glass bonding process must proceed with care as to avoid trapping bubbles in the device, which may involve degassing the PDMS mixture multiple times and priming the device before use.

## Discussion

Resin printing is used for microfluidics for multiple reasons. The most compelling reason is that resin printing can create details with small features and high dimensional accuracy. The minimum feature size of the Formlabs Form 4 printer is 50 um, but other printers can achieve even smaller features. This is crucial for microfluidics devices, which can have complex internal networks and weaves. Another reason for using resin printing in microfluidics is that it allows for optical clarity. Printing using transparent filaments allows researchers to visually monitor fluid flow and particle sorting through the device, which fosters a better understanding of device functionality outside of simply measuring particle inflow and outflow. Finally, resin printing is capable of producing non-porous and watertight devices, which are ideal for fluid containment. Since microfluidic devices are generally small, the high cost of resin printing is somewhat less significant.

My design is fully parameterized with respect to particle size and related variables, which would make it easy to scale up or modify the device to handle other particle sizes. If successful, the design may be further modified to accommodate separation of more than two particle sizes, which may be accomplished via the addition of another snake section.

Pinch flow fractionation has been demonstrated to be effective for particles as small as 15 µm; however, applying PFF to increasingly smaller particles may be limited by various factors. One such factor is the size of the particle-containing buffer streamline in the pinch section. The streamline must be smaller than the smallest particle, which can be adjusted by modifying the ratio of inlet flow rates, but it can only be reliably decreased to a certain point. Smaller particle sizes also allow less room for error, meaning that even small variations in particle size can have significant implications. Since particle-flow separation depends on the consistent alignment of particles in the pinch section, which simply amplifies differences, smaller particles may have slightly different centers of mass that are amplified in the broad segment. Smaller particles may also be more likely to stick to imperfections on the device surface and/or bubbles. Additionally, smaller particles may introduce more 3D flow, where particles can stack on top of each other and deviate from the prescribed 2D flow equations that govern microfluidic design. There is not a single numerical limit for particle size, but using microfluidics with increasingly small particle sizes requires more consideration and likely more expensive fabrication techniques and technologies.

## References
1.	Liu L, Lu BW, Wang XY, Fan LL, Wang JC, Zhao L. Multimodal particle separation via negative pressure-based pinch flow fractionation. Separation and Purification Technology. 2026 Nov 16;414:139709. doi:10.1016/j.seppur.2026.139709
2.	Pødenphant M, Ashley N, Koprowska K, Mir KU, Zalkovskij M, Bilenberg B, et al. Separation of cancer cells from white blood cells by pinched flow fractionation. Lab Chip. 2015 Dec 21;15(24):4598–606. doi:10.1039/c5lc01014d PubMed PMID: 26510401.
3.	Elsayed AA, Erfan M, Sabry YM, Dris R, Gaspéri J, Barbier JS, et al. A microfluidic chip enables fast analysis of water microplastics by optical spectroscopy. Sci Rep. 2021 May 18;11(1):10533. doi:10.1038/s41598-021-89960-4
