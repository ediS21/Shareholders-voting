# Shareholders-voting

Small project in Solidity about Smart contracts. This project uses [remix.ethereum.org](https://remix.ethereum.org) to create a smart contract.

Remix default workspace is present when:
i. Remix loads for the very first time 
ii. A new workspace is created with 'Default' template
iii. There are no files existing in the File Explorer

This workspace contains 3 directories:

1. **'contracts'**: Holds three contracts. The use case is about a company director who creates questions and allows or forbids shareholders to vote and view the results of the voting process.
2. **'scripts'**: Contains four typescript files to deploy a contract. It is explained below.
3. **'tests'**: Contains Solidity and JS test files default contracts.

## CONTRACTS

There are 3 contracts:

### Director

The `Director` contract manages the director of the voting system, providing functionality for initializing the director, allowing the director to be changed, and retrieving the current director's address.

### Question Factory

The `QuestionFactory` contract extends the `Director` contract and handles the creation and management of voting questions and shareholders. It includes structures to represent shareholders and questions, events for new questions and question results, and maps to track relationships between shareholders and questions.

### Question Helper

The `QuestionHelper` contract inherits from the `QuestionFactory` contract and extends functionalities related to limiting shareholder rights, closing the voting process, and viewing results. It introduces additional modifiers and functions for the director to manage voting privileges and access to question results.

## SCRIPTS

The 'scripts' folder has four typescript files that help deploy the 'Storage' contract using 'web3.js' and 'ethers.js' libraries.

For the deployment of any other contract, just update the contract's name from 'Storage' to the desired contract and provide constructor arguments accordingly in the file `deploy_with_ethers.ts` or  `deploy_with_web3.ts`

## How to run

To run a script, right-click on the file name in the file explorer and click 'Run'. Just to remind you, the Solidity file must already be compiled.
Output from the script will appear in remix terminal.

Please note, require/import is supported in a limited manner for Remix-supported modules.
For now, modules supported by Remix are ethers, web3, swarmgw, chai, multihashes, remix and hardhat only for hardhat.ethers object/plugin.
An error like this will be thrown for unsupported modules: '<module_name> module require is not supported by Remix IDE' will be shown.
