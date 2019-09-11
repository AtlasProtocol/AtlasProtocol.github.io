# NRC20 Governance Web Tool
This is the repo that hold our [web tool](https://atlasprotocol.github.io/governance/#/) using Github Pages.

## How To Use

### Step 1 Deploy your contract
Here is the [template contract](https://github.com/AtlasProtocol/interactions/tree/develop/contracts/NAS/governance)

You can deploy using Nebulas web wallet or any other Nebulas wallet.

`init(chairs, executors, contract)`

Set initialization parameters

`chairs` Array of address in chairs group

`executors` Array of address in exec group

`contract` NRC20 token contract address

Here is a example of  parameters

`["[\"n1STxGuEZaneTtNiXoVLD8TdmSk48Erfvnd\",\"n1W9shcaD7pzqM4snNmNs2MQaTwjqsmyhCv\"]","[\"n1STxGuEZaneTtNiXoVLD8TdmSk48Erfvnd\"]","n1nkoSJVLQnaKnDKH56mtKtdjbgLKoHZhtD"]`

## Step 2 Fill information in contract tab in Web tool

Fill in with **contract address** you just deployed and set your **From address**(address hold by you).

That's all the setting steps.

## Contact
If you have any question about this tool, feel free to open issue. 