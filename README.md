# VandalMPC

**VandalMPC** is a pinned fork of the [GNU MPC](http://www.multiprecision.org/mpc/) complex-number arithmetic library, used as a build-time dependency of GDB in the **VandalSDK** toolchain (see `VandalBinUtils`).

This is **not Vandal-authored code**. It is a fork of an existing, independently maintained open-source project, imported here purely so that a specific, known-good version can be built reproducibly as part of the VandalSDK toolchain used by the **Vandalism Engine** game engine.

## Baseline

See `VANDALMPC_BASELINE.txt` for the exact upstream version, tag, and repository this fork was taken from.

## Why this repository exists

VandalSDK's packaged debugger (GDB) links against MPC (built on top of GMP and MPFR) for complex-number arithmetic support. Pinning a specific MPC release as its own repository, alongside the other GDB build dependencies (`VandalGMP`, `VandalMPFR`, `VandalISL`), gives the SDK toolchain build a reproducible, independently versioned source for each dependency, separate from upstream's own release cadence.

This repository exists for internal use while building Vandalism Engine and its SDK. It is not a general-purpose MPC distribution.

## Contributions and issue tracking

This is **not a maintained fork**. ChapmanWorld is not accepting contributions here, and this repository is not the place to raise issues, ask questions, or request features.

* Please do not use this repository as an MPC support forum.
* Please do not raise issues here for upstream MPC bugs.
* Please do not use this repository to report Vandal Engine or VandalSDK bugs.
* Issues with MPC itself should be raised with the upstream MPC project.

## Licensing

MPC is distributed under the **GNU Lesser General Public License (LGPL) version 3 or later**. See `COPYING.LESSER` in this repository for the authoritative upstream license terms.

## Status

Toolchain dependency fork. Tracks a single pinned upstream release for VandalSDK build reproducibility.
