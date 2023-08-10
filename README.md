# Error Handling Smart Contract

The `ErrorHandlingExample` smart contract is a basic example demonstrating the usage of `require()`, `assert()`, and `revert()` statements in Solidity. These statements help validate conditions, ensure internal consistency, and handle unexpected situations within a smart contract.

## Features

- **Increment Counter**: Increments the counter by a specified value, validating that the value is greater than 0 using `require()`.
- **Decrement Counter**: Decrements the counter by a specified value, validating that the value is greater than 0 and does not exceed the current counter value using `require()`. It also uses `revert()` to handle the case where the decrement value exceeds the counter value.
- **Get Counter Value**: Retrieves the current value of the counter.

## Getting Started

To interact with the `ErrorHandlingExample` smart contract, follow these steps:

1. Compile the Solidity code using a compatible compiler (Solidity version 0.8.0 or higher recommended).
2. Deploy the compiled contract to an Ethereum development environment or testnet.
3. Interact with the deployed contract using transactions or read-only calls to its functions.

## Functions

### `incrementCounter(uint256 _value)`

Increments the counter by a specified value.

- Parameters:
  - `_value`: Value to increment the counter by.

- Error Handling:
  - Uses `require()` to ensure `_value` is greater than 0.

### `decrementCounter(uint256 _value)`

Decrements the counter by a specified value.

- Parameters:
  - `_value`: Value to decrement the counter by.

- Error Handling:
  - Uses `require()` to ensure `_value` is greater than 0 and doesn't exceed the counter value.
  - Uses `revert()` to explicitly revert if `_value` exceeds the counter value.

### `getCounter()`

Retrieves the current value of the counter.

- Returns:
  - The current value of the counter.

## Usage Examples

```solidity
// Deploy the ErrorHandlingExample contract
ErrorHandlingExample contractInstance = new ErrorHandlingExample();

// Increment the counter
contractInstance.incrementCounter(5);

// Decrement the counter
contractInstance.decrementCounter(3);

// Retrieve the counter value
uint256 currentValue = contractInstance.getCounter(); // Should return 2
```

## Error Handling

- `require()`: Validates conditions before proceeding with the function execution.
- `assert()`: Checks for internal errors and ensures certain conditions should never fail.
- `revert()`: Explicitly reverts a transaction with a custom error message.

I find the above code true to my knowledge and it is working smoothly in the remix environment
