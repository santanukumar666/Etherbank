# Etherbank
Developed a DeFi application for users to deposit and withdrawn Ethereum coins. Depositing Ethereum yields an additional gain of an ERC20 token with an APY of 10%.

* Deposit must be higher than 0.1 ETH.
* An address is only allowed to have a deposit active at the time. 
### Stack

* React.js – Frontend framework.
* Ganache – Runs local blockchain on Node.js environment.
* Truffle – Enables communication with blockchain for deployment and smart contract tests.
* Mocha/Chi – Test suite for smart contract testing on deployment.
* Web3 – Enables communication with local/remote Ethereum nodes 
## Compile and Migrate Smart Contracts

First, make sure you are running a local ERC20 blockchain, for example [Ganache](https://www.trufflesuite.com/ganache).
Verify that the _development_ network configured in __truffle-config.js__ matches your params, else modify them. 
Then, just execute _truffle_ commands:

```bash
cd truffle/
truffle compile
truffle migrate
```

## Run Truffle Tests

```bash
truffle test
```

## Launch Frontend Application

Go back to the root of the proyect, if not already there, and run:

```bash
cd ..
npm start
```

Visit http://localhost:3000

## Connect Metamask to one of the Ganache Accounts

- Make sure you are running Ganache. Then pick the first account and copy its private key.
- Go to http://localhost:4200
- On Metamask, add a new Network, with the URL http://localhost, appropriate as port and chain ID. Use this network for development.
- Also in Metamask import an account -> specify the private key you copied from the Ganache first account. __Warning__: do not use this account as a real account.
- Reload the webapp. 
