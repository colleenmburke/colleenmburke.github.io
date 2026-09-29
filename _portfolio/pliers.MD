---
title: "Print-in-Place Pliers"
excerpt: "Multimaterial print-in-place pliers with a customizable flexible spring."
header:
  image: /assets/img/pliers_final_w_inserts.jpeg
  teaser: /assets/img/pliers_final.jpeg
---

## Project Overview

This project explores the design and fabrication of print-in-place components using Fused Filament Fabrication (FFF). Print-in-place parts are assemblies manufactured as a single print, with moving elements such as hinges, joints, and linkages integrated into the design. After printing, the components are activated by manually moving or freeing the joints, eliminating the need for separate assembly. Some designs may also include components that are hand-pressed into place after printing.

Print-in-place components offer several advantages. They can reduce the total number of parts, eliminate fasteners and adhesives, and preserve the strength and continuity of the printed geometry. They can also produce mechanisms that are compacted, folded, or nested during printing and expanded afterward, making it possible to fabricate geometries that might otherwise exceed the printer’s build volume.

Common applications of print-in-place components include:

### Toys and Fidgets

[![Infinity Cube](/assets/img/infinity_cube.png)](https://www.printables.com/model/928-yet-another-fidget-infinity-cube-v2)

Print-in-place toys and fidgets commonly use integrated hinges, joints, and articulated sections.

### Mechanical Bearings

[![Mechanical Bearing](/assets/img/ball_bearing.png)](https://www.thingiverse.com/thing:6396239)

Print-in-place bearings demonstrate how rolling components can be manufactured as a single assembly.

### Folding and Telescoping Objects

[![Collapsing Master Sword](/assets/img/sword.png)](https://www.printables.com/model/536001-collapsing-master-sword-print-in-place/comments)

Folding and telescoping objects can expand after printing, allowing larger designs to fit within a printer’s build volume.

### Functional Tools

[![Adjustable Wrench](/assets/img/wrench.png)](https://www.printables.com/model/618534-print-in-place-adjustable-wrench)

Print-in-place tools can integrate handles, hinges, and linkages without requiring separate fasteners.

Despite these benefits, print-in-place designs present several challenges. Moving parts must be printed with sufficient clearance to prevent them from fusing together, while still remaining secure and functional. The ability to print a mechanism without supports also depends on factors such as its geometry, orientation, bridging requirements, and material properties. In addition, tolerances can vary between printers, materials, and slicer settings, meaning that each design may require calibration and testing to achieve reliable movement.

To address these challenges, this project incorporates multimaterial printing. PLA and PETG can be used together in mechanically interlocking designs because they do not strongly adhere to one another, allowing components to separate cleanly while maintaining precise geometry. However, this combination requires careful control of clearances and may still require hand assembly. A second option is to combine PLA, or another rigid material, with TPU 95A. PLA provides structural support, while TPU adds flexibility and can accommodate movement and minor variations in fit. In this project, the components are fabricated separately and hand-pressed together after printing. This approach combines the strength of a rigid material with the adaptability of a flexible one, creating a mechanism that is more tolerant of variation than a fully rigid, single-material design.

## Interactive Fusion 360 Model

The interactive Fusion 360 model of the assembly is embedded below:

<iframe src="https://a360.co/4rwYo26"
        width="800"
        height="600"
        allowfullscreen="true"
        webkitallowfullscreen="true"
        mozallowfullscreen="true"
        frameborder="0">
</iframe>

## Design Purpose and Features

The pliers were designed as a modular, multimaterial mechanism that combines rigid PLA components with a flexible spring insert. The assembly consists of two handles, two jaws, and a centrally located spring that connects the four PLA components. The spring is retained using dovetail joints, allowing it to be pressed into place without adhesives or additional fasteners. The joints use an approximately 4:1 taper, providing sufficient tensile resistance while still allowing the components to be assembled and removed by hand.

Several spring iterations were produced to evaluate the effects of infill density, line width, and infill orientation on flexibility, strength, and replaceability. These variations helped identify a spring configuration that provided adequate restoring force while remaining durable and easy to replace for different applications.

The first iteration used components that were only 2 mm thick. This caused the jaws to misalign and allowed the pliers to move primarily along the x-axis rather than in the intended opening-and-closing direction. The dovetail joints also had excessive clearance. Although the spring could be pressed into place easily, it was not retained securely. The overall geometry was larger than necessary for picking up a resistor, making the pliers difficult to hold. In addition, the individual lines within the flexible spring were too thin and prone to breaking. The spring used a 45-degree infill orientation, which did not provide flexibility along the desired axis.

<table>
  <tr>
    <td align="center">
      <img src="/assets/img/pliers_1.jpeg" alt="First Iteration Pliers Image" width="400">
    </td>
    <td align="center">
      <img src="/assets/img/pliers_1_gif.gif" alt="First Iteration Pliers GIF" width="400">
    </td>
  </tr>
</table>

The second iteration increased the overall thickness of the plier components to 6 mm and reduced the clearance at the dovetail joints. The smaller geometry improved the ergonomics and made the pliers easier to hold. The thicker flexible spring also used wider infill lines, which improved its durability. Changing the infill orientation to 90 degrees allowed the spring to flex in the correct direction. However, the reduced joint clearance made the fit too tight. The spring could not be installed by hand and required a hammer or the butt of a screwdriver to press it into place. Removing the spring also required considerable force, which began to tear the PLA components. As a result, the flexible insert could not be replaced effectively without risking damage to the pliers.

<table>
  <tr>
    <td align="center">
      <img src="/assets/img/pliers_2.jpeg" alt="Second Iteration Pliers Image" width="400">
    </td>
    <td align="center">
      <img src="/assets/img/pliers_2_closeup.jpeg" alt="First Iteration Pliers Delamination" width="400">
    </td>
  </tr>
</table>

The final iteration slightly increased the dovetail clearance to improve assembly and disassembly. The overall thickness in the z-direction was also increased to 8 mm, reducing the remaining misalignment between the jaws. Small ridges were added to the inner tips of the jaws to improve their ability to grip and pick up small components such as resistors. Multiple flexible spring inserts were printed with different infill percentages, allowing the stiffness and restoring force of the pliers to be adjusted for different applications. The increased joint clearance allowed the inserts to be pressed into place and removed by hand while still retaining them securely during use.

<table>
  <tr>
    <td align="center">
      <img src="/assets/img/pliers_final_w_inserts.jpeg" alt="Final Iteration Pliers with Inserts" width="400">
    </td>
    <td align="center">
      <img src="/assets/img/pliers_final_gif.gif" alt="Final Iteration Pliers Gif" width="400">
    </td>
  </tr>
</table>

### Specifications

| Component      | Size       |
|----------------|------------|
| Jaw length     | 20 mm      |
| Jaw capacity   | 5 mm       |
| Total length   | 50 mm      |
| Handle length  | 30 mm      |
| Jaw surface    | Serrated   |

### Printer Settings

| Print setting                  | PLA print setting | TPU 95A print setting |
|--------------------------------|-------------------|-----------------------|
| Nozzle                         | 0.6 mm            | 0.6 mm                |
| Vertical shell perimeters      | 3                 | 4                     |
| Horizontal shell solid layers  | 3                 | 0                     |
| Infill pattern                 | Honeycomb         | Grid                  |
| Infill density                 | 15%               | 18%                   |
| Infill angle                   | 45 degrees        | 90 degrees            |
| Infill extrusion width         | 100%              | 200%                  |
| Solid infill threshold         | 0                 | 5 mm                  |
