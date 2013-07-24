# Tunghsiao Liu’s Automator Workflows
A collection of Automator workflows that speed up your design / development process. Compatible with LaunchBar.


## Installation

Copy the workflows to `~/Library/Services/`.

## Workflow List

### Add @2x Suffix
Add @2x suffix for retina image assets.

### Convert Image Format
Convert selected images to specific format.

### Copy & Add @2x Suffix
Copy (duplicate) selected images and rename them with @2x suffix. Useful when you want to downscale with your own method.

### Create @2x Image
Auto downscale retina images generated by [PNG Express](http://www.pngexpress.com/), or any @2x images.

**Note**: Export your original images in retina size, WITHOUT `@2x` suffix.

### Create App Iconset
Create the following sizes of icon resources for your OS X app:

Filename | Size of canvas (in pixels)
--- | ---
icon_512x512@2x | 1024×1024
icon_512x512    | 512×512
icon_256x256@2x | 512×512
icon_256x256    | 256×256
icon_128x128@2x | 256×256
icon_128x128    | 128×128
icon_32x32@2x   | 64×64
icon_32x32      | 32×32
icon_16x16@2x   | 32×32
icon_16x16      | 16×16

The icon you created should be 1024×1024 with an sRGB color profile. You can read more about icon design guidelines [here](http://developer.apple.com/library/mac/documentation/userexperience/conceptual/applehiguidelines/IconsImages/IconsImages.html).

**Note**: You should always select the original file during the workflow, don’t press any key or click your mouse.

### Create .icns
Create .icns file using `iconutil`. Command Line Tools from Xcode must be installed before using this workflow.

### Unpack .icns
Unpack .icns into .iconset folder. Command Line Tools from Xcode must be installed before using this workflow.

### Create DMG Image
Create distributable, cross-platform hybrid DMG images using `hdiutil`, select a directory first to use this script. You’ll be prompted to enter a volume name for your image, then Voilà!

**Note**: This script doens’t create “fancy” DMG for your OS X app.

### Compress SVG with SVGO
Compress all SVG files in a folder (folder workflow) with [svgo](https://github.com/svg/svgo), `svgo` must be installed before using this workflow. Please note that since `svgo` is a third-party script, it’s [by design](http://developer.apple.com/library/mac/#technotes/tn2065/_index.html) that this script does NOT inherit the `$PATH` variable from your environment, you have to use full path for your `svgo` location, in this workflow, the path of `svgo` is `/usr/local/share/npm/bin/svgo`. (node and npm installed by [Homebrew](http://mxcl.github.io/homebrew/)).

### Compress PNG with OptiPNG
Compress selected PNG files with [OptiPNG](http://optipng.sourceforge.net/), `optipng` must be installed before using this workflow. Please note that since `optipng` is a third-party script, it’s [by design](http://developer.apple.com/library/mac/#technotes/tn2065/_index.html) that this script does NOT inherit the `$PATH` variable from your environment, you have to use full path for your `optipng` location, in this workflow, the path of `optipng` is `/usr/local/bin/optipng`. (Installed by [Homebrew](http://mxcl.github.io/homebrew/)).

**Note**: The default compress option is set to `-o7` (smallest file size and slowest), You may need change that.

### Open with rmate
Open selected file with [rmate](https://github.com/textmate/rmate), `rmate` must be installed before using this workflow. Please note that since `rmate` is a third-party script, it’s [by design](http://developer.apple.com/library/mac/#technotes/tn2065/_index.html) that this script does NOT inherit the `$PATH` variable from your environment, you have to use full path for your `rmate` location, in this workflow, the path of `rmate` is `/usr/local/opt/ruby/bin/rmate` installed by [Homebrew](http://mxcl.github.io/homebrew/).

### Remove @2x Suffix
Remove @2x suffix for retina image assets. Useful when you’re doing something wrong and need to recreate downscaled images one more time.

### Rename Selected Files

![Rename Finder Items](https://raw.github.com/sparanoid/rsrc/automator-workflows/01-rename-finder-items.png)

What? You just bought [A Better Finder Rename](http://www.publicspace.net/ABetterFinderRename/)?

### Resize Images
Resize your images to specific size or by percentage.

### Restart Finder
Restart your Finder, you can execute it in [LaunchBar](www.obdev.at/launchbar/). I packed it as an application since bash script has been limited in Mt. Lion. I also include an unpacked Automator service for this app.

### Show Files
Toggle Hidden files in a simple click, it’s an app just like `Restart Finder.app`.

## Author

**Tunghsiao Liu**

+ http://twitter.com/tunghsiao
+ http://github.com/sparanoid
