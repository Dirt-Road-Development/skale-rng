# SKALE RNG

## Installation

Add this repo to your application by running ```npm add @dirtroad/skale-rng```. This will make the **RNG** contract available to import into your other Solidity contracts
via ```import "@dirtroad/skale-rng/contracts/RNG.sol"```.

## Usage

When using this contract you can add it as an inherited contract to take advantage of all of the functions. Example:

```solidity
contract ExampleRNG is RNG {

    uin256 public amount;

    constructor() {
        amount = getRandomNumber();
    }

    function updateAmount() external {
        amount = getRandomNumber(); 
    }
} ```
