---
title: "Print-in-Place Pliers"
excerpt: "Multimaterial print-in-place pliers with a customizable flexible spring."
header:
  image: /assets/img/hemorrhage_website.png
  teaser: /assets/img/hemorrhage_electronics.png
gallery:
  - image_path: assets/img/hemorrhage_box.png
  - image_path: assets/img/pulsatile_pump.png
  - image_path: assets/img/hemorrhage_electronics_square.png
   
---

## Project Overview

This project explores the design and fabrication of print-in-place components using Fused Filament Fabrication (FFF). Print-in-place parts are assemblies manufactured as a single print, with moving elements such as hinges, joints, and linkages integrated into the design. After printing, the components are activated by manually moving or freeing the joints, eliminating the need for separate assembly. Some designs may also include components that are hand-pressed into place after printing.

Print-in-place components offer several advantages. They can reduce the total number of parts, eliminate fasteners and adhesives, and preserve the strength and continuity of the printed geometry. They can also produce mechanisms that are compacted, folded, or nested during printing and expanded afterward, making it possible to fabricate geometries that might otherwise exceed the printer’s build volume.

Common applications of print-in-place components include:
| Toys and Fidgets | Mechanical Bearings | Folding and Telescoping Objects | Functional Tools |
|---|---|---|---|
| <img src="images/toy.jpg" alt="Print-in-place toy" width="200"> | <img src="images/bearing.jpg" alt="Print-in-place bearing" width="200"> | <img src="images/telescoping-object.jpg" alt="Print-in-place telescoping object" width="200"> | <img src="images/tool.jpg" alt="Print-in-place tool" width="200"> |
| [Toys and fidgets](#) | [Mechanical bearings](#) | [Folding and telescoping objects](#) | [Functional tools](#) |
{% include gallery caption="Print-in-Place Gallery" %}
https://www.printables.com/model/928-yet-another-fidget-infinity-cube-v2
https://www.thingiverse.com/thing:6396239
https://www.printables.com/model/536001-collapsing-master-sword-print-in-place/comments 
https://www.printables.com/model/618534-print-in-place-adjustable-wrench


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

The pliers were designed as a modular, multimaterial mechanism that combines rigid PLA components with a flexible spring component. The spring is positioned at the center of the pliers and connects the four PLA components: two handles and two jaws. Dovetail joints retain the spring and allow it to be pressed into place without requiring adhesives or additional fasteners. The dovetail joints use an approximately 4:1 angle, a common proportion that provides strong tensile resistance while still allowing the parts to be assembled by hand.
Several spring iterations were produced to evaluate the effects of infill density and line width on flexibility, strength, and ease of replacement. These variations made it possible to identify a spring configuration that provided sufficient restoring force for the pliers while remaining easy to remove and replace for different applications.
The first iterations used a 45-degree infill orientation in the flexible component. This orientation restricted movement along the desired axis and prevented the pliers from closing properly. These versions also used more cross-hatched infill lines with smaller line widths, which increased flexibility but made the spring more susceptible to breaking. Later iterations used a 90-degree infill orientation and thicker infill lines. Although these designs used fewer lines, they produced a stronger spring that allowed movement along the correct axis and improved the component’s durability.
Early versions of the pliers also featured thin geometries that allowed the jaws to shift out of plane. To address this issue, later iterations increased the thickness of both the rigid and flexible components along the z-axis. This created a more secure fit between the parts, reduced lateral movement, and prevented the jaws from slipping out of alignment during use.

{% include gallery caption="Automated Hemorrhage Resuscitation Gallery" %}

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

## Final Design
