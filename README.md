# Jacdac CLI

A command line interface to support various tasks using Jacdac.

**Jacdac** is a plug-and-play hardware/software stack
for **microcontrollers** and their peripherals (sensors/actuators),
with applications to rapid prototyping, making, and physical computing.

This repository contains a command line interface tool for the [Jacdac](https://aka.ms/jacdac) protocol.

-   **[Jacdac Protocol Documentation](https://aka.ms/jacdac/)**
-   **[CLI Documentation](https://jacdac.github.io/jacdac-docs/clients/cli/)**
-   Discussions at https://github.com/jacdac/jacdac/discussions
-   Issues are tracked on https://github.com/jacdac/jacdac/issues

The rest of this page is for developers of the `jacdac-ts` library.

## Installation

-   Install [nodejs.org](https://nodejs.org/) 14+
-   Install the tool globally.

```bash
sudo npm install -g jacdac-cli
```

If the native module installation fails, try adding `--unsafe`

```bash
sudo npm install -g jacdac-cli --unsafe
```

## Usage

### `jacdac parse`

Parses a logic analyzer log and replays the packets

```
jacdac parse log.txt
```

### `jacdac devtools`

Starts websocket and native socket server that acts as a bridge between a web dashboard and a client implementation. 
This allows to test a native client using the latest version of the web developer tools.
This command will work in [GitHub codespaces](https://github.com/features/codespaces). 

```
jacdac devtools
```

#### `jacdac devtools --device-script <file>`

Starts the devtools web site and also watches/uploads the source of a given [DeviceScript](https://aka.ms/devicescript) to the development web site. The dev web site will automatically compile and potentially deploy the DeviceScript program to a connected device.

## Contributing

This project welcomes contributions and suggestions.