# No Bypass Mod

Removes the bypass from the end block, so that upgrading from ERCF v1.1 with Sturdy Bunny doesn't require new extrusion to be cut.
This is an alternative to using a bypass with the [Thumper Blocks](../../kieraneglin/Thumper-Blocks).

## BOM

Identical to V2 BOM, minus 1x ECAS fitting.

## Software Configuration

At present, it is recommended to setup Happy Hare as a custom MMU, since ERCF v2 expects a bypass block.
It might be necessary to tune these settings. Additionally, set `cad_bypass_offset: 0` in your mmu_parameters config file.
