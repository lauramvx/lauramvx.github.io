1. License 

MIT-Scheme-c-9.2 is free software licensed under the GPLv2 with an
exception for linking OpenSSL. You should have received a full copy
of the license with this file, otherwise visit stupid.tw/mit-scheme-9.2/COPYING.

2. Your Download

You should have a precompiled Debian binary of the portable C version
of MIT-Scheme version 9.2.
It was made from the following source:
https://ftp.gnu.org/gnu/mit-scheme/stable.pkg/9.2/mit-scheme-c-9.2.tar.gz
You can view its documentation here:
https://web.mit.edu/scheme_v9.2/doc/mit-scheme-ref/index.html#Top

3. Verify File Integrity

To cerify the file integrity, download the sha256 checksum and gpg signature
included with this download. You should have a single directory containing the files:
	mit-scheme-c-9.2.deb
	mit-scheme-c-9.2.deb.asc
	mit-scheme-c-9.2.deb.sha256
From that directory, checksum the tarball to verify its file integrity:

sha256sum -c mit-scheme-c-9.2.deb

To verify the signature:

gpg --keyserver keys.openpgp.org --recv-keys 85274C243D118B715F56DAF5B12234E55691131F
gpg --verify mit-scheme-c-9.2.deb.asc mit-scheme-c-9.2.deb

If either of these fails, something is wrong with your download and you shouldn't
continue installing!

4. Install

To install, simply run:

sudo apt install ./mit-scheme-c.9.2.deb

To uninstall, run:

sudo apt remove ./mit-scheme-c.9.2.deb

5. Use

Try typing:

mit-scheme --version

It should display something like the following:

Release 9.2 || Microcode 15.3 || Runtime 15.7 || SF 4.41 || LIAR/C 4.118 || Edwin 3.116

If it does, congratulations! You have installed Mit-Scheme 9.2!
This version should work with slimv.

NOTE: Installing this software will automatically create symlinks to bchscheme, mit-scheme,
and scheme to mit-scheme-c in /usr/local/bin. If you would like to use another version of
MIT-Scheme alongside this one, you may have to remove or change these symlinks or use
update-alternatives to define behaviour.

Should you install the Debian repository's version of MIT-Scheme before or after installing
mit-scheme-c-9.2, mit-scheme will be set to mit-scheme-x86-64 by update-alternatives,
and SWANK will prefer mit-scheme-c which is 9.2. Therefore, installing both versions does
not necessarily conflict; they seem to be happy neighbours.
