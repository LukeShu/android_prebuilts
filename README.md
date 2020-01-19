# An Android "prebuilts" repository for [AuroraServices][]

## How-to for [RattlesnakeOS][]

Add the following to end of your rattlesnakeos-stack config file.

```toml
[[custom-prebuilts]]
modules = ["AuroraServices"]
repo = "https://gitlab.com/lukeshu/aurora_prebuilts"
```

[AuroraServices]: https://gitlab.com/AuroraOSS/AuroraServices/
[RattlesnakeOS]: https://github.com/dan-v/rattlesnakeos-stack/
