---
title: "Upcoming SJTAG Newsletter Green Papers"
categories:
  - Markup
tags:
  - SJTAG
  - IEEE 1149.1-2013
  - IEEE Std 1687
  - I2C
  - SPI
  - Boundary-scan
  - Board Test
  - System Test
  - Embedded Instruments
---
Green Paper  
By Bradford G. Van Treuren, SJTAG Chair Emeritus

In the coming editions of the SJTAG Newsletter, we will be exploring some of the problem domains exhibited by various SJTAG Use Cases which may or may not have solutions available with existing industrial standards.  The intent of these Green Papers is to inspire collaboration and dialog between members of this industry; also to help educate you to the unique difficulties faced moving forward with providing support at the board and system level for testing, programming, and debugging systems with various levels of complexity.

The first paper presents the contrast between two groups of Use Cases where one domain requires the implicit definition of access while the second requires the explicit definition of access to a target entity.  It will inform you to the broad behavioral requirements on what was presented in the last newsletter for supporting Access Links and Data Links.

The second paper discusses the contrast between the need to support pre-generated tests, which are able to be replicated for factory testing, versus the need to support interactive configuration and control of an entity during Design Verification Test, Hardware Debugging, and Software Debugging.  Both aspects are required to support the introduction of new designs and SJTAG needs to be able to support both domains.

The third paper uncovers how the JTAG based processor debug technology is really a specialized case of an embedded instrument that can be supported at not only the board level, but also at the system level.  There are some unique aspects to this instrumentation that provide keen insight into the problem domain of JTAG Bridges to other protocols controlling instruments in devices.

The fourth and final paper in this series explains how a special class of instrument implementations used inside FPGA devices present problems for current standards targeting this problem domain.  These special instruments leverage Intellectual Property provided by the FPGA vendor, which leverages the internal processor bus yielding an indirect access to the back end instrument from the JTAG interface.  Thus, the description of the instrument behavior is masked by the generic JTAG interface instrumentation to the internal processor bus.

We hope you will find this series of Green Papers to be useful in your understanding of this fascinating problem domain of SJTAG.

*Copyright © 2014, Bradford Van Treuren*
