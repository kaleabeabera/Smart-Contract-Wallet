# Smart Contract Wallet

This is a Solidity-based smart contract wallet that provides a secure and flexible solution for managing funds on the Ethereum blockchain. The wallet includes the following key features:

1. ## Single Owner
   The wallet has one owner.

2. ## Universal Fund Reception
   The wallet should be able to receive funds, no matter what the source is. It can receive funds from both Externally Owned Accounts (EOAs) and Contract Addresses.

3. ## Permissioned Spending
   The owner of the wallet can spend funds on any kind of address, whether it's an Externally Owned Account (EOA) with a private key or a Contract Address. The owner can also grant certain people the ability to spend up to a certain amount of funds.

4. ## Guardian Recovery
   In case funds are lost, the owner can be set to a different address by a minimum of 3 out of 5 guardians. This recovery process ensures that the funds can still be managed.

## Getting Started

To use this smart contract wallet, follow the steps below:

1. Clone the repository to your local machine.

2. Install the required dependencies and Solidity compiler.

3. Compile the `SmartContractWallet.sol` file using the Solidity compiler.

4. Deploy the compiled smart contract to the Ethereum network of your choice.

5. Interact with the deployed smart contract using the provided functions and modifiers to manage the wallet's funds.

## Functionality and Usage

The smart contract wallet offers the following functions:

- `setGuardian`: Allows the owner to assign or revoke guardian status for specific addresses. Guardians have the power to propose a new owner in case of lost funds.

- `proposeNewOwner`: Guardians can propose a new owner address and initiate a recovery process when the owner's access is lost. A minimum confirmation threshold from the guardians is required to change the owner.

- `setAllowance`: Only the owner can set the spending allowance for specific addresses. This function enables granting or revoking permissioned spending rights.

- `transfer`: The owner can initiate a transfer of funds to a target address, along with an optional payload for interaction with other smart contracts. The transfer amount must not exceed the available allowance for the owner.

The smart contract wallet also includes a fallback function (`receive`) that allows the wallet to receive funds.

## Contributing

Contributions to this project are welcome. If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request on GitHub.

## Acknowledgements

Special thanks to the Ethereum Blockchain Developer Bootcamp With Solidity (2023) course on UDEMY for teaching me solidty development.

