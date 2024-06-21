# dark-sushier portage-overlay

personal portage repository for [Gentoo Linux](http://www.gentoo.org/)

## Usage

``` shell
eselect repository add dark-sushier git https://github.com/dark-sushier/portage-overlay.git
emerge --sync dark-sushier
```

## Create ebuild

see https://wiki.gentoo.org/wiki/Basic_guide_to_write_Gentoo_Ebuilds/ja

``` shell
mkdir -p <app-category>/<app-name>
cd <app-category>/<app-name>
export PN=<app-name>
export PV=<app-version>
cp /var/db/repos/gentoo/skel.ebuild ${PN}-${PV}.ebuild
cp /var/db/repos/gentoo/skel.metadata.xml metadata.xml
sudo GENTOO_MIRRORS="" ebuild ./${PN}-${PV}.ebuild
sudo ebuild ./${PN}-${PV}.ebuild clean test install
sudo ebuild ./${PN}-${PV}.ebuild clean install merge
```

## see also

- https://seppuku.club/unix-like/gentoo-overlay-enter/
- https://wiki.gentoo.org/wiki/Basic_guide_to_write_Gentoo_Ebuilds/ja
