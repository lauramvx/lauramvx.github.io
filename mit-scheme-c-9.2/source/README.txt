1. License 

MIT-Scheme-c-9.2 is free software licensed under the GPLv2 with an
exception for linking OpenSSL. You should have received a full copy
of the license with this file, otherwise visit stupid.tw/mit-scheme-9.2/COPYING.

2. Your Download

This archive contains the unmodified source code of mit-scheme-c-9.2.
It's mirrored from https://ftp.gnu.org/gnu/mit-scheme/stable.pkg/9.2/mit-scheme-c-9.2.tar.gz
You can view its documentation here:
https://web.mit.edu/scheme_v9.2/doc/mit-scheme-ref/index.html#Top

3. Verify File Integrity

To cerify the file integrity, download the sha256 checksum and gpg signature
included with this download. You should have a single directory containing the files:
	mit-scheme-c-9.2.tar.gz
	mit-scheme-c-9.2.tar.gz.asc
	mit-scheme-c-9.2.tar.gz.sha256
From that directory, checksum the tarball to verify its file integrity:

sha256sum -c mit-scheme-c-9.2.tar.gz

To verify the signature:

gpg --keyserver keys.openpgp.org --recv-keys 85274C243D118B715F56DAF5B12234E55691131F
gpg --verify mit-scheme-c-9.2.tar.gz.asc mit-scheme-c-9.2.tar.gz

If either of these fails, something is wrong with your download and you shouldn't
continue installing!

4. Build

You can read the official documentation on the build process here:
https://web.mit.edu/scheme_v9.2/pdfdoc/mit-scheme-user.pdf
See pg. 4 (pdf pg. 8), 1.3, 'Portable C Installation', for buld instructions.

If you want to reproduce my patch, you can do the following:

tar -xzf mit-scheme-c-9.2.tar.gz
cd mit-scheme-c-9.2/src
sed -i '221s/.*/extern long C_return_value;/' microcode/cmpint.c
./etc/make-liarc.sh
make install

If you do that, it may compile on your machine.
Note that this patch only causes the src/ directory to build. The local 
documentation in doc/ will not be built.

5. Use

Try typing:

mit-scheme --version

It should display something like the following:

Release 9.2 || Microcode 15.3 || Runtime 15.7 || SF 4.41 || LIAR/C 4.118 || Edwin 3.116

If it does, congratulations! You have installed Mit-Scheme 9.2!
This version should work with slimv.
