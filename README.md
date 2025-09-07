<h1 align="center"><a href="https://streamlink.github.io/">Streamlink-ClearKey<br><img height="150" alt="Streamlink" src="https://raw.githubusercontent.com/streamlink/streamlink/master/icon.svg"></a></h1>

<p align="center">
  <a href="https://streamlink.github.io/install.html"><img alt="Supported Python versions" src="https://img.shields.io/pypi/pyversions/streamlink.svg?style=flat-square&maxAge=86400"></a>
  <a href="https://github.com/streamlink/streamlink"><img alt="License" src="https://img.shields.io/github/license/streamlink/streamlink.svg?style=flat-square&maxAge=86400"></a>
</p>

<p align="center">
  A Python library and command-line interface which pipes streams from various services into a video player.<br>
  Avoid resource-heavy and unoptimized websites, and still enjoy streamed content.
</p>

## About This Fork

This fork adds ClearKey support to Streamlink for DRM protected streams.

**Tested with:**

- CENC MPD streams
- SAMPLE-AES-CTR HLS streams

## Credits

Thanks to ImAleeexx - he was the first one to add the code to work with keys: [ImAleeexx/streamlink-drm](https://github.com/ImAleeexx/streamlink-drm)

# 📦 Installation

```bash
pip3 install --user -U git+https://github.com/Ogretm3n/streamlink-clearkey.git
```

## Usage

```bash
streamlink MPD/HLS_URL [quality] --key HEX
```

**For multiple keys:**

```bash
streamlink MPD/HLS_URL [quality] --key HEX --key HEX
```

**Note:** Only add the key (not the kid).

# 🎯 Features

Streamlink is built on top of a plugin system which allows support for new services to be added easily.  
Most of the popular streaming services are supported, such as [Twitch](https://www.twitch.tv), [YouTube](https://www.youtube.com), and many more.

A list of all plugins currently included can be found on the [plugins page][streamlink-plugins].

# 💡 Quickstart

After installing, simply run:

```sh
streamlink "STREAMURL" best
```

For DRM protected streams:

```sh
streamlink "STREAMURL" best --key "YOUR_KEY_HERE"
```

The default behavior of Streamlink is to play back streams in the [VLC player][player-vlc], but a lot of other options and output methods are available, such as writing the stream to the filesystem, reading stream metadata, etc.

For more in-depth usage, please refer to the [CLI documentation][streamlink-documentation-cli].

An [API guide][streamlink-documentation-apiguide] and [API reference][streamlink-documentation-apiref] is available for Python implementors of Streamlink.

# 🙏 Contributing

All contributions are welcome.
Feel free to open a new thread on the issue tracker or submit a new pull request.
Please read [CONTRIBUTING.md][contributing] first. Thanks!

# ❤️ Support

If you think that Streamlink is useful and if you want to keep the project alive, then please consider supporting its maintainers by sending a small and optionally recurring tip via the [available options][support].  
Your support is very much appreciated, thank you!

---

**Thanks to the Streamlink team for creating this wonderful project.**

  [streamlink-documentation-cli]: https://streamlink.github.io/cli.html
  [streamlink-documentation-apiguide]: https://streamlink.github.io/api_guide.html
  [streamlink-documentation-apiref]: https://streamlink.github.io/api.html
  [streamlink-plugins]: https://streamlink.github.io/plugins.html
  [player-vlc]: https://www.videolan.org/vlc/
  [contributing]: https://github.com/streamlink/streamlink/blob/master/CONTRIBUTING.md
  [support]: https://streamlink.github.io/latest/support.html