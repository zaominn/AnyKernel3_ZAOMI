# AnyKernel3 Kernel Installer

This flash package separates device/product behavior from the upstream
AnyKernel3 engine:

- `anykernel.sh` declares the boot-image operation and installer profile.
- `tools/installer-profile.sh` owns serial-lock preparation, safety checks and
  optional module installation.
- `tools/ak3-core.sh` remains the licensed AnyKernel3 engine by osm0sis.

The split keeps the original flashing behavior and installer information while
making installer changes reviewable without modifying the generic engine.
