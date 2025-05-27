# WOOT'25 Artifact: PLC Memory Dump Dataset

# Artifact Abstract

This artifact provides raw PLC memory dumps that support partial verification of the memory analysis presented in our WOOT '25 paper. The dataset includes memory acquired from three PLCs using protocol-based or physical access methods. It is intended for static analysis and does not require execution.

Users may explore the memory layout characteristics, such as code regions, metadata, padding, and address aliasing (RAP), and validate their presence using standard binary analysis tools (e.g., binwalk). The files are safe for offline analysis and do not contain active or malicious code.

These binary images are static, do not contain malicious code, and are safe to analyze.


# Artifact Contents

- **M221**: Schneider Electric (Modbus UMAS) - Full 4GB dump.
- **M241**: Schneider Electric (Modbus UMAS) - Partial (64MB) dump.
- **AB 1756**: Allen-Bradley (JTAG).



## Access Instructions
The files are hosted on a public [GitHub repository](https://github.com/dndusdndus12/plc_dump).

```
- Binary data can be inspected using `binwalk`, `xxd`, or custom scripts.
- Visual comparison with results in Sections 4–6 of the paper is recommended.
- Observe RAP effects via duplicated data regions across address spaces.
```


## Overview
This artifact includes raw binary dumps from three PLCs analyzed in our paper:

- `/SE/M221_00000000_FFFFFFFF.bin`: 4GB memory dump from Schneider Electric Modicon M221 via UMAS protocol.
- `/SE/M241_00000000_4ffdd000.bin`: 1.34GB memory dump from Modicon M241 via UMAS protocol.
- `/AB/AB_1756_00000000_0840FFFF.bin`: 138MB dump acquired from Allen-Bradley 1756 PLC via JTAG interface.

## Supporting Visuals
- `/SE/M221_RAP_Regions_cut.png`: Highlight of RAP-mirrored regions in M221.
- `/SE/M241_00000000_4ffdd000_80.png`: Visualization of dense memory region in M241.
- `/AB/AB_1756_00000000_0840FFFF.bin_dH.png`: Entropy visualization of AB 1756 memory.

## Citation
Please cite the corresponding WOOT 2025 paper `TBD` when using this dataset.


