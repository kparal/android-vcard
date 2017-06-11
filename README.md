android-vcard
=============

Android-vcard is a Java library for manipulating vCard files. The source code
was extracted from the Google Android 1.0 project.

---------------------------------------------------------------------

[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

### Android-vcard is not maintained aymore!

**This project is unmaintained. There is no user support either, sorry.**

---------------------------------------------------------------------

This is not an application for Android. This is a development library for PC.

This project was created out of desperation that there is no decent Java vCard
library. All libraries which I have found had problems with various file or
character encodings, vCard versions, etc. Therefore I hacked a vCard related
code out of Google Android project and made it into a standalone library.

I made a few changes in the Google's code (notably a few improvements in "UTF-8"
support and redirected error reporting to a standard Java Logging facility). But
I don't plan on any further additions or bugfixes. It does not make much sense
to do custom changes into this project when Google probably fixed all the bugs
already in newer releases of the Android code base. However, I also lack the
time and motivation to extract this library again from the latest Android source
code (the current library code is taken from Android 1.0). If you have the
motivation, please try it. If you contact me afterwards, I'll happily forward
visitors to your project.

The project is licensed under Apache License 2.0.

### Program links
* Project page: https://github.com/kparal/android-vcard
* Some old documentation: https://github.com/kparal/android-vcard/tree/wiki
* Old project page: http://code.google.com/p/android-vcard/
* Google Android source: http://source.android.com/

### Program files
```
ChangeLog       - Description of latest changes.
license.txt     - Library license.
README.md       - This file.
upstream.md5    - List of md5 hashes of upstream files for detecting changes.
examples/       - Usage examples.
lib/            - Program compilation and runtime libraries.
nbproject/      - Project files for the NetBeans IDE.
src/            - Program sources.
test/           - Program test sources.
```

Project root directory can be opened by NetBeans IDE as its project.


Compiling library
-----------------

In sources root directory (where `build.xml` is located) run this command:
```
$ ant clean jar
```

All the sources should be compiled in the `build/` directory. In the `dist/`
directory the resulting `android-vcard.jar` should be created, together with all
needed libraries.


Packaging library
-----------------

You can run command:
```
$ ant package
```

to obtain library in a form of a distribution package in the `dist/` directory.


Example usage
-------------

* For reading a vCard, see [examples/ReadExample.java](examples/ReadExample.java).
* For writing a vCard, see [examples/WriteExample.java](examples/WriteExample.java).


Similar projects
----------------

Other Java vCard libraries:

* [vCard4J](http://vcard4j.sourceforge.net/) ([project page](http://sourceforge.net/projects/vcard4j/))
* [Card Me](http://dma.pixel-act.com/) ([project page](http://sourceforge.net/projects/cardme/))
* [jPim](http://jpim.sourceforge.net/) ([project page](http://sourceforge.net/projects/jpim/)) - it's a PIM library, but it includes vCard manipulation support
* [iCal4j vCard](http://wiki.modularity.net.au/ical4j/index.php?title=VCard)

Good luck.
