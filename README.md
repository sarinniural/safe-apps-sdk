# Safe Apps Developer Tools Monorepo

[![Logo](https://raw.githubusercontent.com/gnosis/safe-apps-sdk/master/assets/logo.png)](https://gnosis-safe.io/)

Developer tools to integrate third-party applications (Safe Apps) with Safe (https://gnosis-safe.io/app/).

You can find more resources on Safe Apps in the [Gnosis Safe Developer Portal](https://docs.gnosis-safe.io/build/sdks/safe-apps).

![safeapps_pathways_v4](https://user-images.githubusercontent.com/6764315/123075714-c5564100-d418-11eb-8da0-898aa163dee2.png)

## Packages

| Package                                                       | Description                                                                                                            |
|---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [cra-template-safe-app](/packages/cra-template-safe-app)      | CRA template to quickly bootstrap a Safe app                                                                           |
| [safe-apps-react-sdk](/packages/safe-apps-react-sdk)          | A wrapper of safe-apps-sdk with helpful React Hooks                                                                    |
| [safe-apps-sdk](/packages/safe-apps-sdk)                      | JavaScript SDK                                                                                                         |
| [safe-apps-provider](/packages/safe-apps-provider)            | A generic provider that can be used with common web3 libraries (e.g. web3.js or Ethers)                                |
| [safe-apps-onboard](https://docs.blocknative.com/onboard)     | Blocknative included Safe App support in onboard.js v1.26.0. To use it, add `{ walletName: "gnosis" }` to wallet list. |
| [safe-apps-web3modal](/packages/safe-apps-web3modal)          | A wrapper around Web3Modal that would automatically connect to the Safe if the app is loaded as a Safe app             |
| [safe-apps-web3-react](https://github.com/Uniswap/web3-react) | A web3-react connector for Safe is included in web3-react starting from version 8                                      |
| [safe-apps-wagmi](/packages/safe-apps-wagmi)                  | A wagmi connector for Safe Apps                                                                                        |

## Testing your Safe App

You can directly use [our production interface](https://gnosis-safe.io/app) for testing your Safe App

We also made a very simple interface for testing safe apps that can be used on any network: https://dev.gnosis-safe.io/

## Setting up development environment

### Installing dependencies

```
npm i -g lerna
yarn global add lerna

lerna bootstrap
```

### Running commands

We will use `build` command as an example. Same applies to other commands.

For all packages:

```
lerna run build
```

For a specific package:

```
lerna run --scope @gnosis.pm/safe-apps-sdk build --stream
```

`--stream` options enables command output. By default, lerna displays it only in case of an error.

## Release process

Release process is described in [releases.md](/docs/releases.md)

## Useful links

- [Making an app to withdraw all assets from a Safe in one transaction - tutorial](/guides/drain-safe-app)
- [Start a new project using the Safe App React template](/packages/cra-template-safe-app)
- [Video introduction to Building with Safe Apps SDK & Contract Proxy Kit](https://www.youtube.com/watch?v=YGw8WfBw5OI)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
