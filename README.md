# Smart contracts tools
![image](https://user-images.githubusercontent.com/73957838/113349971-3224d800-930f-11eb-9c3b-ff616e12294c.png)

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

##### Configuration files
The config file is where you config the network connections.

Look at this page to have more informations:
trufflesuite.com/docs/advanced/configuration

## Truffle commands
```
Truffle v5.3.0 - a development framework for Ethereum

Usage: truffle <command> [options]

Commands:
  build     Execute build pipeline (if configuration present)
  compile   Compile contract source files
  config    Set user-level configuration options
  console   Run a console with contract abstractions and commands available
  create    Helper to create new contracts, migrations and tests
  db        Database interface commands
  debug     Interactively debug any transaction on the blockchain
  deploy    (alias for migrate)
  develop   Open a console with a local development blockchain
  exec      Execute a JS module within this Truffle environment
  help      List all commands or provide information about a specific command
  init      Initialize new and empty Ethereum project
  install   Install a package from the Ethereum Package Registry
  migrate   Run migrations to deploy contracts
  networks  Show addresses for deployed contracts on each network
  obtain    Fetch and cache a specified compiler
  opcode    Print the compiled opcodes for a given contract
  preserve  Save data to decentralized storage platforms like IPFS and Filecoin
  publish   Publish a package to the Ethereum Package Registry
  run       Run a third-party command
  test      Run JavaScript and Solidity tests
  unbox     Download a Truffle Box, a pre-built Truffle project
  version   Show version number and exit
  watch     Watch filesystem for changes and rebuild the project automatically

See more at http://trufflesuite.com/docs
```

## Comand sequence

### 1. Console
```
truffle console
```
It'll open the console of truffle to you execute the commands.

### 2. Execute command compile
```
compile
```
Here the contract is converted to bytecode to be execute by EVM.
The ABI is generated for another accounts that want use it too.

### 3. Migrate
```
migrate
```
It will deploy the contract on the blockchain network.

```
truffle(development)> migrate

Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.



Starting migrations...
======================
> Network name:    'development'
> Network id:      5777
> Block gas limit: 6721975 (0x6691b7)


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0x71c308d55b25978f5a6de357db730ed27cb9745cd600cb42cac921c6354da813
   > Blocks: 0            Seconds: 0
   > contract address:    0x539fa7f5fD2E5258E1521C074C783b2cF52Ed885
   > block number:        13
   > block timestamp:     1617310001
   > account:             0xb2f1E4EC91f22527B178dBf633b2D5f54e83E167
   > balance:             99.99616114
   > gas used:            191943 (0x2edc7)
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00383886 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00383886 ETH


Summary
=======
> Total deployments:   1
> Final cost:          0.00383886 ETH


- Blocks: 0            Seconds: 0
- Saving migration to chain.
```
