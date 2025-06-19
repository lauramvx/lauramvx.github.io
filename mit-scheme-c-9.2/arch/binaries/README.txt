1. License 

MIT-Scheme-c-9.2 is free software licensed under the GPLv2 with an
exception for linking OpenSSL. You should have received a full copy
of the license with this file, otherwise visit stupid.tw/mit-scheme-9.2/COPYING.

2. Your Download

You should have a precompiled Arch binary of the portable C version
of MIT-Scheme version 9.2.
It was made from the following source:
https://ftp.gnu.org/gnu/mit-scheme/stable.pkg/9.2/mit-scheme-c-9.2.tar.gz
You can view its documentation here:
https://web.mit.edu/scheme_v9.2/doc/mit-scheme-ref/index.html#Top

3. Verify File Integrity

To cerify the file integrity, download the sha256 checksum and gpg signature
included with this download. You should have a single directory containing the files:
	mit-scheme-c-9.2-1-x86_64.pkg.tar.zst
	mit-scheme-c-9.2-1-x86_64.pkg.tar.zst.asc
	mit-scheme-c-9.2-1-x86_64.pkg.tar.zst.sha256
From that directory, checksum the tarball to verify its file integrity:

sha256sum -c mit-scheme-c-9.2-1-x86_64.pkg.tar.zst

To verify the signature:

gpg --verify mit-scheme-c-9.2-1-x86_64.pkg.tar.zst.asc mit-scheme-c-9.2-1-x86_64.pkg.tar.zst

If either of these fails, something is wrong with your download and you shouldn't
continue installing!

4. Install

To install, simply run:

sudo pacman -U ./mit-scheme-c-9.2-1-x86_64.pkg.tar.zst

To uninstall, run:

sudo pacman -R mit-scheme-c

5. Use

Try typing:

mit-scheme --version

It should display something like the following:

Release 9.2 || Microcode 15.3 || Runtime 15.7 || SF 4.41 || LIAR/C 4.118 || Edwin 3.116

If it does, congratulations! You have installed Mit-Scheme 9.2!
This version should work with slimv.
