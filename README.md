# WOOT 2025 Artifact: PLC Memory Dump Dataset

## Overview
This artifact includes raw binary dumps from three PLCs analyzed in our paper:

- `M221_00000000_FFFFFFFF.bin`: 4GB memory dump from Schneider Electric Modicon M221 via UMAS protocol.
- `M241_00000000_4ffdd000.bin`: 1.34GB memory dump from Modicon M241 via UMAS protocol.
- `AB_1756_00000000_0840FFFF.bin`: 138MB dump acquired from Allen-Bradley 1756 PLC via JTAG interface.

## Supporting Visuals
- `AB_1756_00000000_0840FFFF.bin_dH.png`: Entropy visualization of AB 1756 memory.
- `M241_00000000_4ffdd000_80.png`: Visualization of dense memory region in M241.
- `M221_RAP_Regions_cut.png`: Highlight of RAP-mirrored regions in M221.

## Artifact Usage
These files are meant for static analysis only. No execution or system-specific setup is needed. For evaluation:

- Use `binwalk` to extract and verify control logic structures.
- Validate memory classifications (Code/Meta/Padding/Etc.) as discussed in Section 6.
- Observe RAP effects via duplicated data regions across address spaces.

## Notes
- These dumps contain no sensitive information or active firmware keys.
- All memory contents are anonymized and sanitized where applicable.
- File access is read-only and does not pose any execution risk.

## Citation
Please cite the corresponding WOOT 2025 paper when using this dataset.

## Licensing
For evaluation purposes only. Redistribution requires explicit permission.
