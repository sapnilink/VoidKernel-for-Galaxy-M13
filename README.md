# VoidKernel

A custom Linux kernel for the **Samsung Galaxy M13 (SM-M135FU)** focused on improving performance, responsiveness, thermal behavior, and overall system efficiency while maintaining stability.

> **Current Status:** Early Development

---

## Features

* ✅ Built from Samsung's Android 14 kernel source
* ✅ Successfully boots on the Galaxy M13 (SM-M135F)
* ✅ BFQ I/O scheduler enabled
* 🔄 Additional CPU governor tuning (planned)
* 🔄 Memory management optimizations (planned)
* 🔄 Thermal policy improvements (planned)

---

## Goals

This project aims to explore Android kernel development while improving the user experience on the Galaxy M13.

Planned improvements include:

* Better CPU scheduling
* Reduced unnecessary thermal throttling
* Improved battery efficiency
* Enhanced storage responsiveness
* Memory management tuning
* Clean, maintainable kernel modifications

---

## Device Information

| Property        | Value              |
| --------------- | ------------------ |
| Device          | Samsung Galaxy M13 |
| Model           | SM-M135F           |
| SoC             | Samsung Exynos 850 |
| Architecture    | ARM64              |
| Android Version | 14                 |
| Linux Version   | 4.19.198           |

---

## Build Environment

* Linux
* Clang (Android toolchain)
* GNU Binutils
* Samsung Open Source Release Center kernel source

---

## Building

Clone the repository:

```bash
git clone https://github.com/sapnilink/VoidKernel-for-Galaxy-M13.git
cd VoidKernel-for-Galaxy-M13
```

Configure and build using the appropriate Samsung build configuration or your existing build script.

Example:

```bash
chmod +x build_kernel.sh
./build_kernel.sh
```

The compiled kernel image will typically be located in:

```text
out/arch/arm64/boot/Image
```

---

## Flashing

1. Extract the stock `boot.img`.
2. Unpack using `magiskboot`.
3. Replace the extracted `kernel` with the compiled `Image`.
4. Repack the boot image.
5. Package it into an Odin-compatible TAR archive.
6. Flash through Odin.

**Always keep a copy of your stock boot image before flashing.**

---

## Current Progress

* [x] Kernel successfully compiles
* [x] Successfully boots on physical hardware
* [x] BFQ I/O scheduler enabled
* [ ] CPU governor optimization
* [ ] Scheduler tuning
* [ ] Memory management improvements
* [ ] Thermal tuning
* [ ] Performance benchmarking
* [ ] Battery benchmarking

---

## Contributing

Bug reports, suggestions, and pull requests are welcome.

Please open an issue before making large changes so they can be discussed.

---

## License

This project is based on Samsung's Linux kernel source and is distributed under the terms of the GNU General Public License Version 2 (GPL-2.0). See the LICENSE file for details.

