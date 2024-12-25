# Expo Camera Permission Bug on Android

This repository demonstrates an uncommon bug related to camera permissions in Expo's Camera API on Android. The bug manifests as inconsistent behavior when camera permissions are not granted by the user. The application may continue to attempt to access the camera, leading to errors and unexpected results.  The specific error messages are device-dependent and can vary significantly. 

## Bug Description

The primary issue is the inconsistent handling of camera permission denials across different Android devices and versions. While the app *should* gracefully handle the permission denial, it often doesn't resulting in application crashes or unexpected behavior.

## Reproduction Steps

1. Run the provided `bug.js` example.
2. Deny camera permission when prompted.
3. Observe the inconsistent behavior (e.g., crashes, unexpected errors, or continued attempts to access the camera).

## Solution

The provided `bugSolution.js` demonstrates a more robust approach to handling camera permission requests. This solution includes explicit checks for permission status and provides a more user-friendly experience when permissions are denied. 