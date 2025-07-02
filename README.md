# web3-ui

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-40-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

_In Development - Refactoring in Progress 🏗️_

A library of UI components specifically crafted for web3 use cases.

| Package name                                                                                       | Current version                                                                                                      |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| [(Deprecated) `@web3-ui/core`](https://github.com/Developer-DAO/web3-ui/tree/main/packages/core)   | [![npm version](https://badge.fury.io/js/@web3-ui%2Fcore.svg)](https://badge.fury.io/js/@web3-ui%2Fcore)             |
| [`@web3-ui/components`](https://github.com/Developer-DAO/web3-ui/tree/main/packages/components)    | [![npm version](https://badge.fury.io/js/@web3-ui%2Fcomponents.svg)](https://badge.fury.io/js/@web3-ui%2Fcomponents) |
| [(Deprecated) `@web3-ui/hooks`](https://github.com/Developer-DAO/web3-ui/tree/main/packages/hooks) | [![npm version](https://badge.fury.io/js/@web3-ui%2Fhooks.svg)](https://badge.fury.io/js/@web3-ui%2Fhooks)           |

## Quick start

### Note: This is for the current public release. This library is being refactored and instructions will change.

1. Install the package

```bash
$ yarn add @web3-ui/core ethers
```

2. Setup the Provider

```tsx
import { Provider, NETWORKS } from '@web3-ui/core';

function MyApp({ Component, pageProps }) {
  return (
    <Provider network={NETWORKS.mainnet}>
      <Component {...pageProps} />
    </Provider>
  );
}
```

3. Use the components and hooks

```tsx
import { ConnectWallet, useWallet } from '@web3-ui/core';

function Home() {
  const { connection } = useWallet();

  return (
    <div>
      <ConnectWallet />
      <div>{connection.ens || connection.userAddress}</div>
    </div>
  );
}
```

## Roadmap

Please see the [Roadmap](/contributing/ROADMAP.md) for more details

## How to Contribute

Read the [CONTRIBUTING GUIDELINES](/CONTRIBUTING.md).

## The motive behind this package

- [RFC: web3-ui (a web3-specific UI library)](https://forum.developerdao.com/t/rfc-web3-ui-a-web3-specific-ui-library/565)
## Special thanks

This project would not have been possible without these wonderful projects:

- [ethers](https://github.com/ethers-io/ethers.js/)
- [scaffold-eth](https://github.com/scaffold-eth/scaffold-eth)
- [Chakra UI](https://github.com/chakra-ui/chakra-ui)
- [web3modal](https://github.com/web3modal/web3modal)
- [useDApp](https://github.com/EthWorks/useDapp)
- [wagmi](https://github.com/tmm/wagmi)
- [Storybook](https://github.com/storybookjs/storybook)
- [Preconstruct](https://github.com/preconstruct/preconstruct)
