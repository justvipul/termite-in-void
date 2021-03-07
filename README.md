


```
mkdir ~/git-src
cd ~/git-src
```
```
sudo xbps-install -Sy git-all gcc make automake autoconf gtk-doc glib-devel vala-devel gobject-introspection pkg-config intltool gettext-devel gnutls gtk+3 pango gnutls-devel gtk+3-devel pango-devel gperf pcre2-devel
```

```
git clone https://github.com/onlyvip/vte-ng.git
```
```
cd vte-ng
git checkout 0.50.2-ng 
git cherry-pick 53690d5c
```
###############################
```
./autogen.sh --prefix=/usr
```
####################################
      ##### OR ############
################################# 
```
./autogen.sh
```
#######################
```
make
sudo make install

cd ~/git-src
git clone --recursive https://github.com/thestinger/termite.git
cd termite
sed 's/PREFIX = \/usr\/local/PREFIX = \/usr/' -i Makefile
make
sudo make install

```

```
cd ~
wget https://raw.githubusercontent.com/thestinger/termite/master/termite.terminfo
tic -x termite.terminfo
```
