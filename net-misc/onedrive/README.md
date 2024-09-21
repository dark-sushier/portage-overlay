# net-misc/onedrive

## Usage

``` shell
emerge --ask net-misc/onedrive
mkdir -p ~/.config/onedrive
echo 'sync_dir = "~/OneDrive"' > ~/.config/onedrive/config
## specify the directory to sync
echo 'emacs' > ~/.config/onedrive/sync_list
onedrive --sync --verbose --dry-run
onedrive --sync
systemctl --user enable onedrive
systemctl --user start onedrive
```
## See Also

- https://github.com/abraunegg/onedrive/blob/master/docs/install.md#dependencies-gentoo
- https://github.com/abraunegg/onedrive/blob/master/contrib/gentoo/onedrive-2.5.0.ebuild
