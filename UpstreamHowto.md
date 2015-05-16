This page is intended for developers of android-vcard to easily document how to sync the library with the latest upstream version.

WARNING: This is really obsolete. It was created against Google Android v1.

## Links ##

  * http://source.android.com/download
  * http://android.git.kernel.org/

## Sync android-vcard with latest upstream ##

  1. Checkout latest android code:
```
$ git clone git://android.git.kernel.org/platform/frameworks/base.git android-frameworks-base
```
  1. Copy [upstream.md5](http://code.google.com/p/android-vcard/source/browse/trunk/android-vcard/upstream.md5) to `android-frameworks-base`.
  1. Run in there:
```
$ cut -d ' ' -f 3 upstream.md5 | xargs md5deep -lx upstream.md5
```
  1. Only changed files will be listed.
  1. Sync changed upstream files to library files.
  1. Don't forget to update `upstream.md5`.