# Documentation

## Config

Adding another revanced app is as easy as this:

``` toml
[Some-App]
apkmirror-dlurl = "https://www.apkmirror.com/apk/inc/app"
# or uptodown-dlurl = "https://app.en.uptodown.com/android"
```

> [!WARNING]
> When a patch name itself contains a single quote, double it inside the string (e.g. 'Hide ''Get Music Premium''').

### More about other options:

There exists an example below with all defaults shown and all the keys explicitly set.  
**All keys are optional** (except download urls) and are assigned to their default values if not set explicitly.  

``` toml
parallel-jobs = 1                    # Amount of cores to use for parallel patching, if not set $(nproc) is used
compression-level = 9                # Module zip compression level
remove-rv-integrations-checks = true # Remove checks from the revanced integrations
dpi = "nodpi anydpi 120-640dpi"      # dpi packages to be searched in order. default: "nodpi anydpi"

patches-source = "revanced/revanced-patches" # Where to fetch patches bundle from. default: "revanced/revanced-patches"
cli-source = "ReVanced/revanced-cli"             # Where to fetch cli from. default: "ReVanced/revanced-cli"
# Options like cli-source can also set per app
rv-brand = "ReVanced Extended" # Rebrand from 'ReVanced' to something different. default: "ReVanced"

patches-version = "v2.160.0" # 'latest', 'dev', or a version number. default: "latest"
cli-version = "v5.0.0"       # 'latest', 'dev', or a version number. default: "latest"

[Some-App] # The table name, the builder will fallback to it if variables such as app-name or release-name weren't bound.
app-name = "YouTube" # The modules' names display the app-name and rv-brand values, the module's name would be YouTube ReVanced Extended. If this variable isn't bound, the builder will fallback to the table name (Some-App).
release-name = "SomeApp" # If set, release name becomes SomeApp instead of Some-App. default is same as table name, which is 'Some-App' here.
enabled = true       # Whether to build the app. default: true
build-mode = "apk"   # 'both', 'apk' or 'module'. default: apk

# 'auto' option gets the latest possible version supported by all the included patches
# 'latest' gets the latest stable without checking patches support. 'beta' gets the latest beta/alpha
# Whitespace seperated list of patches to exclude. default: ""
version = "auto"     # 'auto', 'latest', 'beta' or a version number (e.g. '17.40.41'). default: auto

# Optional args to be passed to cli. can be used to set patch options
# Multiline strings in the config is supported
patcher-args = """\
  -OdarkThemeBackgroundColor=#FF0F0F0F \
  -Oanother-option=value \
  """

excluded-patches = """\
  'Some Patch' \
  'Some Other Patch' \
  """

included-patches = "'Some Patch'"                          # Whitespace seperated list of non-default patches to include. default: ""
include-stock = true                                       # Includes stock apk in the module. default: true
exclusive-patches = false                                  # Exclude all patches by default. default: false
apkmirror-dlurl = "https://www.apkmirror.com/apk/inc/app"
uptodown-dlurl = "https://spotify.en.uptodown.com/android"
module-prop-name = "some-app-module"                       # Module prop name.
dpi = "360-480dpi"                                         # Used to select apk variant from apkmirror. default: nodpi
arch = "arm64-v8a"                                         # 'arm64-v8a', 'arm-v7a', 'all', 'both'. 'both' downloads both arm64-v8a and arm-v7a. default: all
```

---

## Building Locally

### On Linux

``` bash
$ git clone https://github.com/Susheate/rvx-morphe-module-builder
$ cd rvx-morphe-module-builder
$ ./build.sh
```

### On Termux

``` bash
bash <(curl -sSf https://raw.githubusercontent.com/Susheate/rvx-morphe-module-builder/main/build-termux.sh)
```
