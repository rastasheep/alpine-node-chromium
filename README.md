# alpine-node-chromium
### Dockerized chromium, built on top of [official Node alpine](https://hub.docker.com/_/node/) images.

## About image

- [What, why, how?]()
- [Image tags]()
- [Installed packages]()
- [Environment variables]()

### • What, why, how?

### • Image tags

### • Installed packages
- [udev](https://pkgs.alpinelinux.org/package/v3.5/main/x86_64/udev)
- [ttf-opensans](https://pkgs.alpinelinux.org/package/edge/testing/x86_64/ttf-opensans)
- [chromium](https://pkgs.alpinelinux.org/package/edge/community/x86_64/chromium)

### • Environment variables
- `CHROME_BIN=/usr/bin/chromium-browser`
- `LIGHTHOUSE_CHROMIUM_PATH=/usr/bin/chromium-browser`

## Issues

If you run into any problems with this image, please check (and potentially file new) issues on the [rastasheep/alpine-node-chromium](https://github.com/rastasheep/alpine-node-chromium/issues) repository, which is the source for this image.

## License

alpine-node-chromium is licensed under the [MIT license](http://opensource.org/licenses/MIT).

