# PatternRecognition
brew doctor
vim /user/local/Library/brew.rb
#!/System/Library/Frameworks/Ruby.framework/Versions/Current/usr/bin/ruby -W0
brew doctor
brew update

Homebrew requires Leopard or higher. For Tiger support, see:
https://github.com/mistydemeo/tigerbrew

% ruby -e "$(curl -fsSkL raw.github.com/mistydemeo/tigerbrew/go/install)"
It appears Homebrew is already installed. If your intent is to reinstall you
should do the following before running this installer again:
    rm -rf /usr/local/Cellar /usr/local/.git && brew cleanup

% rm -rf /usr/local/Cellar /usr/local/.git && brew cleanup
Homebrew requires Leopard or higher. For Tiger support, see:
https://github.com/mistydemeo/tigerbrew

[10:59PM]% ruby -e "$(curl -fsSkL raw.github.com/mistydemeo/tigerbrew/go/install)"
==> This script will install:
/usr/local/bin/brew
/usr/local/Library/...
/usr/local/share/man/man1/brew.1
==> The following directories will be made group writable:
/usr/local/lib/pkgconfig
/usr/local/share/info

Press ENTER to continue or any other key to abort
==> /usr/bin/sudo /bin/chmod g+rwx /usr/local/lib/pkgconfig /usr/local/share/info
Password:
==> Downloading and Installing Homebrew...
remote: Counting objects: 271083, done.
remote: Compressing objects: 100% (60/60), done.
remote: Total 271083 (delta 37), reused 0 (delta 0), pack-reused 271023
Receiving objects: 100% (271083/271083), 49.77 MiB | 782.00 KiB/s, done.
Resolving deltas: 100% (196123/196123), done.
From https://github.com/mistydemeo/tigerbrew
 * [new branch]      master     -> origin/master
 HEAD is now at 1eccd9d csfml: remove erroneous extra lines
 ==> Installation successful!
 You should run `brew doctor' *before* you install anything.
 Now type: brew help
 ruby -e "$(curl -fsSkL raw.github.com/mistydemeo/tigerbrew/go/install)"  28.07s user 4.40s system 41% cpu 1:18.47 total
[11:00PM]%

[11:01PM]% vim ~/.zshrc

14 # for brew
15 export PATH=/usr/local/sbin:/usr/local/bin:$PATH

[11:03PM]% brew doctor

[11:03PM]% brew update
Updated Tigerbrew from 1eccd9db to 1eccd9db.
==> New Formulae
homebrew/dupes/bzip2     homebrew/dupes/krb5      homebrew/dupes/libedit   homebrew/dupes/xar
==> Updated Formulae
homebrew/dupes/diffstat      homebrew/dupes/gpatch    homebrew/dupes/heimdal       homebrew/dupes/m4        homebrew/dupes/openssh   homebrew/dupes/tcpdump
homebrew/dupes/ed        homebrew/dupes/grep      homebrew/dupes/lapack        homebrew/dupes/make      homebrew/dupes/rsync     homebrew/dupes/whois
homebrew/dupes/file-formula  homebrew/dupes/groff     homebrew/dupes/libpcap       homebrew/dupes/nano      homebrew/dupes/screen
homebrew/dupes/gdb       homebrew/dupes/gzip      homebrew/dupes/lsof          homebrew/dupes/openldap      homebrew/dupes/tcl-tk
==> Deleted Formulae
homebrew/dupes/ab        homebrew/dupes/apr       homebrew/dupes/fetchmail     homebrew/dupes/tidy
homebrew/dupes/ant       homebrew/dupes/apr-util      homebrew/dupes/httpd
[11:03PM]%

[11:04PM]% brew tap homebrew/science
==> Tapping homebrew/science
Cloning into '/usr/local/Library/Taps/homebrew/homebrew-science'...
remote: Counting objects: 526, done.
remote: Compressing objects: 100% (522/522), done.
remote: Total 526 (delta 4), reused 161 (delta 3), pack-reused 0
Receiving objects: 100% (526/526), 408.65 KiB | 303.00 KiB/s, done.
Resolving deltas: 100% (4/4), done.
Checking connectivity... done
Tapped 519 formulae (546 files, 2.8M)
[11:05PM]%

[11:06PM]% brew install opencv
==> Installing opencv from homebrew/homebrew-science
==> Tapping homebrew/python
Cloning into '/usr/local/Library/Taps/homebrew/homebrew-python'...
remote: Counting objects: 16, done.
remote: Compressing objects: 100% (16/16), done.
remote: Total 16 (delta 1), reused 5 (delta 0), pack-reused 0
Unpacking objects: 100% (16/16), done.
Checking connectivity... done
Tapped 13 formulae (51 files, 216K)
==> Installing dependencies for homebrew/science/opencv: gmp, mpfr, libmpc, xz, isl, gcc, eigen, jpeg, libpng, libtiff, ilmbase, openexr, homebrew/python/numpy
==> Installing homebrew/science/opencv dependency: gmp
==> Downloading http://ftpmirror.gnu.org/gmp/gmp-6.0.0a.tar.bz2
==> Downloading from: http://mirror.jre655.com/GNU/gmp/gmp-6.0.0a.tar.bz2
######################################################################## 100.0%
==> ./configure --prefix=/usr/local/Cellar/gmp/6.0.0a --enable-cxx
==> make
==> make check
make[4]: *** [check-TESTS] Error 1
make[3]: *** [check-am] Error 2
make[2]: *** [check-recursive] Error 1
make[1]: *** [check-recursive] Error 1
make: *** [check] Error 2

READ THIS: https://github.com/mistydemeo/tigerbrew/wiki/troubleshooting

brew install opencv  138.96s user 50.54s system 192% cpu 1:38.52 total
[11:08PM]%
