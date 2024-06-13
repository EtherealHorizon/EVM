
# Metacrafter EVM assessment

This is the assessment for Ethereum EVM beginners course.
The purpose of this assessment is to check basic understanding of Solidity programming.


## Getting started

This program is written in solidity. It is a contract that has variables that store token and their balance. Mint function is used to generate tokens and burn function is used to spend them.
To run this program, we use Remix editor, which is an online tool for Solidity.
## Code

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;


contract MyToken {

    // public variables here
    string public TokenName = "Corgi";
    string public TokenAbrv = "CRG";
    uint public TotalSupply = 0;
    
    // mapping variable here

    mapping(address => uint ) public balances;

    // mint function

    function Mint(address _address, uint _value)public {
        TotalSupply += _value;
        balances[_address] += _value;
    }
    
    // burn function

    function Burn(address _address, uint _value)public {
        if(balances[_address] >= _value){
        TotalSupply -= _value;
        balances[_address] -= _value;
    }
    }
}



## Execution

To compile this code, click Win+S and then deploy the contract by clicking on the Ethereum Symbol on the left hand side of the menu.
## Authors

- [@rishupatel](https://www.github.com/EtheralHorizon)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details

[MIT](https://choosealicense.com/licenses/mit/)

