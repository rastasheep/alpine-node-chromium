# alpine-node-chromium
### Dockerized chromium, built on top of [official Node alpine](https://hub.docker.com/_/node/) images.

## About image

- [What, why, how?](#-what-why-how)
- [Image tags](#-image-tags)
- [Installed packages](#-installed-packages)
- [Environment variables](#-environment-variables)

### • What, why, how?

Image intended to be used in modern front-end development workflow, to be exact, with [Karma test runner](https://karma-runner.github.io/1.0/index.html) via [karma-chrome-launcher](https://github.com/karma-runner/karma-chrome-launcher) which uses headless Chromium instead traditional PhantomJS which doesn't play well with Alpine linux.

If you're interested into actual Karma configuration, it looks like:
```
  browsers: ['ChromiumNoSandbox'],
  customLaunchers: {
    ChromiumNoSandbox: {
      base: 'ChromiumHeadless',
      flags: ['--no-sandbox', '--headless', '--disabled-gpu']
    }
  }
```

### • Image tags

- rastasheep/alpine-node-chromium:8-alpine (based on: node:8-alpine)
- rastasheep/alpine-node-chromium:7-alpine (based on: node:7-alpine)
- rastasheep/alpine-node-chromium:6-alpine (based on: node:6-alpine)
- rastasheep/alpine-node-chromium:4-alpine (based on: node:4-alpine)

### • Installed packages

Chromium stuff
- [udev](https://pkgs.alpinelinux.org/package/v3.5/main/x86_64/udev)
- [ttf-opensans](https://pkgs.alpinelinux.org/package/edge/testing/x86_64/ttf-opensans)
- [chromium](https://pkgs.alpinelinux.org/package/edge/community/x86_64/chromium)

Image optimization libs
- [gifsicle](https://pkgs.alpinelinux.org/package/edge/community/x86_64/gifsicle)
- [pngquant](https://pkgs.alpinelinux.org/package/edge/community/x86_64/pngquant)
- [optipng](https://pkgs.alpinelinux.org/package/v3.6/community/x86_64/optipng)
- [libjpeg-turbo-utils](https://pkgs.alpinelinux.org/package/edge/main/x86_64/libjpeg-turbo-utils)

### • Environment variables
- `CHROME_BIN=/usr/bin/chromium-browser`
- `LIGHTHOUSE_CHROMIUM_PATH=/usr/bin/chromium-browser`

## Issues

If you run into any problems with this image, please check (and potentially file new) issues on the [rastasheep/alpine-node-chromium](https://github.com/rastasheep/alpine-node-chromium/issues) repository, which is the source for this image.

## License

alpine-node-chromium is licensed under the [MIT license](http://opensource.org/licenses/MIT).

