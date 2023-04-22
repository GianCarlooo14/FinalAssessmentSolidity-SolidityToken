# FinalAssessmentSolidity-NFTMetacrafters

This is a Solidity program where a simple implementation of a token contract called NFTMetacrafters. The purpose of this contract is to allow us to create new tokens, which can be minted and burned as needed.

## Description

This Solidity contract is a basic implementation of a token contract called NFTMetacrafters. It allows the creation and destruction of tokens through the mint and burn functions. The contract can be used as a starting point for creating and managing tokens on the Ethereum blockchain.

## Getting Started

### Installing

* How/where to download your program
* Any modifications needed to be made to files/folders

### Executing program

* How to run the program
* Step-by-step bullets
```Solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract NFTMetacrafters {


    string public tokenName = "GianCarlooo";
    string public tokenAbbrv = "GC";
    uint public totalSupply = 0; 

    mapping(address => uint) public balances;

    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}


```

## Authors

Gian Carlo R. Dumana

BSIT 2.5

8213650@ntc.edu.ph

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
