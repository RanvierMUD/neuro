# \<Neuro\>

Neuro is a simple and easily-extensible websocket client to use with the [Ranvier](https://ranviermud.com) MUD game engine.

<p align="center"><img width="640" src="https://raw.githubusercontent.com/shawncplus/neuro/master/assets/demo.gif"></p>

It currently does not ship with any distribution strategy (e.g.,
[electron-packager](https://github.com/electron-userland/electron-packager)) so if you want to distribute this client to
your players you will have to use that package or something similar to build the distributables yourself.

Neuro is built with [Electron](https://github.com/electron) and [Polymer](https://polymer-project.org). The main place
to start will be in `src/neuro-app/neuro-app.html`. To use with Ranvier your Ranvier server must be using the
`ranvier-websocket` bundle to enable websocket connections. If you wish to modify the data Ranvier is sending to Neuro
follow the documentation for [Extending Bundles](http://ranviermud.com/extending/bundles/#creating-a-bundle) (in short:
copy `ranvier-websockets` to a new folder, disable the `ranvier-websockets` bundle in `ranvier.json` and enable your new
bundle.

## Running

```
git clone https://github.com/shawncplus/neuro
cd neuro
npm install
bower install
npm run start
```

## Creating Releases

To create distributables for Neuro simply run `npm run package-<platform>` where platform is one of `linux`, `win`, or
`mac`. Note for Mac there may be some extra signing process but I'm not sure since I've never used it, caveat emptor.

## Features

Neuro is a minimal client created in the same spirit as Ranvier: unopinionated but with sane examples for you to build
from without tearing your hair out. Out of the box it has the following features:

* Player HUD for health/mana/etc.
* Active effect list
* Persistent options for font size/select last command
* Target health frames with support for multiple targets
* Command history
* Auto-linking urls
