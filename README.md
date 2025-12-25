# ReVanced Extended
[![CI](https://github.com/Susheate/revanced-extended-magisk/actions/workflows/ci.yml/badge.svg?event=schedule)](https://github.com/Susheate/revanced-extended-magisk/actions/workflows/ci.yml)

Get the [latest CI release](https://github.com/susheatee/revanced-extended-magisk/releases/latest).

### A fork of [NoName-exe's Revanced Extended repo](https://github.com/NoName-exe/revanced-extended) made to fix mount not being kept across reboots.

## Features
 * Keep mount across reboots.
 * Build Magisk modules for Youtube Revanced Extended and Youtube Music Revanced Extanded.
 * Updated with the latest versions of patches.
 * Cleans APKs from unneeded libs to make them smaller.
 * Fully open-source, every binary or APK is compiled without human intervention.
 * Modules:
     * Recompile invalidated odex for YouTube and YouTube-Music for faster usage.
     * Receive updates from Magisk app.
     * Should not break safetynet or trigger root detections used by certain apps.
     * Handle installation of the correct version of the stock app and all that.
     * Support Magisk and KernelSU.

 ## Notes
* Use [zygisk-detach](https://github.com/j-hc/zygisk-detach) to block Play Store from updating YouTube and YouTube-Music.

## Credits
[j-hc](https://github.com/j-hc) for [zygisk-detach](https://github.com/j-hc/zygisk-detach) and the [revanced-magisk-module repo](https://github.com/j-hc/revanced-magisk-module).

[ReVanced Team](https://github.com/revanced)

[inotia00](https://github.com/inotia00) for [revanced-extended patches](https://github.com/inotia00/revanced-patches).

[NoName-exe](https://github.com/NoName-exe) for making the [revanced-extended repo](https://github.com/NoName-exe/revanced-extended).
