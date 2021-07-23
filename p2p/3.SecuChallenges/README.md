# Security Challenges with Solidity Smart Contracts

Ethereum is a blockchain protocol that introduced smart contracts into the blockchain world. Smart Contracts are contracts but written by a developer using the Solidity programming language. Once the smart contract has been written on the blockchain using a transaction it becomes immutable and cannot be further modified.

But as every IT program, Smart Contracts have flaws which can be use by hackers in order to hack a contract and change their behaviour.

## Table of content
* [Step 0 - Setup](./README.md#step-0---setup)
* [Step 1 - Easy level](./README.md#step-1---easy-level)
    * [Hello Ethernaut](./README.md#1.0-hello-ethernaut)
    * [Fallback](./README.md#1.1-fallback)
    * [Coin Flip](./README.md#1.2-coin-flip)
* [Step 2 - Medium Level](./README.md#step-2---medium-level)
    * [Gatekeeper One](./README.md#2.0-gatekeeper-one)
    * [Force](./README.md#2.1-force)
    * [Vault](./README.md#2.2-vault)
* [Step 3 - Hard level](./README.md#step-3---hard-level)
    * [The rewarder](./README.md#the-rewarder)
    * [Compromised](./README.md#compromised)
    * [Selfie](./README.md#selfie)
* [Going Further](./README.md#going-further)

## Step 0 - Setup

First, you have to download [MetaMask Plugin](https://metamask.io/download.html), and create an ethereum account.
Then, you can claim some Rinkeby faucet [here](https://www.rinkeby.io/#faucet).
You will use it to solve the following challenges, but it does not have a real value ; it is often use for testing purposes.

Finally, You can use the code editor of your choice, but we highly recommend using the online Remix Editor available [here](https://remix.ethereum.org/).
In the `Solidity compiler` tab :

* Set the compiler version to `0.8.5`
* Select the `auto-compile` checkbox.

In the `Deploy & run` transactions :

* The environment refers to the ethereum network you're using. JavaScript VM means that the code will execute on a local network
Injected Web3 will use metamask to connect to the real Ethereum network.

## Step 1 - Easy Level

In this category, you will learn the very basics of Ethereum Smart Contracts, Solidity syntax language and how to use you web3JS
console. To access it, open `Inspect Element` on your browser and click on the `Console` tab.

To understand the syntax of Solidity language, you can have some ressources [here](https://www.tutorialspoint.com/solidity/solidity_basic_syntax.htm).

### 1.0 [Hello Ethernaut](https://ethernaut.openzeppelin.com/level/0x4E73b858fD5D7A5fc1c3455061dE52a53F35d966)

The first challenge has the purpose to introduce you to the utils you're going to need to solve the challenges on ethernaut.

### 1.1 [Fallback](https://ropsten.ethernaut.openzeppelin.com/level/0xe2F72aa61fD6322C6c4d22227a594391E051F990)

This challenge introduce you to the fallback security breach, and learn good practices for your futures smart contracts!

### 1.2 [Coin Flip](https://ethernaut.openzeppelin.com/level/0x4dF32584890A0026e56f7535d0f2C6486753624f)

It's going to introduce you to the basic random number generator security breach.

## Step 2 - Medium Level

### 2.0 [Gatekeeper One](https://ethernaut.openzeppelin.com/level/0x9b261b23cE149422DE75907C6ac0C30cEc4e652A)

This challenge will introduce you to the gasleft function and the conversion between types.

### 2.1 [Force](https://ethernaut.openzeppelin.com/level/0x22699e6AdD7159C3C385bf4d7e1C647ddB3a99ea)

For this challenge, you're going to need a lot of perseverance and a it's going to help you understand a bit more the complex smart contracts.

### 2.2 [Vault](https://ethernaut.openzeppelin.com/level/0xf94b476063B6379A3c8b6C836efB8B3e10eDe188)

This challenge will introduce you to how the variables are stored in the etherum blockchain.

## Step 3 - Hard Level

Thoses challenges will help you understand how bigger contracts and flashloan works and how there might be an exploit in it.

### 3.0 [The rewarder](https://www.damnvulnerabledefi.xyz/challenges/5.html)

### 3.1 [Compromised](https://www.damnvulnerabledefi.xyz/challenges/6.html)

### 3.2 [Selfie](https://www.damnvulnerabledefi.xyz/challenges/7.html)

## Going Further

You can keep the websites given for the differents challenges and do some other ones !
