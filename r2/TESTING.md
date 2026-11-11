# STORM 2 R1 testing

## Completed host/build checks

- 85 native logging assertions under AddressSanitizer and UndefinedBehaviorSanitizer.
- 28 isolated save backup/export/restore assertions, using `STORM2.S` paths and protecting 100% save markers.
- 30 driver/package compatibility assertions, 14 session/status file assertions, 10 FPS text assertions, 6 renderer-report assertions and 24 configuration/display assertions.
- Six member-linkage checker regression tests, runtime Java/D8 compilation and checked cross-package references/interface callbacks in the real customized APK.
- Native engine executable/linkage sections, other upstream libraries, assets, license bodies and bundled `save100/STORM2.S` verified against the pinned upstream APK.
- APK signature, ARM64 helper exports, archive integrity and 16 KiB ZIP alignment checked during assembly.

## Android checks

The Android validation workflow builds with an ephemeral test key and exercises the real APK at font scales 1.0 and 1.3. Coverage includes the launcher, stock mappings, save ZIP reimport through the original importer, game menu, touch rendering, statistics sizing/collapse, shutdown locking, driver picker/configuration, JNI helper binding and logging On/Off.

A separate step opens the actual game activity and checks that SDL reaches the expected missing-game-file boundary without a Java access/verifier crash. No game data is downloaded for CI. Results are recorded after the workflow completes; these checks do not constitute gameplay testing.

## Device checks still needed

Real game startup, gameplay performance, native save completion, physical controller behavior, frame-generation presentation and PanVK/RADV gameplay compatibility need a supported phone and the user's own game data. No FPS increase or universal driver compatibility is claimed.
