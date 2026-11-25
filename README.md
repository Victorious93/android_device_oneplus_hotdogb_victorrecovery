# android_device_oneplus_hotdogb_victorrecovery

VictorRecovery device tree for the **OnePlus 7T (`hotdogb`)**.

> ## ⚠️ UNTESTED, EXPERIMENTAL
> This tree has **not been built or tested by us on a device**. Nothing here is claimed to boot, decrypt or flash correctly.
> **You can brick your phone.** Flashing recoveries needs an unlocked bootloader (unlocking **erases all data** and may void your warranty). Back up first. Try `fastboot boot recovery.img` before flashing anything permanently. Use at your own risk, no warranty.

## Origin and credits
This repository is an **import with full history** of
[`rabilgic/twrp_device_oneplus_hotdogb`](https://github.com/rabilgic/twrp_device_oneplus_hotdogb) (TWRP device tree, branches Android-11 / 12.1 / 13 and fox-*), which in turn credits **lossyx** and **nebrassy** for the original trees. The upstream commits and authorship are preserved unchanged. Our additions are separate commits on top. The upstream README is kept as [`README.upstream.md`](README.upstream.md).

Related work this tree is meant to be compared with: [`TeamWin/android_device_oneplus_sm8150-common`](https://github.com/TeamWin/android_device_oneplus_sm8150-common), [`mauronofrio/android_device_oneplus_hotdog_unified_TWRP`](https://github.com/mauronofrio/android_device_oneplus_hotdog_unified_TWRP).

## Licensing
- The upstream repository has **no top-level LICENSE file**. Some files carry Apache-2.0 / AOSP headers; the rest have no stated licence. We have not relicensed anything and make no claim over upstream files. Upstream authors' rights stay with them. If you are an upstream author and want something changed, open an issue.
- `prebuilt/Image` is a precompiled **stock kernel** (Linux, GPL-2.0). The corresponding source is OnePlus's, published at https://github.com/OnePlusOSS. We do not modify it.
- New files added by Victorious93 are Apache-2.0 (see `LICENSE`).

## Open questions (not verified)
- The upstream README says the 7T has a dedicated recovery partition. Our research notes say it is A/B with recovery in the boot ramdisk. **This is unresolved and must be checked on the real phone** (`ls /dev/block/by-name`) before anything is flashed.
- Which ROM and kernel the phone runs (including the Kali NetHunter setup) is to be read over `adb`. The phone isn't connected yet.
- Decryption on Android 12+ based ROMs is not expected to work without extra work.

## Building
See the main project: https://github.com/Victorious93/VictorRecovery (experimental, untested workflow, manual trigger only).
