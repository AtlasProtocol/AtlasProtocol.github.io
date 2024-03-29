# Multi-Signature NRC20 Governance (MSNGov) Web Tool
This repo holds the source code for Atlas Protocol's open source [Multi-Signature NRC20 governance web tool](https://atlasprotocol.github.io/governance/#/).

Atlas Protocol(ATP)'s MSNGov is a Multi-Signature governance tool for [NRC20 assets on Nebulas Blockchain](https://github.com/nebulasio/wiki/wiki/NRC20). Its unique governance structure allows users to assign different roles to multiple governers(e.g, board chairs, executives), so to archieve better flexibility in governance and better separation of responsibilities in business entities.

## How To Use Atlas Protocol NRC20 Governance Web Tool

### Step 1: Deploy your governance contract
Using the NRC20 governance [template contract](https://github.com/AtlasProtocol/interactions/tree/develop/contracts/NAS/governance)

You can deploy using [Nebulas web wallet](https://github.com/nebulasio/web-wallet) or any Nebulas SDK tooks API(http://wiki.nebulas.io/en/latest/dapp-development/tools.html).

### Step 2: Init governance contract
Once you collected all the governors NAS address and their administrative roles, you can initiate the deployed governance contract by calling its `init` function:

`init(chairs, execs, contract)`

In which, the initialization parameters are:

`chairs` Array of address in board chairs group

`execs` Array of address in executive group

`contract` The contract address of the NRC20 token to be governed 

Example:

`["[\"n1STxGuEZaneTtNiXoVLD8TdmSk48Erfvnd\",\"n1W9shcaD7pzqM4snNmNs2MQaTwjqsmyhCv\"]","[\"n1STxGuEZaneTtNiXoVLD8TdmSk48Erfvnd\"]","n1nkoSJVLQnaKnDKH56mtKtdjbgLKoHZhtD"]`

## Step 3: Transfer asset to the governance contract address
To enable the deploed contract as a asset governor, one need to first transfer the asset to be managed to the contract addres.
One can do that using an NRC20 transfer using an API contract call or NAS nano pro wallet or [any other wallet that support NRC20](https://nebulas.io/wallets.html)

**NOTE: Make sure ONLY transfer asset that associate with NRC20 contract you set in Step 2**
## Step 4: Filling information into Contract Tab

Filling in with **contract address** you just deployed and set your **From address**(address owned by you that can sign the transactions generated by this tool).

## Step 5: Sign generated transactions and broadcast to Nebulas mainnet
NRC20 governance tool supports 2 way of signing & broadcasting
* [Nebulas Chrome extension wallet](https://medium.com/nebulasio/creating-a-nas-wallet-9d01b5fa2df6)
* [NAS nano pro app] (https://nano.nebulas.io/)


## Contribution
If you have any question about this tool or interested in contributing, please feel free to open an issue. 

## Disclaimer
This open source tool (MSNGov) is created by Atlas Protocol as a proof-of-concept for on-chain asset governance. Atlas Protocol SHOULD NOT be hold responsible for any incident like lost of asset caused by ANYONE using this tool.
Users are free to use and modify it to suit their need. By using it, you acknowledge that this tool is still an early prototype and a decent amount of your own effort should be put in to assess and evalute this tool and you COULD NOT hold Atlas Protocol responsible for any misuse and lost of asset.
