<p align="center">
	<img src="https://raw.githubusercontent.com/prettierlichess/prettierlichess/master/res/prettierlichess-logo.svg" width=150>
	<h1 align="center">Prettierlichess</h1>
</p>
<p align="center">
	<a href="https://prettierlichess.github.io/">
		<img src="https://img.shields.io/badge/Official Website-gray?logo=lichess&style=for-the-badge">
	</a>
	<a href="https://chrome.google.com/webstore/detail/prettier-lichess/epgnobcgnmchnhgkgpedebbmhbblfcob">
		<img src="https://img.shields.io/chrome-web-store/rating/epgnobcgnmchnhgkgpedebbmhbblfcob?color=blue&label=Chrome%20store&logo=googlechrome&style=for-the-badge">
	</a>
	<a href="https://addons.mozilla.org/en-US/firefox/addon/prettier-lichess/">
		<img src="https://img.shields.io/amo/rating/prettier-lichess?color=blue&label=Firefox%20store&logo=firefox&style=for-the-badge">
	</a>
	<a href="https://github.com/prettierlichess/prettierlichess/releases/latest">
		<img src="https://img.shields.io/github/v/release/prettierlichess/prettierlichess?style=for-the-badge">
	</a>
</p>

[Lichess](https://lichess.org/) is an amazing platform that has more than just the ability to play chess, and all for free. Unfortunately I felt like it didn't show this well with it's current design, nor did it show that it was a site that resides in 2023. Now with Prettier Lichess, Lichess becomes more readable, more discoverable, and prettier (plus customizable colors)!

## Code and license

Here is the source code for both the chrome and firefox extension! It's simple but it's mine. Feel free to download, fork, use, and mess with it all you want. No attribution or anything required.

The extension is not published in the Apple Store, but it is possible to get it to work in Safari by creating a build with XCode. More information about that can be found [here](https://github.com/prettierlichess/prettierlichess/issues/153).

## General Usage

### Quick install (Chrome, no build)

1. Go to [github.com/adxy/prettylichess](https://github.com/adxy/prettylichess), click the green **Code** button, then **Download ZIP**.
2. Find the downloaded ZIP file and unzip it (double-click it). You get a folder called `prettylichess-main`.
3. In Chrome, type `chrome://extensions` in the address bar and press Enter.
4. Turn on **Developer mode** (switch in the top right).
5. Click **Load unpacked** (top left).
6. Open the unzipped `prettylichess-main` folder, select the `src` folder inside it, and click **Select**.

Done! Open [lichess.org](https://lichess.org/) to see it. The settings pop-up (colour picker) needs the full install below.

#### Copy for agent

> Install the Prettier Lichess Chrome extension without building. Download `https://github.com/adxy/prettylichess/archive/refs/heads/main.zip` and unzip it. Open `chrome://extensions`, enable Developer mode, click "Load unpacked" and select the `src` folder inside the unzipped folder (absolute path). Confirm "Prettier Lichess" appears and is enabled. Note the settings pop-up will not work from `src`.

### Full install (Chrome, with working settings pop-up)

1. Download and unzip the repo (steps 1 and 2 above).
2. Install [Node.js](https://nodejs.org/) if you don't have it.
3. Open a terminal inside the unzipped `prettylichess-main` folder and run:
   ```
   npm install
   npm run build:chrome
   ```
4. In Chrome, go to `chrome://extensions` and turn on **Developer mode**.
5. Click **Load unpacked**, select the new `dist-chrome` folder inside `prettylichess-main`, and click **Select**.

To update after changes, run `npm run build:chrome` again and click the reload icon on the extension.

#### Copy for agent (full install)

> Install the Prettier Lichess Chrome extension. Download `https://github.com/adxy/prettylichess/archive/refs/heads/main.zip` and unzip it. In the unzipped folder run `npm install` then `npm run build:chrome`. Then open `chrome://extensions`, enable Developer mode, click "Load unpacked" and select the `dist-chrome` folder (absolute path). Confirm "Prettier Lichess" appears and is enabled.

Set Lichess to dark background to have the best compatibility with prettierlichess. \
With the pop-up you can then customise the colours and choose themes. Have fun!

## Community Themes

Check out the community driven theme library [here](https://github.com/algertc/prettierlichess-themes).

## Development workflow

### Setup

Execute this command for the setup to get all packages:

```
npm install
```

### Build

Build outputs are separated per browser:

-   Chrome build → `dist-chrome/`
-   Firefox build → `dist-firefox/`

For a single combined build (both Chrome and Firefox), run:

```
npm run build
```

To build just one target:

```
npm run build:chrome
npm run build:firefox
```

The Firefox build also emits a Firefox-friendly `manifest.json` into `dist-firefox/` based on `src/manifest.firefox.json`.

### Watch/serve

To rebuild automatically when changes are made (watches both Chrome and Firefox builds simultaneously), run:

```
npm run watch   # Watches both builds, writes to dist-chrome/ and dist-firefox/
```

For the popup test server:

```
npm run popup:run    # builds Chrome then serves from dist-chrome/
```

That's pretty much it :smiley:

For a more detailed description of how the extension works, have a look [here](https://github.com/prettierlichess/prettierlichess/blob/master/.github/CONTRIBUTING.md#structure-of-the-extension).

## Questions, bugs and feature requests

If you have any questions, feature requests or want to report bugs, feel free to [create an issue](https://github.com/prettierlichess/prettierlichess/issues/new).

## How to contribute

For more information, see the [contribution page](https://github.com/prettierlichess/prettierlichess/blob/master/.github/CONTRIBUTING.md).

## Contributors

Thanks to everyone who contributed to this project! Prettierlichess exists thanks to you.
