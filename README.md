
termite install in void. 

```
mkdir ~/git-src
cd ~/git-src
```
## dependencies
```
sudo xbps-install -Su
sudo xbps-install -Sy git-all gcc make automake autoconf gtk-doc glib-devel vala-devel gobject-introspection pkg-config intltool gettext-devel gnutls gtk+3 pango gnutls-devel gtk+3-devel pango-devel gperf pcre2-devel base-devel git curl cmake wget xprop
``` 
## get vte
```
git clone https://github.com/onlyvip/vte-ng.git
cd vte-ng
git checkout 0.50.2-ng 
git cherry-pick 53690d5c
./autogen.sh --prefix=/usr
make
sudo make install
```
get termite
```
cd ~/git-src
git clone --recursive https://github.com/thestinger/termite.git
cd termite
sed 's/PREFIX = \/usr\/local/PREFIX = \/usr/' -i Makefile
make
sudo make install
```

for saner working od termite

```
cd ~
wget https://raw.githubusercontent.com/thestinger/termite/master/termite.terminfo
tic -x termite.terminfo
```
