[![Build Status](https://semaphoreci.com/api/v1/d-programming-gdc/gdc/branches/stable/badge.svg)](https://semaphoreci.com/d-programming-gdc/gdc)

### What is GDC?

GDC is a GPL implementation of the D compiler which integrates the open source D front end with GCC.

The GNU D Compiler (GDC) project was originally started by David Friedman in 2004 until early 2007 when he disappeared from the D scene, and was no longer able to maintain GDC. Following a revival attempt in 2008, GDC is now under the lead of Iain Buclaw who has been steering the project since 2009 with the assistance of its contributors, without them the project would not have been nearly as successful as it has been.

Documentation on GDC is available from [the wiki][wiki]. Any bugs or issues found with using GDC should be reported at [our bugzilla site][bugs]. For help with GDC, the [D.gnu][maillist] mailing list is the place to go with questions or problems.

Work is currently under way to merge GDC into a future release of GCC. Assistance of any sort during this time would be invaluably appreciated. Feel free to contact via [email][email] or join in at #d.gdc on FreeNode.

### Checking out GCC

The GCC submodule was initially created using the following command.
```
git submodule add --depth 1 -b master https://github.com/gcc-mirror/gcc.git gcc
```

For newly cloned repositories, this command below obtains GCC sources.  If it fails, then increase depth until it succeeds.
```
git submodule update --init --depth 50 gcc
```

To update to latest GCC trunk, use the following command.
```
git submodule update --remote --depth 1 gcc
```

### Building

The master branch of this project closely follows [GCC development branch][gcc-devel], which if you intend to use GDC for production applications, is likely not the version of GCC you want to build against.  For versions of GDC releases, obtain sources from GCC downloads site.

[home]: http://gdcproject.org
[wiki]: http://wiki.dlang.org/GDC
[bugs]: http://bugzilla.gdcproject.org
[maillist]: http://forum.dlang.org/group/D.gnu
[email]: mailto:ibuclaw@gdcproject.org
[gcc-devel]: http://gcc.gnu.org/git/?p=gcc.git;a=shortlog
