This is an Android "prebuilts" repository incorporating the
[RattlesnakeOS community-maintained prebuilts][RattlesnakeOS-microg]
of [microG][], as well as the privileged [Aurora
Services][AuroraServices] component to the Aurora Store.

## How to use

Add the following to end of your `rattlesnakeos-stack` config file.

```toml
[[custom-patches]]
  patches = ["00002-microg-sigspoof.patch"]
  repo = "https://github.com/LukeShu/android_prebuilts"

[[custom-prebuilts]]
  modules = ["GmsCore","GsfProxy","FakeStore","com.google.android.maps.jar","AuroraServices"]
  repo = "https://github.com/LukeShu/android_prebuilts"
```

[AuroraServices]: https://gitlab.com/AuroraOSS/AuroraServices/
[RattlesnakeOS]: https://github.com/dan-v/rattlesnakeos-stack/
[RattlesnakeOS-microg]: https://github.com/RattlesnakeOS/microg
[microG]: https://microg.org/

# How to modify

 - Updating microg: Merge from https://github.com/RattlesnakeOS/microg
   (which is downstream from
   https://notabug.org/bubblethink/android_prebuilts_prebuiltapks ,
   which is downstream from
   https://github.com/lineageos4microg/android_prebuilts_prebuiltapks
   I guess look at commit dates if you're concerned someone's dropping
   the ball--I'm not sure what any of their processes are.)
 - Updating Aurora Services: Run `./update`
