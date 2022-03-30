# text-logo.png

<sup>**_You have a project name, now you have a logo !_**</sup>

Using a text, a font and few configurations to generate a png, which you can embed in your REAME.md for a neat look.

Drop in replacement for [logo.svg](https://github.com/bubkoo/logo.svg).

---

<!--
Badge template:
[![Title](https:// image url)](https:// link url)
-->

![GPL-3.0](https://img.shields.io/github/license/kane-thornwyrd/text-logo.png)

---

### **[Website](https://kane-thornwyrd.github.io/text-logo.png) | [Wiki](https://github.com/kane-thornwyrd/text-logo.png/wiki) | [Issues](https://github.com/kane-thornwyrd/text-logo.png/issues) | [Contributing](https://github.com/kane-thornwyrd/text-logo.png/blob/master/.github/CONTRIBUTING.md)**

Built with 💗 by [Kane Thornwyrd](https://github.com/kane-thornwyrd) and [contributors](https://github.com/kane-thornwyrd/text-logo.png/graphs/contributors)

---

## Table of Contents

- [Features](#features)
- [Installation](#installation)
  - [For CLI usages](#for-cli-usages)
  - [For API usages](#for-api-usages)
- [Workflow](#workflow)
- [Philosophy](#philosophy)
- [See Also](#see-also)
- [License](#license)
- [Contributing](#support)

## Features

<!-- List the project features here -->

- CLI & API interfaces.
- Generate a logo.png using your text, your font and your configuration.
- That's all folks !

<sub>[⇧ back to top](#table-of-contents)</sub>

## Installation

### For CLI usages

> Not required, you can use it via `npx`.

> Not even advised.

```sh
$ npm i -g text-logo.png
```

### For API usages

```sh
$ npm i -SD text-logo.png
```

<sub>[⇧ back to top](#table-of-contents)</sub>

## Workflow

### CLI options:

- `-l, --logo` [string]: (optional) The logo text. Default is the project `name` in the `package.json`.
- `-x` [integer]: (optional) Horizontal position of the beginning of the text. Default is `0`.
- `-y` [integer]: (optional) Vertical position of the baseline of the text. Default is `0`.
- `-f, --font` [string]: (**required**) relative path or url to the ttf/otf font file.
- `-s, --fontSize` [integer]: (optional) Specify the font size. Default is `72`.
- `-o, --output` [string]: (optional) Specify the output path. Default is `logo.png`.
- `-c, --config` [string]: (optional) Specify the configuration file relative path or url, it should be in json format and contain only [the configuration object](#configuration-object-exemple). **If the config file is specified, it will take precedence on the other `[options]` arguments**.
- `-O, --overwrite` [`true`|`false`|`y`|`n`|`0`|`1`]: (optional) Overwrite when a logo file exist. Default is `true`.
- `-k, --kerning` [`true`|`false`|`y`|`n`|`0`|`1`]: (optional) Take kerning information into account. Default is `true`.
- `-d, --divided` [`true`|`false`|`y`|`n`|`0`|`1`]: (optional) Generate individual path for every char. Default is `false`.
- `-v, -V, --version`: Print the current version of `Text-Logo.png`.
- `-h, --help`: You are looking at it.

<sub>[⇧ back to top](#table-of-contents)</sub>

### Configuration object:

_All that is optional in the CLI options are optional here._

```json
{
  "logo": "your text string",
  "x": 0,
  "y": 0,
  "font": ".fonts/myfont.ttf",
  "fontSize": 72,
  "output": "logo.png",
  "overwrite": true,
  "kerning": true,
  "divided": false
}
```

So, a barebone version could be:

```json
{
  "font": ".fonts/myfont.ttf"
}
```

<sub>[⇧ back to top](#table-of-contents)</sub>

### CLI usages:

**If you did not installed it in your project:**

```sh
$ npx text-logo.png [options]
```

**If you installed it in your project, from cli:**

```sh
$ ./node_module/.bin/text-logo.png [options]
```

**If you installed it in your project, from `package.json` - `scripts` section:**

```json
{
  "name": "your project name",
  "version": "0.0.0",
  "description": "[...]",
  "scripts": {
    "logo": "text-logo.png"
  },
  "config": {
    "text-logo.png": "[Object:text-logo.png configuration] or [string: relative path to the configuration file]"
  }
}
```

<sub>[⇧ back to top](#table-of-contents)</sub>

### API usage

```js
const TextLogoPNG = require("text-logo.png")[TextLogoPNG];
const configuration = require("name-of-your-text-logo.png-config-file.json");

const logo = new TextLogoPNG(configuration); // logo will be a stream.Readable
```

For more informations on stream.Readable, [check out the Node.js documentation](https://nodejs.org/dist/latest-v16.x/docs/api/stream.html#class-streamreadable).

<sub>[⇧ back to top](#table-of-contents)</sub>

## Philosophy

I love a well written and pleasant to the eyes `README.md`, thus I adopted [logo.svg](https://github.com/bubkoo/logo.svg), especially when I wrote [Boilerplate](https://github.com/kane-thornwyrd/boilerplate)…

And I have put my hands back on `boilerplate`, after few years, to upgrade everything and fix security issues, and noticed that `logo.svg` is using an old and bugged version of the `dot-prop` library (thanks `npm audit`), and was also quite dormant, with the last commit 6 years ago (and a poor issue filled just to ask why) at the moment I wrote those lines.

So, I have sniffed around a bit in the code of `logo.svg` about its latest version, I didn't even used yet (?). And found out that bubkoo added a call to `update-notifier`, which is fine, I guess, but I prefer simpler pieces of code, without call to a server for a trivial piece of information, however secure and approved that server could be.

So, the corollary to those statements is that this software (text-logo.png) is feature complete, there will \***\*never\*\*** have any other functionalities! (I'll try to be friendly, but asking about adding more features is a de facto questioning about your reading and cognitive capacities)

<sub>[⇧ back to top](#table-of-contents)</sub>

## See Also

- The Kane's projects [Boilerplate](https://github.com/kane-thornwyrd/boilerplate) project
- Bubkoo [logo.svg](https://github.com/bubkoo/logo.svg) project

<sub>[⇧ back to top](#table-of-contents)</sub>

## License

This project is licensed under the General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

<sub>[⇧ back to top](#table-of-contents)</sub>

## Contributing

Please take a look at our [contributing guidelines](CONTRIBUTING) if you're interested in helping!

<sub>[⇧ back to top](#table-of-contents)</sub>
