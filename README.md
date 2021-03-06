# Supply chain & data auditing

This repository containts an Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

The DApp User Interface when running should look like...

![truffle test](images/ftc_product_overview.png)

![truffle test](images/ftc_farm_details.png)

![truffle test](images/ftc_product_details.png)

![truffle test](images/ftc_transaction_history.png)


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Please make sure you've already installed ganache-cli, Truffle and enabled MetaMask extension in your browser.

### Installing

A step by step series of examples that tell you have to get a development env running

Clone this repository:

```
git clone https://github.com/kaushal9678/Ethereum_coffee_SupplyChain_DAPP.git
```

Change directory to ```app``` folder and install all requisite npm packages (as listed in ```package.json```):

```
cd app
npm install
```

Launch Ganache:

```
ganache-cli -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

Your terminal should look something like this:

![truffle test](images/ganache-cli.png)

In a separate terminal window, Compile smart contracts:

```
truffle compile
```

Your terminal should look something like this:

![truffle test](images/truffle_compile.png)

This will create the smart contract artifacts in folder ```build\contracts```.

Migrate smart contracts to the locally running blockchain, ganache-cli:

```
truffle migrate
```

Your terminal should look something like this:

![truffle test](images/truffle_migrate.png)

Test smart contracts:

```
truffle test
```

All 10 tests should pass.

![truffle test](images/truffle_test.png)

In a separate terminal window, launch the DApp:

```
npm run dev
```

When you want to deploy your app to Rinkeby, you need to create a project in `Infura`. 
[Infura](https://infura.io/project/)
> After creating project use `infuraKey` of newly created project.

> For mnemonic go to `Metamask` settings and in `advanced` option click on `Reveal seeds`.

## Deploy to Rinkeby Network
use following command

```
truffle migrate --reset --network rinkeby

```
Above command returns following output


![truffle test](images/rinkeby_migrate.png)

##  Final output after deploying supplychain solution to Rinkeby network
![truffle test](images/rinkeby_final.png)

* While doing transaction on Rinkeby network following are the MetaMask history

![truffle test](images/metamask_transaction_history1.png)
![truffle test](images/metamask_transaction_history2.png)

**Below image is the transaction on EtherScan for following transaction hash**
``` 0xb55b1c36bd5c1ce9f8fc9700c6b9ea1e57c4b7bf5eb782f69ad95ae10ad80e95 ```

![truffle test](images/etherscan.png)



## Built With

* [Ethereum](https://www.ethereum.org/) - Ethereum is a decentralized platform that runs smart contracts
* [IPFS](https://ipfs.io/) - IPFS is the Distributed Web | A peer-to-peer hypermedia protocol
to make the web faster, safer, and more open.
* [Truffle Framework](http://truffleframework.com/) - Truffle is the most popular development framework for Ethereum with a mission to make your life a whole lot easier.



## Acknowledgments

* Solidity
* Ganache-cli
* Truffle
* IPFS
