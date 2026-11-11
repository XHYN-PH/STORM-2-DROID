# STORM 2 — R1

Modified and Translated by **XHYN_PH**. Based on the original Android **v0.5.43** release.

- **English throughout the interface:** launcher, settings, mapping labels, game options, help and error messages. The game is configured for English.
- **New app identity:** STORM 2, with the round orange and cream Leaf logo.
- **Cleaner menus:** rounded dark dialogs and gold accents, with settings integrated into the stock launcher. Decorative option-click particles are removed; simple press and bounce feedback remain.
- **More useful game options:** Fit, Stretch and proportional Crop, touch visibility and opacity, brightness, statistics size and confirmed return to the launcher.
- **Smaller FPS/statistics panel:** 70% by default, adjustable from 50–125%, draggable and collapsible. Game and generated output FPS are labelled separately.
- **Save export and backups:** export the current STORM 2 save, create/export backups and restore a backup. Restoration keeps a backup of the current save and is blocked while the game runs or the 100% save is active. The original importer and bundled 100% save remain intact.
- **Logging control:** default-off app logging with the original Send log link retained. When logging is enabled, shared logs include settings and current-session details.
- **Additional graphics options:** brightness/gamma, shadow cap, GPU-memory budget and streaming-cache overrides run after the stock configuration writer. Original graphics controls and controller mappings are retained.
- **Less interface overhead:** cached touch artwork, bounded overlay drawing, background statistics reads, and polling/animations paused when no longer needed. Foreground refresh requests also follow display and surface changes.
- **Clearer startup and shutdown feedback:** loading feedback follows shader preparation; returning to the launcher waits for normal game shutdown before save management becomes available. Exiting does not create a manual save.
- **Experimental driver imports:** retain Turnip on Adreno and add compatible PanVK for Mali and RADV for Samsung Xclipse through the original driver picker. GPU/Android/package checks help reject incompatible imports. Additional drivers are not bundled; gameplay on Mali/Xclipse still needs real-device testing.
- **XHYN_PH links:** YouTube footer, fork update checks, public customization/build code, and Telegram in the README.

The port's original engine is closed source. These changes do not unlock 60 FPS gameplay, expand the game camera or guarantee fixes for native rendering/stall problems. No game files are included.

[Download](https://github.com/XHYN-PH/STORM-2-DROID/releases/latest) · [Telegram](https://t.me/xhynports) · [YouTube](https://youtube.com/@xhyn_ph)
