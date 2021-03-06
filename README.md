# Dugite - The Native Bits

[![Travis Build Status](https://api.travis-ci.com/desktop/dugite-native.svg?token=vdtkHSqgzNMgfyZkfVbP&branch=master)](https://travis-ci.com/desktop/dugite-native)
[![AppVeyor Build status](https://ci.appveyor.com/api/projects/status/j0mmb48vs7imoour/branch/master?svg=true)](https://ci.appveyor.com/project/github-windows/dugite-native/branch/master)

This project contains the tooling for building a version of Git that is optimized for
scripted usage in applications. It also removes many non-core features:

 - no linking to system libraries
 - use symlinks to reduce output size
 - no Perl runtime
 - no dependency on OpenSSL
 - no Tcl/Tk GUI
 - no translation of error messages
 - no 32-bit support

There are also additional customizations included in this toolchain:

 - Git-LFS
 - certificate bundle for Linux consumers

**Note:** this is not intended to installed by end users - [go here](https://git-scm.com/)
to download Git for your operating system.

### Status

This project is under active development for Git-related projects at GitHub. This will stabilize as this library gets more usage in production.

### Roadmap

It is expected that this toolchain will be updated as Git and it's other dependencies are updated, to ensure applications are running on the latest
stable version of Git.

Feel free to open issues or pull requests about fixes or optimizations we can incorporate
into the packaging process. Refer to the [CONTRIBUTING.md](./CONTRIBUTING.md) file for instructions and the [documentation](./docs/) sections for more information about the repository.

Bugfixes and feature requests for Git should be discussied on the [Git mailing list](https://git.wiki.kernel.org/index.php/GitCommunity).

### Supported Platforms

 - Windows 7 and later
 - macOS 10.9 and up
 - Linux (tested on Ubuntu Precise/Trusty and Fedora 24)

### Credits

The [Git for Windows](https://git-for-windows.github.io) project already
provides a minimal environment (called 'MinGit') with each release that covers
most of the above requirements.

[Travis](https://travis-ci.org/) provide the build infrastructure for compiling and packaging Git across all the necessary platforms. [AppVeyor](https://appveyor.com/) also provides build infrastructure for testing Windows-specific features.
