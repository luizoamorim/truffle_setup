# Project goals

## Identify ways that Truffle can improve the smart contract creation and deployment process.
With truffle you don't need more to make all the manual process that is:
- Compile the solidity code with remix.
- Deploy the smart contract.
- Take the ABI.
- And access tha blockchain by web3.

Truffle automate this tasks for you. With few commands you can do all this.

## Install truffle to your local environment.
- First you need to have node.js installed in your local machine.
- Then run:
```
npm install truffle -g
```

It's all.

## Set up a truffle environment and deploy your first contract.
- To start your truffle project, create a folder and then run:
```
truffle init
```
It will create the environment for you.

### Project structure

#### Contracts
Is generated a folder called contracts that create a sample solidity
smart contract.
Is here that you'll develop your smart contracts.

##### Migrations
It's responsible to migrating the smart contract. Migrating in this case is
like when you copy the ABI on Remix.
When you migrate your contract, you'll see a new file come up that includes
the ABI for you withot you needing to copy and paste it every time.

#### Configuration files
The config file is where you config the network connections.

Look at this page to have more informations:
trufflesuite.com/docs/advanced/configuration