# Expo CLI: Device/Configuration Incompatibility Errors

This repository demonstrates a common issue encountered when building and running Expo projects: errors stemming from incompatibilities between the project's configuration and the target device or simulator.  This can manifest as build failures or runtime crashes.

## Problem

The core problem is a mismatch between the capabilities of your target device (OS version, architecture) and the constraints specified in your `app.json` or EAS build configuration.  This might involve minimum supported OS versions, supported architectures, or other configuration discrepancies.

## Solution

The solution involves careful review of your project's configuration to ensure it aligns with your target devices. This includes checking:

* **`app.json` (or `expo.json`):**  Verify the `expo.ios.supportsTablet`, `expo.android.adaptiveIcon`, `minSdkVersion`, and other relevant settings.
* **EAS Build Configuration:**  If using EAS Build, scrutinize your configuration file for any architecture restrictions or other parameters that could be limiting compatibility.
* **Device/Simulator Specifications:**  Ensure that your target device or simulator matches the capabilities outlined in your configuration.

Often a rebuild after correcting configuration is necessary.