This is an Android "prebuilts" repository incorporating the
[RattlesnakeOS community-maintained prebuilts][RattlesnakeOS-microg]
of [microG][], as well as the privileged [Aurora
Services][AuroraServices] component to the Aurora Store.

## How to
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
