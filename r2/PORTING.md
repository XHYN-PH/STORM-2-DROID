# STORM 2 integration notes

The customization source comes from STORM 3 R1–R2.4; the engine and game data do not.

| Hook | STORM 3 reference | STORM 2 v0.5.43 |
| --- | --- | --- |
| App package | `com.naruto.storm3` | `com.naruto.storm2` |
| Launcher settings list | field `o` | field `r` |
| Launcher preferences | field `a` | field `e` |
| Configuration writer | `t()` | `s()` |
| Card / switch-row builders | `q()` / `p()` | `p()` / `o()` |
| Switch callback | `a.b.a(boolean)` | `a.b.b(boolean)` |
| Touch view / button / stick | `a.f0` / `a.c0` / `a.e0` | `a.h0` / `a.e0` / `a.g0` |
| Statistics view | `a.a0` | `a.b0` |
| Floating menu / touch listener | `a.Z` / `a.Y` | `a.a0` / `a.Z` |
| Polling dispatcher | `a.L` | `a.M` |
| Save container | `storm3fb.s` | `storm2.s` |
| Save file / title ID | `STORM3FB.S` / `4E4D085C` | `STORM2.S` / `4E4D0819` |
| Original Send log | launcher method | default branch of `a.p.onClick` |

The first Android run caught an `AbstractMethodError` from the changed switch callback. Both the logging listener and Java compile stub now use the actual STORM 2 callback. The member checker verifies concrete implementations against real APK interface definitions and rejects the earlier candidate before assembly.

Native statistics still return seven floats and shader preparation returns two integers. Native helper JNI names remain in `com.naruto.port`. Executable sections of the five original helper libraries match the STORM 3 reference; the STORM 2 engine itself remains the pinned upstream engine. Native translations cover only the three display strings present in that engine, with executable/linkage sections verified unchanged.

Both original touch artwork methods match the STORM 3 reference after type renaming. Build-time checks compare all original touch/editor methods and the controller mapping class before and after customization. No input-axis or right-stick helper is added.
