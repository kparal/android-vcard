Java library for manipulating vCard files. The source code was extracted from the [Google Android](http://source.android.com/) project (version 1).

**This is not an application for Android. This is a development tool for PC.**

This project was created out of desperation that there is no decent Java vCard library. All libraries which I have found had problems with various file or character encodings, vCard versions, etc. Therefore I hacked a vCard related code out of Google Android project and made it into a standalone library.

Read UsageExamples for instructions how to easily use it.

I made a few changes in the Google's code (notably a few improvements in "UTF-8" support and redirected error reporting to a standard Java Logging facility). But I don't plan on any further additions or bugfixes. It does not make much sense to do custom changes into this project when Google probably fixed all the bugs already in newer releases of the Android code base. However, I also lack the time and motivation to extract this library again from the latest Android source code (the current library code is taken from Android 1.0). If you have the motivation, feel free to give a hand here. You can even maintain this whole project, you are warmly welcome.

**This project is currently unmaintained and looking for developers. There is also no user support, sorry. Don't ask me over email, thanks.**

Looking for other Java vCard libraries? See SimilarProjects.

<wiki:gadget border="0" url="http://stefansundin.com/stuff/flattr/google-project-hosting.xml" width="55" height="62" up\_uid="kamil.paral" up\_title="android-vcard" up\_url="http://code.google.com/p/android-vcard/" />

<a href='Hidden comment: 
[http://flattr.com/thing/49269/android-vcard http://api.flattr.com/button/button-static-50x60.png]
'></a>