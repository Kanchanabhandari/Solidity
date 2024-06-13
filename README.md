# Custom Token (MyCustomToken)

  This project implements a basic ERC20-like token contract on the Ethereum blockchain. It allows for minting (creating) and burning (destroying) tokens, as well as checking balances of token holders.

# Description

  The Custom Token project aims to create a simple token contract using Solidity. It provides functionalities for minting new tokens and burning existing tokens based on specific conditions. This contract can serve as a foundation for building more complex token ecosystems or decentralized applications (dApps) on Ethereum.

# Getting Started

# Executing program

 First to open any Browser and to open Remix IDE, it's an online Solidity Platform. link - https://remix.ethereum.org/.

 then create a new file and file extension is .sol and save it. then copy and paste the code into the file:

// SPDX-License-Identifier: MIT pragma solidity 0.8.18;

contract CustomToken {

    // public variables here
    string public tokenName = "MyCustomToken";
    string public tokenSymbol = "MCT";
    uint public totalSupply = 0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public 
    {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public 
    {
        if (balances[_address] >= _value)
        {
          totalSupply -= _value;
          balances[_address] -= _value;
          }
    }
}

# Authors

  Kanchana Bhandari

# License

 This project is licensed under the [NAME HERE]MIT License - see the LICENSE.md file for details.
