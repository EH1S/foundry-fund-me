## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

- **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
- **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
- **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
- **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/


# Foundry Fund Me 🏦

A Solidity smart contract project built with Foundry that allows users to fund ETH and only the contract owner to withdraw — complete with tests, scripts, and mocks.

---

## 📦 Features

- `FundMe` contract:  
  - Users can fund with ETH  
  - Requires a minimum USD-equivalent amount (via Chainlink price feed)  
  - Only owner can withdraw funds  
  - Includes a more gas-efficient `cheaperWithdraw` variant  

- **Testing** with Forge:  
  - Mock price feed (MockV3Aggregator)  
  - Tests covering funding, withdrawals, edge cases (insufficient funds, multiple funders)  

- **Deployment script**  
  - `DeployFundMe.s.sol` uses `HelperConfig` for network-specific price feed addresses  
  - Supports local/forked/testing & live networks  

- **Formatting / linting / CI**  
  - `forge fmt` enforced in GitHub Actions  
  - Code style consistency  

---

## 🧪 Setup & Usage

### 1. Clone

```bash
git clone https://github.com/EH1S/foundry-fund-me.git
cd foundry-fund-me


## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
