Scarlet
=======
__Scarlet__ and its related libraries are aiming to provide functionality to convert, export and import various types of game data. They are written in C# and based on the .NET Framework.

Disclaimer
==========
This project is still incomplete and work-in-progress. Functionality will change, be added or removed, and all interfaces, calling conventions, etc. should be considered subject to change.

Parts
=====
* __Scarlet__: Common main library (required)
* __Scarlet.IO.ImageFormats__: Library for image file format conversion (requires Scarlet)
* __Scarlet.IO.ContainerFormats__: Library for container/archive management (requires Scarlet)
* __Scarlet.IO.CompressionFormats__: Library for handling compressed data (requires Scarlet)
* __ScarletTestApp__ (ScarletConvert): Sample converter application implementation (requires all the above)

Formats
=======
File formats that can be loaded and exported/extracted by the libraries as of [this commit](https://github.com/xdanieldzd/Scarlet/tree/a9f0be8b29c77166f138fa4308f83cd932ce270e) contain the following:

* __Images__
 * DDS (DXTx and PVRx; ex. Skullgirls 2nd Encore, PS Vita)
 * DMPBM (ex. Shin Megami Tensei: Devil Survivor Overclocked)
 * GBIX (ex. K-ON! Houkago Live, PSP version)
 * GXT (various PlayStation Vita games)
 * KSLT (ex. Dead or Alive Xtreme 3: Venus, possibly more Koei Tecmo games)
 * NMT (ex. Disgaea 4, PS Vita version, possibly more Nippon Ichi Software games)
 * SHTX (ex. Danganronpa Another Episode)
 * SHTXFS (ex. Danganronpa Another Episode)
 * STEX (ex. Etrian Odyssey IV, Shin Megami Tensei IV, possibly more Atlus games)
 * TEX (various Capcom games)
 * TID (ex. Hyperdimension Neptunia ReBirth 1, PC _and_ PS Vita versions, possibly more Idea Factory/Compile Heart/Felistella games)
 * TMX (various Atlus games)
 * TX2 (ex. Phantom Brave, PS2 version, various other Nippon Ichi Software games)
 * TXF (ex. Disgaea 4, PS3 version, possibly more Nippon Ichi Software games)
 * TXG (ex. Sakurasou no Pet na Kanojo, PSP version)
   * XGTL (wrapper around multiple TXGs)
    * CBG (wrapper around XGTL)
 * TXP (ex. Z.H.P: Unlosing Ranger vs Darkdeath Evilman, Disgaea 2 PSP, Disgaea Infinite, possibly more Nippon Ichi Software games on PSP)
 * VTXP (ex. Punchline, PS Vita; _not_ the same as, nor related to TXP above)
* __Containers__
 * FMDX (ex. K-ON! Houkago Live, PSP version)
 * NISPACK (various Nippon Ichi Software games)
 * NSAC (ex. Disgaea 4, PS Vita version, possibly more Nippon Ichi Software games)
 * PSPFS_V1 (ex. Phantom Brave, PSP version, possibly more Nippon Ichi Software games)
 * UKArc/PAC (ex. Dengeki Bunko: Fighting Climax, PS Vita version)
* __Compression__
 * GZip (generic; also ex. Dengeki Bunko: Fighting Climax, PS Vita version)
 * NIS LZS (ex. Disgaea 4, PS3 and PS Vita versions)
 * Nintendo DS LZSS-0x10 (ex. Shin Megami Tensei: Devil Survivor Overclocked)

Note that support for these is not 100% complete (especially Capcom TEX is lacking), as well as the unintentional bias towards NIS games.

Acknowledgements
================
* PVRTC texture decompression code ported from [PowerVR Graphics Native SDK](https://github.com/powervr-graphics/Native_SDK), Copyright (c) Imagination Technologies Ltd.
 * see *\Scarlet\Drawing\Compression\PVRTC.cs* and *LICENSE.md*
* Includes [NetRevisionTool](http://unclassified.software/apps/netrevisiontool) by Yves Goergen for injecting Git revision information
* Initial VTXP format notes by [BlackDragonHunt](https://github.com/BlackDragonHunt)
* Texture swizzle logic reverse-engineering and original C implementation by [FireyFly](https://github.com/FireyFly)
* Sample files, testing and moral support by [Ehm2k](https://twitter.com/Ehm2k)

See Also
========
* [GXTConvert](https://github.com/xdanieldzd/GXTConvert), a dedicated GXT-to-PNG converter (might not have feature parity with Scarlet)
