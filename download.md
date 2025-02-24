# Download

<style>
table { margin-left:1em; }
tr { /*border-top:thin solid #ddd;*/ border-bottom:thin solid #ddd; }
div > p > strong > code { margin-left:1em; } /* top-level code lines */
code { white-space:nowrap; }
tr { vertical-align:top; }
td { padding-bottom:.5em; padding-right:1em; }
td:first-of-type { 
  /* white-space:nowrap; */
  /* width:1%; */
}
a { white-space:nowrap; }
.warnings {
    display:inline-block;
    font-style:italic;
    font-size:small;
}
.warnings > a:before {
    content: " ⚠ ";
    color:red;
}
</style>

Here are some ways to install hledger - choose one that suits you.
And please do [let us know](index.html#helpfeedback) or 
[update this page](https://github.com/simonmichael/hledger/blob/master/site/download.md)
if you have any trouble.

The current hledger release is **1.14.2**; here are the [release notes](release-notes).

## Binary packages

These prebuilt binaries will install quickly:

|                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <br><big>**Multiplatform**</big>                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | <br><small>*Packaged&nbsp;version(s):*</small>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Nix](https://nixos.org/nix)<br><small>*Linux,&nbsp;Mac*</small>                                        | <span style="font-size:small;">**`nix-env -i -f https://github.com/NixOS/nixpkgs/archive/fe41fd.tar.gz -A hledger hledger-web hledger-ui`**<br>*On Linux, note <span class=warnings>[#1030](https://github.com/simonmichael/hledger/issues/1030), [#1033](https://github.com/simonmichael/hledger/issues/1033)</span>*</span>                                                                                                                                                                                                                                                                                                                                             | ![](https://img.shields.io/badge/Nix_package-1.14.2-brightgreen.svg)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Docker](https://www.docker.com/products/docker-desktop)<br><small>*Linux,&nbsp;Mac,&nbsp;Windows*</small>                       | **`docker pull dastapov/hledger`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [![](https://img.shields.io/badge/Docker_image-1.14.2-brightgreen.svg)](https://hub.docker.com/r/dastapov/hledger)<br><small>[more..](https://hub.docker.com/search?q=hledger&type=image&sort=updated_at&order=desc)</small>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [Homebrew](https://brew.sh)<br><small>*Linux,&nbsp;Mac,&nbsp;Windows*</small>                     | **`brew install hledger`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [![](https://repology.org/badge/version-for-repo/homebrew/hledger.svg)](https://formulae.brew.sh/formula/hledger)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [Wine](https://www.winehq.org)<br><small>*Linux,&nbsp;Mac,&nbsp;FreeBSD*</small>                         | <span style="font-size:small;">*Install Wine & use the Windows binary below*</span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <br><big>**Windows**</big>                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows&nbsp;binaries                                                            | <code>**[hledger.zip](https://ci.appveyor.com/api/buildjobs/gudfa3gv7pj94ab0/artifacts/hledger.zip)**</code> <span style="font-size:small;">*from Appveyor CI*</span> <br>or <code>[latest dev build](https://ci.appveyor.com/api/projects/simonmichael/hledger/artifacts/hledger.zip?branch=master)</code> <span style="font-size:small;">*may fix Windows 7 <span class=warnings>[#1039](https://github.com/simonmichael/hledger/issues/1039)</span>*</span> <!-- <span class=warnings> [no hledger-ui](https://github.com/jtdaugherty/vty/pull/1#issuecomment-297143444),[doesn't work on old windows ?](https://github.com/simonmichael/hledger/issues/774),[many files in PATH causing hangs](https://github.com/simonmichael/hledger/issues/791) --><!-- ,[appveyor builds failing](https://github.com/simonmichael/hledger/issues/832) </span>--> | [![](https://img.shields.io/badge/Windows_binaries-1.14.1+_20190309-brightgreen.svg)](https://ci.appveyor.com/project/simonmichael/hledger/builds/22955930/artifacts) <br>[![](https://img.shields.io/badge/Windows_binaries-nightly-brightgreen.svg)](https://ci.appveyor.com/project/simonmichael/hledger/build/artifacts)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <br><big>**GNU/Linux**</big>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Arch                                                                             | **`pacman -S hledger hledger-ui hledger-web`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [![](https://repology.org/badge/version-for-repo/arch/hledger.svg)](https://www.archlinux.org/packages/?sort=&q=hledger)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Gentoo                                                                           | **`sudo layman -a haskell && sudo emerge hledger hledger-ui hledger-web`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [![](https://img.shields.io/badge/Gentoo_package-1.14.2-brightgreen.svg)](https://gentoo.zugaina.org/Search?search=hledger)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Debian                                                                           | **`sudo apt install hledger hledger-ui hledger-web`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | [![Debian Unstable](https://repology.org/badge/version-for-repo/debian_unstable/hledger.svg)](https://packages.debian.org/unstable/hledger)<br>[![Debian Testing](https://repology.org/badge/version-for-repo/debian_testing/hledger.svg)](https://packages.debian.org/testing/hledger)<br>[![Debian Stable](https://repology.org/badge/version-for-repo/debian_stable/hledger.svg)](https://packages.debian.org/stable/hledger)<br>[![Debian Oldstable](https://repology.org/badge/version-for-repo/debian_oldstable/hledger.svg)](https://packages.debian.org/oldstable/hledger)<br><small>[more..](https://packages.debian.org/search?searchon=names&keywords=hledger)</small>                                                                                                                       |
| Ubuntu                                                                           | **`sudo apt install hledger hledger-ui hledger-web`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | [![Ubuntu 19.04](https://repology.org/badge/version-for-repo/ubuntu_19_04/hledger.svg)](https://packages.ubuntu.com/disco/hledger)<br>[![Ubuntu 18.10](https://repology.org/badge/version-for-repo/ubuntu_18_10/hledger.svg)](https://packages.ubuntu.com/cosmic/hledger)<br>[![Ubuntu 18.04](https://repology.org/badge/version-for-repo/ubuntu_18_04/hledger.svg)](https://packages.ubuntu.com/bionic/hledger)<br>[![Ubuntu 16.04](https://repology.org/badge/version-for-repo/ubuntu_16_04/hledger.svg)](https://packages.ubuntu.com/xenial/hledger)<br>[![Ubuntu 14.04](https://repology.org/badge/version-for-repo/ubuntu_14_04/hledger.svg)](https://packages.ubuntu.com/trusty/hledger)<br><small>[more..](https://packages.ubuntu.com/search?suite=all&searchon=names&keywords=hledger)</small> |
| Fedora                                                                           | **`sudo dnf install hledger`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [![Fedora Rawhide](https://img.shields.io/badge/Fedora_Rawhide_package-1.10-red.svg)](https://apps.fedoraproject.org/packages/hledger/)<br>[![Fedora 30](https://img.shields.io/badge/Fedora_30_package-1.5-red.svg)](https://apps.fedoraproject.org/packages/hledger/)<br>[![Fedora 29](https://repology.org/badge/version-for-repo/fedora_29/hledger.svg)](https://apps.fedoraproject.org/packages/hledger/)<br>[![Fedora 28](https://repology.org/badge/version-for-repo/fedora_28/hledger.svg)](https://apps.fedoraproject.org/packages/hledger/)<br>[![Fedora 27](https://repology.org/badge/version-for-repo/fedora_27/hledger.svg)](https://apps.fedoraproject.org/packages/hledger/)<br><small>[more..](https://apps.fedoraproject.org/packages/s/hledger)</small>                              |
| Void                                                                             | **`xbps-install -S hledger hledger-ui hledger-web`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | [![Void Linux x86_64](https://repology.org/badge/version-for-repo/void_x86_64/hledger.svg)](https://voidlinux.org/packages/?q=hledger)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <br><big>**BSD**</big>                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [OpenBSD&nbsp;WIP](https://github.com/jasperla/openbsd-wip#how-to-use-this-tree) | **`make -C /usr/ports/openbsd-wip/productivity/hledger install`**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [![openbsd-wip port](https://img.shields.io/badge/openbsd--wip_port-1.10-red.svg)](https://github.com/jasperla/openbsd-wip/tree/master/productivity/hledger)<br><small>[more..](https://github.com/jasperla/openbsd-wip/tree/master/productivity)</small>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <br><big>**Other**</big>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Sandstorm](https://sandstorm.io)<br><small>*Community/private cloud platform*</small>                 | **[HLedger Web app](https://apps.sandstorm.io/app/8x12h6p0x0nrzk73hfq6zh2jxtgyzzcty7qsatkg7jfg2mzw5n90)** <!-- <br><span class=warnings>[features needed](https://github.com/simonmichael/hledger/issues/425)</span> -->                                                                                                                                                                                                                                                                                                                                                                                               | ![](https://img.shields.io/badge/Sandstorm_app-1.9.1-red.svg)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

<!-- <br><br><small>*Or: (nix-channel --update may be needed. CI [build][nix unstable linux builds] [issues][nix unstable mac builds] may cause failure/large downloads; check those links/try with --dry-run first)*</small> <br><span style="font-size:small;">**`nix-env -i hledger-1.14.2 hledger-ui-1.14.2 hledger-web-1.14.1`**</span> -->

<a name="b"></a>

## Building from source

You can build hledger wherever the Glasgow Haskell Compiler is supported.
This can take a while, but it's normally a reliable process.
Use one of the methods below to build the current hledger release.
The hledger-install script requires only bash and installs the required tools.
Or, you can install stack or cabal yourself and deal with them directly.

|                                                                    |                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                                    |                                                                                                                                                                                                                                                                                                                                                                         |
| [hledger-install.sh](https://github.com/simonmichael/hledger/blob/master/hledger-install/hledger-install.sh)<br><small>*Linux,&nbsp;Mac,&nbsp;WSL*</small> | <span style="font-size:medium;">**`curl -s https://raw.githubusercontent.com/simonmichael/hledger/master/hledger-install/hledger-install.sh -O`**<br>**`less hledger-install.sh`**&nbsp;&nbsp;&nbsp;&nbsp;*# satisfy yourself that the script is safe*<br>**`bash hledger-install.sh`**&nbsp;&nbsp;&nbsp;&nbsp;*# runs stack or cabal, installing stack if needed*</span> |
| [stack](https://haskell.fpcomplete.com/get-started)<br><small>*Linux,&nbsp;Mac,&nbsp;Windows*</small>          | <span style="font-size:medium;">**`stack install --resolver=lts-14.1 hledger hledger-web hledger-ui --verbosity=error`**</span>&nbsp;&nbsp;&nbsp;&nbsp;*# installs GHC if needed.*                                                                                                                                                                                              |
| [cabal](https://www.haskell.org/cabal)<br><small>*Linux,&nbsp;Mac,&nbsp;Windows*</small>          | <span style="font-size:medium;">**`cabal v2-update && cabal v2-install hledger-1.14.2 hledger-web-1.14.1 hledger-ui-1.14.2`**</span>                                                                                                                                                                                                                                    |

On Windows, hledger-ui is not available and should be omitted from the commands above (except, it probably works in WSL).

#### Resource usage

Building Haskell programs typically involves downloading and compiling and
optimising a lot of Haskell libraries. 
If you are doing it for the first time, know that building hledger could take 
1-2G of disk, 1-2G of free memory, and up to an hour (though usually it's much less).
It's fine to kill a build and restart it later;
and your later builds will be much faster.

If needed, you can save time/memory/disk space by omitting the
[hledger-web](http://hackage.haskell.org/package/hledger-web) and
[hledger-ui](http://hackage.haskell.org/package/hledger-ui) packages
from the stack or cabal commands above.
To estimate the build time remaining, add `--dry-run`.

#### Using stack

The latest version of stack (2.1.3 as of 2019-07) will likely work best, so we recommend it.
If you have an older version, you can usually upgrade quickly with `stack upgrade`.
Versions older than 1.7.1 will definitely not work.
On Windows, the 64-bit version of stack is recommended.

<!--
Some other [add-on tools](/hledger.html#third-party-add-ons) like
[hledger-api](http://hackage.haskell.org/package/hledger-api),
[hledger-iadd](http://hackage.haskell.org/package/hledger-iadd),
and [hledger-interest](http://hackage.haskell.org/package/hledger-interest)
can be installed like so:

  **`stack install --resolver=lts-14.1 hledger-api hledger-interest hledger-iadd hledger-interest-1.5.3 hledger-iadd-1.3.9`**
-->

<!-- <a name="b3"></a> -->

<!-- #### cabal -->

#### C libraries may be required

A few C libraries, like terminfo, are required but not installed by the commands above.
When such C libs are missing, the build will fail at the end with a link error 
such as "/bin/ld.gold: error: cannot find -ltinfo".
To solve this, just install the appropriate system package(s) and run the build command again. 

These package names vary by platform. If you don't see your platform below,
do a web search for the link error message (and send updates for this list):

|                 |                                                   |
|-----------------|---------------------------------------------------|
| Debian, Ubuntu: | **`sudo apt install -y libtinfo-dev`**            |
| Fedora, RHEL:   | **`sudo dnf install -y gmp-devel ncurses-devel`** |

<a name="build-issues"></a><a name="windows-build-issues"></a>

#### Platform-specific build issues

Here are some known build issues and workarounds on certain platforms:

<!--
<div class="warnings" style="font-size:medium;">

[nix: nix install on linux can fail with "cloning builder process: Operation not permitted"](https://github.com/simonmichael/hledger/issues/1030)\
[nix: on Linux, nix-installed hledger won't handle non-ascii data](https://github.com/simonmichael/hledger/issues/1033)\
[windows: hledger-web fails to start on Windows 7](https://github.com/simonmichael/hledger/issues/1039)\
[windows: hledger-ui is not available](https://github.com/jtdaugherty/vty/pull/1#issuecomment-297143444)\
[windows: build hangs using GHC 8.6.3](https://github.com/well-typed/generics-sop/issues/93)\
[windows: cross-environment non-ascii display issues](https://github.com/simonmichael/hledger/issues/961#issuecomment-471229644)\
[arch: haskell build advice from Arch wiki](https://wiki.archlinux.org/index.php/Haskell)\
[arch: No information found for ghc-8.4.2](https://github.com/commercialhaskell/stack/issues/3984)\
[freebsd 12: no cabal file found](https://github.com/simonmichael/hledger/issues/709)\
[openbsd 6: exec permission denied](https://deftly.net/posts/2017-10-12-using-cabal-on-openbsd.html)\
[openbsd: how to get stack](https://github.com/commercialhaskell/stack/issues/2822#issuecomment-318892816)\

</div>
-->
<!-- [arch: some past problems](https://github.com/simonmichael/hledger/issues/668) -->

<p><span class="warnings" style="font-size:medium;"> <a href="https://github.com/simonmichael/hledger/issues/1030">nix: nix install on linux can fail with “cloning builder process: Operation not permitted”</a><br />
<a href="https://github.com/simonmichael/hledger/issues/1033">nix: on Linux, nix-installed hledger won’t handle non-ascii data</a><br />
<a href="https://github.com/simonmichael/hledger/issues/1039">windows: hledger-web fails to start on Windows 7</a><br />
<a href="https://github.com/jtdaugherty/vty/pull/1#issuecomment-297143444">windows: hledger-ui is not available</a><br />
<a href="https://github.com/well-typed/generics-sop/issues/93">windows: build hangs using GHC 8.6.3</a><br />
<a href="https://github.com/simonmichael/hledger/issues/961#issuecomment-471229644">windows: cross-environment non-ascii display issues</a><br />
<a href="https://wiki.archlinux.org/index.php/Haskell">arch: haskell build advice from Arch wiki</a><br />
<a href="https://github.com/commercialhaskell/stack/issues/3984">arch: No information found for ghc-8.4.2</a><br />
<!-- [arch: some past problems](https://github.com/simonmichael/hledger/issues/668) --> <a href="https://github.com/simonmichael/hledger/issues/709">freebsd 12: no cabal file found</a><br />
<a href="https://deftly.net/posts/2017-10-12-using-cabal-on-openbsd.html">openbsd 6: exec permission denied</a><br />
<a href="https://github.com/commercialhaskell/stack/issues/2822#issuecomment-318892816">openbsd: how to get stack</a><br />
</span></p>

#### Setting $PATH may be required

After building you may see a message about where the executables were installed.
After installation, make sure this install directory is configured in your shell's \$PATH
(preferably near the start of it, in case you have older hledger binaries lying around).
The install directory is:

|                    | on non-Windows systems | on Windows 
|--------------------|------------------------|------------------------------------------
| If stack was used  | `$HOME/.local/bin`     | `%APPDATA%\local\bin` (eg&nbsp;`C:\Users\Joe\AppData\Roaming\local\bin`)
| If cabal was used  | `$HOME/.cabal/bin`     | `%APPDATA%\cabal\bin`

How to configure \$PATH is platform- and shell-specific.
If you are using bash, this should take care of it:

  **`echo "export PATH=~/.local/bin:~/.cabal/bin:$PATH" >> ~/.bashrc && source ~/.bashrc`**

#### Test the installation

After a successful build and install, you should be able to run the
hledger tools (whichever ones you installed) and see the expected versions:

  `$`**`hledger --version`**\
  `hledger 1.14.2`\
  `$`**`hledger-ui --version`**\
  `hledger-ui 1.14.2`\
  `$`**`hledger web --version`**\
  `hledger-web 1.14.1`\
  `$`**`hledger iadd --version`**\
  `This is hledger-iadd version 1.3.9`

And you can check that the unit tests pass (just for fun):

  `$`**`hledger test`**\
  `...`\
  `✅  198 tests passed, no failures! 👍 🎉`

<a name="c"></a>

### Building the development version

The master branch in hledger's git repo is stable enough for daily use,
and includes the [latest improvements](https://github.com/simonmichael/hledger/commits/master).
You'll need [git](https://en.wikipedia.org/wiki/Git) and 
[`stack`](http://haskell-lang.org/get-started) or [cabal](https://www.haskell.org/cabal/).
This will build and install all of the main hledger tools using stack:

  **`git clone https://github.com/simonmichael/hledger`**\
  **`cd hledger`**\
  **`stack install`**

cabal users may find the `cabal-install.sh` or `cabal.project` files useful.

The --version output of development builds has a .99 suffix meaning "dev".
So 1.14.99 means "1.15-dev", the in-development version of 1.15.

### Building the development version with docker

You can also build development version in the docker container, which will take care of pulling
all the necessary tools and dependencies:

  **`git clone https://github.com/simonmichael/hledger`**\
  **`cd hledger/docker`**\
  **`./build.sh`**

This will build image tagged `hledger` with just the latest binaries inside.

If you want to keep all the build artifacts and use the resulting image for hledger development, use
`build-dev.sh` instead.
