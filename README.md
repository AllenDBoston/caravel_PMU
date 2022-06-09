# FPGA Programming Management Unit

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![UPRJ_CI](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml) [![Caravel Build](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml)

## Description
The Programming Management Unit will serve as a macro that can be placed near a FPGA to handle bitstream loading. While the primary functionality of the PMU is to load a bitstream into an FPGA Core it will also incorporate some hardware security and integrity features. This is in response to the need for OpenFPGA to be able to incorporate some hardware security IPs to FPGA designs. To accurately access the level of protection the security features provide to the FPGA/FPGA bitstream, an iterative approach to the PMU design will be taken starting with version one. The iterative approach is currently defined by a threat model shown in Figure 1. As of today the primary objectives of the PMU is to accurately transfer bitstream data to the core and protect the IP that lies within a bitstream using AES. The final version of the PMU will resemble a RISC-V core that incorporates all the features of the previous PMU versions as well as post fabrication feature implementation and programming of multiple FPGA configuration chains.

<p>
  <img src="/docs/figures/ThreatModel.png">
</p>
