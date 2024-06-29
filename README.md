# ErrorHandling Smart Contract

This project demonstrates the use of `require()`, `assert()`, and `revert()` statements in a Solidity smart contract.

## Contract Overview

The `ErrorHandling` contract includes the following functionality:

- **Deposit Ether:** Allows any user to deposit Ether into the contract.
- **Withdraw Ether:** Allows only the contract owner to withdraw Ether from the contract.
- **Assert Example:** Demonstrates the use of the `assert()` statement.
- **Revert Example:** Demonstrates the use of the `revert()` statement.
- **Get Balance:** Returns the current balance of the contract.

## Functions

### `constructor()`

Sets the initial owner of the contract to the address that deploys the contract and initializes the balance to zero.

### `deposit()`

Allows users to deposit Ether into the contract. The `require()` statement ensures that the deposit amount is greater than zero.

### `withdraw(uint256 amount)`

Allows the owner to withdraw a specified amount of Ether from the contract. The `require()` statements ensure that the caller is the owner and that the contract has sufficient balance for the withdrawal.

### `assertExample()`

Demonstrates the use of the `assert()` statement by checking that the contract's balance is never negative.

### `revertExample()`

Demonstrates the use of the `revert()` statement by always reverting with a custom error message.

### `getBalance()`

Returns the current balance of the contract.

## Modifiers

### `onlyOwner`

A modifier that restricts the execution of certain functions to the contract owner. It uses a `require()` statement to check if the caller is the owner.

## Deployment

To deploy this contract, use a Solidity-compatible development environment such as Remix, Truffle, or Hardhat. Make sure to have a wallet with enough Ether for gas fees.

## Usage

1. **Deploy the Contract:** Deploy the contract to the Ethereum network.
2. **Deposit Ether:** Call the `deposit()` function with a value greater than zero to deposit Ether into the contract.
3. **Withdraw Ether:** Call the `withdraw()` function with the desired amount to withdraw Ether (only by the owner).
4. **Assert Example:** Call the `assertExample()` function to check the balance assertion.
5. **Revert Example:** Call the `revertExample()` function to see the revert in action.
6. **Get Balance:** Call the `getBalance()` function to view the current contract balance.

## License

This project is licensed under the MIT License.
