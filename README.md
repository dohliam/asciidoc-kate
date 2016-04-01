# asciidoc-kate - An AsciiDoc/AsciiDoctor plugin for Kate editor/KatePart

The XML file in this repository (`asciidoc.xml`) contains rules for highlighting the syntax of [AsciiDoc](http://asciidoc.org/) and [AsciiDoctor](http://asciidoctor.org/) markup files in [Kate](http://kate-editor.org/), the default text editor for [KDE](https://www.kde.org/).

Once [installed](#installation), opening any file with the `.adoc` extension should automatically highlight AsciiDoc syntax as in the example below:

![AsciiDoc syntax highlighting screenshot](https://cloud.githubusercontent.com/assets/9295750/14151632/afee9468-f663-11e5-859e-800e16cf027f.png)

This highlighter works fine with Kate or [Kwrite](https://www.kde.org/applications/utilities/kwrite/) (which are both based on [KatePart](http://kate-editor.org/about-katepart/)), and should also work with most of the common features of both AsciiDoc and AsciiDoctor.

## Installation

Steps to install the AsciiDoc syntax highlighting file:

1. Download the file `asciidoc.xml` or clone this repository
2. Find the folder `~/.kde/share/apps/katepart/syntax/` on your system (create it if it does not already exist)
3. Move `asciidoc.xml` into `~/.kde/share/apps/katepart/syntax/`
4. Open or restart Kate to use the syntax highlighter.

Default syntax highlighting files for Kate are usually stored in the folder `/usr/share/kde4/apps/katepart/syntax/`. However, custom syntax highlighters should probably be saved in the local syntax highlighting folder (`~/.kde/share/apps/katepart/syntax/`) in the user's home directory so that they don't get accidentally overwritten during an update.

NOTE: The above applies to KDE 4. If you are using Plasma 5, the local folder for Kate syntax files has changed to `~/.local/share/katepart5/syntax/`.

## Usage

Files with the extension `.ad`, `.adoc` or `.asciidoc` will automatically be highlighted using the rules in `asciidoc.xml`. Plain text or other files can be forced to use AsciiDoc highlighting rules by selecting _AsciiDoc_ from the _Highlighting_ menu:

* __Tools__ > __Highlighting__ > __Markup__ > __AsciiDoc__

## Issues

Although most basic formatting is working and should be fine for normal use, there are still many advanced features from the AsciiDoc / AsciiDoctor spec that are not supported yet. Some (like includes and complex attributes) can't feasibly be supported in Kate due to limitations of the editor itself (an editor like [Atom](https://atom.io/) with an actual [HTML preview feature for AsciiDoc files](https://github.com/asciidoctor/atom-asciidoc-preview) would probably be better if you need these features).

However, it would be great to support as many features as possible within Kate/Kwrite. If you have a fix for something (or an idea for a new feature), feel free to submit a PR!

## License
Based on [kate-markdown](http://github.com/claes/kate-markdown/) by [Claes Holmerson](http://github.com/claes/).

Dual-Licensed under both GPL and BSD licenses.
