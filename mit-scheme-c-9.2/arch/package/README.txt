1. License 

MIT-Scheme-c-9.2 is free software licensed under the GPLv2 with an
exception for linking OpenSSL. You should have received a full copy
of the license with this file, otherwise visit stupid.tw/mit-scheme-9.2/COPYING.

2. Your Download

mit-scheme-c-9.2.tar.gz contains the unmodified upstream source code.
It's mirrored from https://ftp.gnu.org/gnu/mit-scheme/stable.pkg/9.2/mit-scheme-c-9.2.tar.gz
You can view its documentation here:
https://web.mit.edu/scheme_v9.2/doc/mit-scheme-ref/index.html#Top

PKGBULD contains instructions for makepkg to compile it on Arch.
It automatically applies a patch that may make it compile on your machine.

3. Verify File Integrity

To cerify the file integrity, download the sha256 checksum and gpg signature
included with this download. You should have a single directory containing the files:
	mit-scheme-c-9.2.tar.gz
	mit-scheme-c-9.2.tar.gz.asc
	mit-scheme-c-9.2.tar.gz.sha256
From that directory, checksum the tarball to verify its file integrity:

sha256sum -c mit-scheme-c-9.2.tar.gz

To verify the signature:

gpg --verify mit-scheme-c-9.2.tar.gz.asc mit-scheme-c-9.2.tar.gz

If either of these fails, something is wrong with your download and you shouldn't
continue installing!

4. Build

In the directory containing both MAKEPKG and mit-scheme-c-9.2.tar.gz, run:

makepkg

After compiling for a long time, you should end up with a directory that
looks like this:

PKGBUILD
mit-scheme-c-9.2-1-x86_64.pkg.tar.zst
mit-scheme-c-9.2.tar.gz
mit-scheme-c-debug-9.2-1-x86_64.pkg.tar.zst
pkg
src

5. Install

Now simply run:

sudo pacman -U ./mit-scheme-c-9.2-1-x86_64.pkg.tar.zst

To uninstall, run:

sudo pacman -R mit-scheme-c

6. Use

Try typing:

mit-scheme --version

It should display something like the following:

Release 9.2 || Microcode 15.3 || Runtime 15.7 || SF 4.41 || LIAR/C 4.118 || Edwin 3.116

If it does, congratulations! You have installed Mit-Scheme 9.2!
This version should work with slimv.
