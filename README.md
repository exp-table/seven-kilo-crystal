<img align="right" width="150" height="150" top="100" src="./public/readme.png">

# SevenKiloCrystal • [![tests](https://github.com/exp-table/seven-kilo-crystal/actions/workflows/ci.yml/badge.svg?label=tests)](https://github.com/exp-table/seven-kilo-crystal/actions/workflows/ci.yml) ![license](https://img.shields.io/github/license/refcell/femplate?label=license) ![solidity](https://img.shields.io/badge/solidity-^0.8.17-lightgrey)

An **not very efficient** data packing library.

## What is Seven Kilo Crystal?

SKC is a library that is an alternative to `abi.encode` and `abi.encodePacked` that can result in smaller `bytes`.
It is **NOT** optimized and consumes more gas than the two options above.

It serves as educational material.

**Warning**

It should be noted that unpacking the crystal (payload) produces an array whose elements order is in reverse w.r.t the elements that were added.

## Installation

To install with [**Foundry**](https://github.com/gakonst/foundry):

```sh
forge install exp-table/seven-kilo-crystal
```

## Usage

```js
bytes memory crystal = SevenKiloCrystal.cook();
crystal = SevenKiloCrystal.addition(crystal, uint(100));
crystal = SevenKiloCrystal.addition(crystal, uint(2**256 - 1));
uint256[] memory smoked = SevenKiloCrystal.smoke(crystal);
```

### Notable Mentions

- [femplate](https://github.com/refcell/femplate)
- [foundry](https://github.com/foundry-rs/foundry)
- [solady](https://github.com/vectorized/solady)
- [forge-std](https://github.com/brockelmore/forge-std)
- [forge-template](https://github.com/foundry-rs/forge-template)
- [foundry-toolchain](https://github.com/foundry-rs/foundry-toolchain)

### Disclaimer

_These smart contracts are being provided as is. No guarantee, representation or warranty is being made, express or implied, as to the safety or correctness of the user interface or the smart contracts. They have not been audited and as such there can be no assurance they will work as intended, and users may experience delays, failures, errors, omissions, loss of transmitted information or loss of funds. The creators are not liable for any of the foregoing. Users should proceed with caution and use at their own risk._

See [LICENSE](./LICENSE) for more details.
