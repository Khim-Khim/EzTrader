# OSAKA METAHOURSE EXCHANGE CONTRACTS

> Áp dụng công nghệ blockchain vào trao đổi và mua bán

[![BAP SOFTWARE](https://bap-software.net/wp-content/uploads/2020/01/logo-bap-software-1.png)](https://bap-software.net/en/)


This project is using:

- [Hardhat](https://github.com/NomicFoundation/hardhat) cho việc deloy và testing.
- [We3.js](https://github.com/ChainSafe/web3.js) Cho việc tương tác với các contract và transaction.
- [Openzeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts) Cho các việc lập trình và update smart contract.


Check the corresponding docs for additional information and help.


💿 Install all dependencies:

```sh
npm install
```

# Spectre verification

To try out Spectre verification, you first need to deploy a contract to an Spectre network.

In this project, enter the private key of the account which will send the deployment transaction. With a valid .env file in place, first deploy your contract:

shell
npx hardhat run --network spectretestnet scripts/deploy/ExchangeMH.js

Then, flatten the contract file that has just been deployed following command :npx hardhat flatten contracts/Exchange1155.sol > Exchange1155Flatten.sol 

Then, copy the deployment address and find it in https://testnet.spectre-scan.io/. Verify contract and interact with this.


# Upgradeable contract
This contract use OpenZeppelin-Upgradeable to upgrade contract.

```sh
npx hardhat run --network spectretestnet scripts/deploy/Upgradeable_Exchange1155.js
```
Upgrade contract : copy proxy address and deploy contract version2 with proxy address following command:
```sh
npx hardhat run --network spectretestnet scripts/deploy/Upgradeable_Example_721.js
```



