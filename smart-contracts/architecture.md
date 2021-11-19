---
description: >-
  This section describes provides a high-level overview regarding the technical
  implementation of Help Protocol.
coverY: 0
---

# Architecture

## Smart Contracts

The source code for Help smart contracts can be found on** **[**GitHub**](https://github.com/Help-Protocol/help-pcontracts).

| Contract     | Function                                                                           |
| ------------ | ---------------------------------------------------------------------------------- |
| Help Factory | Central directory that organizes the various component contracts of Help Protocol. |
| Gov          | Allows other Help contracts to be controlled by decentralized governance.          |
| Lock         | Responsible for locking up UST.                                                    |



The Pledge Token ($KARMA) is a Terraswap CW20 Token instance that is created during the initial bootstrapping of the protocol and is registered with the Help Protocol core contracts.

When new hAssets are whitelisted, Help Protocol will create the following contract instances:

* Terraswap CW20 Token for the new hAsset
* Terraswap Pair for the new hAsset against UST
* Terraswap CW20 Token for the new hAsset's LP Token
* Terraswap CW20 Token for the new hAsset's sLP Token
