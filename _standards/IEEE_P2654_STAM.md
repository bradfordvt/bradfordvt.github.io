---
title: "IEEE P2654 - Standard for System Test Access Management (STAM) to Enable Use of Sub-System Test Capabilities at Higher Architectural Levels"
excerpt: "This standard addresses use/ reuse of test assets in system context by: 1) defining a representation for behavioral descriptions of pertinent sub-assembly interfaces and of relevant data and protocol transformations; 2) defining methods for utilizing such representations to enhance management of and access to said test assets. In conjunction with existing methods for test access and test management, this will allow the coordination and control of a variety of digital interfaces to devices, boards, and sub-systems to extend test access to board and system levels. This standard does not replace or provide an alternative to existing test interface standards, but aims instead to enable their usage throughout the hierarchy of systems."
url: page.href
header:
  image: /assets/images/P2654_Logo.png
  teaser: assets/images/P2654_Logo.png
gallery:
  - url: /assets/images/IllustrativeSJTAGSystem.png
    image_path: assets/images/IllustrativeSJTAGSystem.png
    alt: "placeholder Illustrative SJTAG System"
  - url: /assets/images/SJTAGVisualization.png
    image_path: assets/images/SJTAGVisualization.png
    alt: "placeholder SJTAG Visualization"
  - url: /assets/images/EMBISTEcoSystemforDataTransfer.png
    image_path: assets/images/EMBISTEcoSystemforDataTransfer.png
    alt: "placeholder EMBIST EcoSystem"
  - url: /assets/images/SystemLevelAccessDataPathConcept.png
    image_path: assets/images/SystemLevelAccessDataPathConcept.png
    alt: "placeholder System Level Access Concept"
---
# Scope
This standard addresses use/ reuse of test assets in system context by: 1) defining a representation for behavioral descriptions of pertinent sub-assembly interfaces and of relevant data and protocol transformations; 2) defining methods for utilizing such representations to enhance management of and access to said test assets. In conjunction with existing methods for test access and test management, this will allow the coordination and control of a variety of digital interfaces to devices, boards, and sub-systems to extend test access to board and system levels. This standard does not replace or provide an alternative to existing test interface standards, but aims instead to enable their usage throughout the hierarchy of systems.

# Purpose
The purpose of this standard is to facilitate a means to seamlessly integrate component access topologies, interface constraints, and other dependencies at the board and system level by using standardized descriptions focusing on topology, interfaces and behavior (as opposed to physical structure). This will ease the burden on those preparing test, maintenance and support applications, including Automatic Test Pattern Generation (ATPG), in particular where the application requires to co-ordinate control of and data transfer through multiple interfaces and/or protocols. Typically, the providers of these conforming descriptions are the producers of integrated circuits, printed circuit boards or sub-systems, including, for example, intellectual property cores in a System on Chip (SoC), with digital interfaces that are intended to be used in an automated fashion within a larger assembly. This standard will also include a methodology to ensure access to particular destination registers in the correct time order.

# Need
Standards exist to access diverse feature sets for device-level test and instrumentation. However, there is currently no standard that provides for the aggregate management and coordination of such standards for higher level assemblies, such as boards or systems.

Users of board- and system-level automated test equipment need to be able to command their tools and instruments, identifying the dependencies, constraints, and required coordination. Embedded applications also need to have access to these same instruments at higher levels during run-time.

Standardization is needed to facilitate such automation and to enhance testability, test coverage, and diagnostics resolution in the higher level assemblies.

{% include gallery caption="This is gallery of key concepts being investigated by the working group." %}

[http://www.sjtag.org](http://www.sjtag.org)
[https://standards.ieee.org/project/2654.html](https://standards.ieee.org/project/2654.html)
