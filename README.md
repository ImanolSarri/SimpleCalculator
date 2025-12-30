# SimpleCalculator
📐 Calculator Smart Contract

A smart contract written in Solidity (v0.8.24) that implements a basic calculator with arithmetic operations, demonstrating the use of events, modifiers, and internal functions. This contract is intended mainly for educational and learning purposes.



📄 Overview

The Calculator smart contract allows users to perform simple mathematical operations such as:

➕ Addition

➖ Subtraction

✖️ Multiplication

It also showcases core Solidity concepts, including:

State variables

Modifiers

Events

Internal functions (internal)

Logical validation before function execution



⚙️ Technical Specifications

Language: Solidity

Version: 0.8.24

License: LGPL-3.0-only

pragma solidity 0.8.24;



🧮 State Variable
uint256 public result = 10;


Stores the current result of the calculator

Initialized with the value 10

Declared as public, so Solidity automatically generates a getter function



🧱 Modifiers
checkNumber
modifier checkNumber(uint256 num1_)


Validates that the provided number is exactly 10

Reverts the transaction if the condition is not met

Used as an example of pre-execution logic control



📢 Events
➕ Addition
event Addition(uint256 number1, uint256 number2, uint256 result);


Emitted when an addition operation is executed.

➖ Substraction
event Substraction(uint256 number1, uint256 number2, uint256 result);


Emitted when a subtraction operation is executed.



🧩 External Functions
➕ addition
function addition(uint256 num1_, uint256 num2_) public returns (uint256)


Adds two numbers

Returns the calculated result

Emits the Addition event

➖ substraction
function substraction(uint256 num1_, uint256 num2_) public returns (uint256)


Performs subtraction using an internal function

Returns the calculated result

Emits the Substraction event

✖️ multiplier
function multiplier(uint256 num1_) public


Multiplies the stored result by num1_

Updates the contract state

✖️ multiplier2
function multiplier2(uint256 num1_) public checkNumber(num1_)


Multiplies the result only if num1_ equals 10

Demonstrates practical usage of a modifier



🔒 Internal Functions
subtration_logic
function subtration_logic(uint256 num1_, uint256 num2_) internal pure returns (uint256)


Contains the subtraction logic

Declared as internal and pure

Can only be called from within the contract



🧪 Use Cases

Learning basic smart contract structure

Practicing modifiers and events

Educational example for Solidity courses

Foundation for more advanced contracts



🚀 Possible Improvements

Add descriptive revert messages

Fix naming inconsistencies (substraction → subtraction)

Emit events in all state-changing functions

Add unit tests (Hardhat / Foundry)

Optimize gas usage with custom errors



📜 License

This project is licensed under the LGPL-3.0-only license.



✍️ Author

Developed for educational purposes to learn Ethereum Smart Contract Development.
