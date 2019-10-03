# boardReview
A checklist for reviewing PCB's before sending them out to fab.
## Table of contents
- [boardReview](#boardreview)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
  - [Board Review](#board-review)
      - [Schematic Document Review](#schematic-document-review)
      - [PCB Document Review](#pcb-document-review)
  - [Output Job Review and Execution](#output-job-review-and-execution)
      - [Documentation Outputs (Smart PDFs)](#documentation-outputs-smart-pdfs)
      - [Fabrication Outputs](#fabrication-outputs)
      - [Report Outputs](#report-outputs)
      - [Validation Outputs](#validation-outputs)
  - [Common Past Errors](#common-past-errors)
  - [References](#references)



## Overview

## Board Review
#### Schematic Document Review
 - Are all pins hooked up correctly on all IC's
 - All grounds are routed
 - If a net label GND is being used is it tied to a ground object somewhere
 - All cloned resistors and capacitors have correct
   - Values
   - Digikey part numbers
   - Footprints
 - IC's have correct footprints for part ordered
 - All parts are annotated
 - All components used are in a project included library
 - Compile Project

#### PCB Document Review
 - Import Changes from PCB Project
 - Apply Design Rules (OSH Park)
   - Via hole size
   - Minumum Annular Ring
   - Via trace width
 - Layer Stackup all layers visible
 - No island polygons
 - Ground pins of components aren't floating
 - Polygons with high voltage differences are far enough apart
 - USB lines are placed with differential routing tool
 - All strings are 30mil text height
 - All traces are 10mil w/ exception of differential usb lines
 - Are via stitching groups down and are polygons poured around them
 - Ensure all polygons aren't shelved
 - Design Rule Checks (Zero Errors)
   - No net antennas
   - Double check silk screen to solder mask
   - No unrouted nets
 - Are decoupling capacitors and power cap arrays located as close to pins as possible



## Output Job Review and Execution
#### Documentation Outputs (Smart PDFs)
 - Schematic Prints
 - PCB Prints

#### Fabrication Outputs
 - NC Drill Files
 - Gerber (NOT Gerber X2) Files

#### Report Outputs
 - Bill of Materials
    - Comment
    - Description
    - Designator
    - Footprint
    - Libref
    - Quantity
    - Supplier Part No
    - Value

#### Validation Outputs
 - Design Rules Check
 - Footprint Comparison Report

## Common Past Errors
 - Polygon Pours were shelved
 - Ground Pour not down
 - Island Polygon on a ground pad
 - Wrong size or form factor of components
 - High voltage diff between 2 polygons
 - Grounds for modem not all routed in schematic
 - Output enable pulled wrong direction
 - Output enable pin left floating
 - Vias too small on connector



## References
 - [OSHPARK design rules](https://docs.oshpark.com/design-tools/altium-designer/)