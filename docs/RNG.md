# Solidity API

## RNG

_A contract to generate random numbers using the SKALE Network RNG endpoint.
The RNG endpoint code for the function getRandomBytes() is taken from the SKALE Network Documentation:
https://docs.skale.network/tools/skale-specific/random-number-generator_

### getRandomBytes

```solidity
function getRandomBytes() public view returns (bytes32 addr)
```

Fetches 32 random bytes from the SKALE Network RNG endpoint.

_The assembly code retrieves random bytes from the SKALE Network.
For more details on how it works, refer to the SKALE Network documentation:
https://docs.skale.network/tools/skale-specific/random-number-generator_

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| addr | bytes32 | A 32-byte random value. |

### getRandomNumber

```solidity
function getRandomNumber() public view returns (uint256)
```

Generates a random number.

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | A random number as a uint256. |

### getNextRandomNumber

```solidity
function getNextRandomNumber(uint256 nextIndex) public view returns (uint256)
```

Generates a random number with an additional index iteration. 
This should be used for multiple values in the same block.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nextIndex | uint256 | The index to iterate the RNG value by. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | A random number as a uint256. |

### getNextRandomRange

```solidity
function getNextRandomRange(uint256 nextIndex, uint256 max) public view returns (uint256)
```

Generates a random number within a specified range with an additional index iteration.
This should be used for multiple values in the same block.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| nextIndex | uint256 | The index to iterate the RNG value by. |
| max | uint256 | The maximum value (inclusive) that the random number can be. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | A random number between 0 and max (inclusive). |

### getRandomRange

```solidity
function getRandomRange(uint256 max) public view returns (uint256)
```

Generates a random number within a specified range.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| max | uint256 | The maximum value (inclusive) that the random number can be. |

#### Return Values

| Name | Type | Description |
| ---- | ---- | ----------- |
| [0] | uint256 | A random number between 0 and max (inclusive). |

