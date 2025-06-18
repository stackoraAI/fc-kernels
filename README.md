# fc-kernels

## Overview

This project automates the building of custom Linux kernels for Firecracker microVMs, using the same kernel sources as official Firecracker repo and custom configuration files. It supports building specific kernel versions and uploading the resulting binaries to a Google Cloud Storage (GCS) bucket.

## Prerequisites

- Linux environment (for building kernels)

## Building Kernels

1. **Configure kernel versions:**
   - Edit `kernel_versions.txt` to specify which kernel versions to build (one per line, e.g., `6.1.102`).
   - Place the corresponding config file in `configs/` (e.g., `configs/6.1.102.config`).

2. **Build:**
   ```sh
   make build
   # or directly
   ./build.sh
   ```
   The built kernels will be placed in `builds/vmlinux-<version>/vmlinux.bin`.

## License

This project is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details. 