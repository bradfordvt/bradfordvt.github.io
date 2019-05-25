---
title: "IEEE Std 1687 - IEEE Standard for Access and Control of Instrumentation Embedded within a Semiconductor Device"
excerpt: "A methodology for accessing instrumentation embedded within a semiconductor device, without defining the instruments or their features themselves, via the IEEE 1149.1TM test access port (TAP) and/or other signals, is described in this standard. The elements of the methodology include a hardware architecture for the on-chip network connecting the instruments to the chip pins, a hardware description language to describe this network, and a software language and protocol for communicating with the instruments via this network."
url: page.href
header:
  image: /assets/images/IJTAG_Logo.png
  teaser: assets/images/IJTAG_Logo.png
gallery:
  - url: /assets/images/Example IEEE 1687-2014_IEEE 1149.1-2013 Topology.png
    image_path: assets/images/Example IEEE 1687-2014_IEEE 1149.1-2013 Topology.png
    alt: "placeholder Example IEEE 1687-2014_IEEE 1149.1-2013 Topology"
  - url: /assets/images/TAP Finite State Machine.png
    image_path: assets/images/TAP Finite State Machine.png
    alt: "placeholder TAP Finite State Machine"
  - url: /assets/images/Single-module 1687 network architecture.png
    image_path: assets/images/Single-module 1687 network architecture.png
    alt: "placeholder Single-module 1687 network architecture"
  - url: /assets/images/Multiple-module 1687 network.png
    image_path: assets/images/Multiple-module 1687 network.png
    alt: "placeholder Multiple-module 1687 network"
  - url: /assets/images/Raw instrument.png
    image_path: assets/images/Raw instrument.png
    alt: "placeholder Raw instrument"
  - url: /assets/images/Single TDR.png
    image_path: assets/images/Single TDR.png
    alt: "placeholder Single TDR"
---
*The following is an excerpt from the IEEE Std 1687-2014 publication.*

# Scope
This standard develops a methodology for access to embedded instrumentation, without defining the instruments or their features themselves, via the IEEE 1149.1TM test access port (TAP) and additional signals that may be required. The elements of the methodology include a description language for the characteristics of the features and for communication with the features, and requirements for interfacing to the features.

# Purpose
IEEE Std 1149.1 specifies circuits to be embedded within a semiconductor device to support board test; namely, the TAP, TAP Controller, and a number of internal registers. 1 In practice the TAP and TAP Controller are being used for other functions well beyond boundary scan in an ad-hoc manner across the
industry to access a wide variety of embedded instruments. The purpose of the IEEE 1687 initiative is to provide an extension to IEEE Std 1149.1 specifically aimed at using the TAP to manage the configuration, operation, and collection of data from this embedded instrumentation circuitry.

# Background
There exists the widespread use of embedded instrumentation such as built-in self-test (BIST) engines, complex I/O characterization and calibration, embedded timing instrumentation, etc.), each of which is accessed and managed by a variety of external controllers using a variety of mechanisms and protocols. Therefore, a need exists for standardization of these methods in order to facilitate an efficient and orderly process for the preparation of tests that access and control these embedded instruments. Given the widespread use of IEEE 1149.1 TAP and boundary-scan architecture as a gateway to many internal test, debug, and programming features, it is logical to build upon the foundation of the boundary scan standards (IEEE Std 1149.1-1990 [B2], IEEE Std 1149.1-2001, IEEE Std 1149.1-2013 , IEEE Std 1149.4TM-2010 [B3], IEEE Std 1149.6TM-2010 [B4], IEEE Std 1532TM-2002 [B5], and IEEE Std 1500TM-2005) to support TAP-based access to internal device test features in a standardized manner. 2 IEEE Std 1149.1-2013 extended previous versions of that standard to include procedural access to reconfigurable test data registers (TDRs) accessible via the TAP. IEEE Std 1687 describes an instrument-centric approach to this problem that allows retargeting from instrument ports through a wide variety of on-chip network configurations (of which IEEE Std 1500 is one example) to a device interface (of which the TAP is one example). Like IEEE Std 1500, IEEE Std 1687 specifies how to build a conformant on-chip network while not forcing a specific device interface to the network. IEEE Std 1687 has taken a more descriptive than prescriptive approach for specifying the on-chip network, thus allowing many existing architectures to conform.

This standardization effort is intended to address the access to on-chip instrumentation, not the instruments themselves. The elements of standardized access include the following:
1. The hardware architecture for connecting instruments to the TAP via a serial access network and/or to other interfaces via a serial or parallel access network,
2. A hardware description language (HDL) that documents this access network between theinstruments and device interfaces, and
3. A procedure description language that documents the operation of the instruments.

Items that have been specifically included in the scope of the standard include the application of instrument-level procedures retargeted through various levels of hierarchy, the retargeting of intellectual property (IP)-level patterns to device-level TAP patterns, and the documentation of the connection of instruments to other (non-TAP) interfaces.
Items that have been excluded from the scope of the standard are the detailed off-chip protocols for instrument communication over non-TAP interfaces, synchronized interoperation between instruments, and the assurance of reusability of chip-level patterns at board or system levels.

The goal of IEEE Std 1687 is to facilitate the use and reuse of internal instrumentation by providing a standard yet flexible network architecture for accessing the instruments and standard descriptions of both the network and the operation of the instruments. Given the considerable number of devices containing internal instruments that are already available, this standard has made every reasonable attempt to provide support for the description of commonly used legacy implementations. The standard also supports forward-
looking architectures that are scalable and uniform in their approach to accessing embedded instruments in a hierarchical manner.

{% include gallery caption="This is gallery of key concepts being investigated by the working group." %}

[https://standards.ieee.org/standard/1687-2014.html](https://standards.ieee.org/standard/1687-2014.html)
