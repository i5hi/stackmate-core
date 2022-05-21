<h1 align="center">STACKMATE-CORE</h1>

### NOTE
This library is now being actively developed [here](https://github.com/i5hi/StackmateNetwork/stackmate-core.git).

This library will be updated here soon.

### TLDR
A Rust-C FFI library exposing composite functionality from [rust-bitcoin](https://github.com/rust-bitcoin/rust-bitcoin/) & [bdk](https://github.com/bitcoindevkit/bdk); to create cross-platform descriptor wallets.

Currently used by [Stackmate Wallet](https://github.com/StackmateNetwork/the-stackmate).

## Table of Contents
- [Acknowledgements](#acknowledgements)
- [Overview](#overview)
- [Test](#test)
- [Build](#build)
- [Documentation](#docs)
- [Contributions](#contributions)
- [Community](#community)
- [Maintainers](#maintainers)
- [License](#license)

## Acknowledgements

Immense love to our friend and sponsor `Prashant Balani` for being patient and supportive throughout the 3 years of R&D that was required to make this project come to life!

Massive thanks to the [bdk](https://bitcoindevkit.org) & [cyphernode](http://cyphernode.io) teams for all the support and feedback which saved us a lot of time and improved the quality of our work.

## Overview

The entire ffi uses a string interface; defined in `src/lib.rs`

1. Inputs are converted into native rust types as the first sanitization step. 

2. Native types are then used in pure rust modules.

3. All native structs being returned `impl` a `c_stringify` method which converts the native struct into stringified JSON outputted as a CString.

## Test

`tests/test.sh`

Test individual units with printing.

`cargo test -- --nocapture <test_name>`

## Build

`resources/build.sh` currently only supports android builds. 

Binaries are zipped into `resources/builds.zip`.

## Documentation

[Docs.rs](https://docs.rs/stackmate/0.7.0/stackmate/)

This library expects the client to build a policy (string) by themselves - refer to http://bitcoin.sipa.be/miniscript/ for more info.

More documentation can be found in `resources/docs`.

## Contributions

We are looking for active contributions in the following areas:

- General code review

- IOS builds

- Taproot support 

- Neutrino support

- Lightning support

## Community

Join us on the Bitcoin-only India group where we are openly working on tools required for a Bitcoin standard in India.

Discord: https://discord.gg/PdRERkyNt4

## Maintainers

[Morteza](https://github.com/mocodesmo)

[Vishal](https://github.com/i5hi)

## License

[MIT](https://github.com/i5hi/stackmate-core/blob/main/LICENSE)
