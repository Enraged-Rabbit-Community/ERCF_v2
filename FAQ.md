# ERCF v2 FAQ

### Q1. Will there be kits available for ERCF V2, and where can we get them?
LDO and  a number of vendors will have kits available for ordering in the coming months. Full kits will be available sometime in late 1st quarter of 2024.

### Q2. I bought an ERCF v1.1 kit. Will this be compatible?
ERCF v1.1 kits will be compatible with V2 with some additional hardware and fastener kits. We have made every effort to utilize as much of the original kit as possible. Upgrade kits will be available at various select vendors in the coming months. Be aware the kits will be less a single channel for the V2 upgrade to accommodate the wider filament blocks.

### Q3. Will ERCF come with a filament cutter?
ERF (Enraged Rabbit Filametrix) has been developed and optimized to work with ERCF V2. Although dozens of toolhead designs exist, the initial launch will be based on the Voron Stealthburner with Clockwork 2. There are numerous versions of toolheads, and the library of STLs will be expanding to support the greater community. We also encourage the public to develop and test their versions and to submit them to be included in our collection. More extruders are being actively developed and will be released in the coming months.

### Q4. I see that ERCF comes with a built-in buffer. Is this required or optional?
Enraged Rabbit Cotton Tail (ERCT) has been specifically designed to give the best multi-filament experience for V2; however, it is completely modular and optional for your build. You can choose to use other buffer designs; our software design is flexible. One of the stand-out features of ERCT is the ability to use a pre-gate sensor, which is designed specifically to improve Endless Spool performance.

### Q5. Do I have to order a kit, or can I self-source this? Is there a BOM?
Kits are expected to be available in the 1st quarter of 2024. Our BOM will list all the parts needed with a wizard to help you customize the kit to your requirements. The BOM will be found through our GitHub listing with links to vendors who can provide parts for self-sourcing.

### Q6. When and where will the v2 BOM be located? Is it with the same BOM as V1.1?
The V2 BOM will located on the GitHub page after RC1 has been released. This will be at a new location, not the old ERCF V1.1 site.

### Q7. What tool heads will this support?
Initially, ERCF V2 will be released with ERF (Filametrix) for Voron Stealthburner CW2 toolheads. Active development and collection of many popular hotends to companion with it is underway and will be part of the GitHub Repository. Alternative extruders are also being developed or being sourced with a cutting head. ERCF V2 also supports sensorless systems but is less reliable than a filament-cutting solution.

### Q8. Is the BTT MMB board required, or will older Easy BRD still work with V2? 
BTT MMB is the new standard and recommended board for V2. Easy BRD and alternatives will work for most of V2's features, but some of the new features, like pregate sensors and, in some cases, RGB lighting, will require a board with enough endstop and LED inputs to operate fully.

### Q9. Where can I get support for my ERCF V2 build?
ERCF V2 is built on a community of supporters and other experienced builders. Visit [VoronDesign #ercf_questions](https://discord.com/channels/460117602945990666/909743915475816458) Discord server for any questions and support issues where members of the V2 team as well as the community is there to help.

### Q10. Is there a build guide on assembling and calibrating my new ERCF?
Yes, a build guide is available in PDF format on the GitHub repository.

### Q11. Will ERCF V2 work with other non-Voron printers?
ERCF V2 currently works with most Klipper-based printers. The current exceptions are sandboxed builds of Klipper made proprietary by some companies and do not have the ability to add third-party software. Consult your product's support pages to see if there are ways to add third-party add ons, which may allow you to install the necessary software for ERCF V2 to work with your printer.

### Q12. I modified by V1.1 with TripleDecky, SturdyBunny, Springy, etc.  Do I already have a ERCFv2?
No. While ERCFv2 incorporates many "beta" modification projects from the team, it also includes many refinements, some subtle and some not.  These changes were all necessary to guarantee ERCFv2 would work together.  The only exception to this is that TripleDecky C7.0 filament blocks are identical to those in ERCFv2.  Other than those you are strongly encouraged to reprint and re-build to ensure you have a supported platform. In addition Happy Hare, with a vendor and version set to "ERCF" and "2.0" will correctly support ERCFv2 but this mode will not necessarily work with a heavily modified v.1.

