
# Create a Token:

A straight forward "Token Creation" application written in Solidity, that shows off the language's fundamental syntax and features. This program's goal is to provide those who are unfamiliar with Solidity a place to start so they can acquire a sense of how it operates.



## Description

The Solidity programming language, which is used to create smart contracts on the Ethereum blockchain, was used to create this straightforward contract. "MyToken" is returned by the contract's function. As a stepping stone for future, more complicated projects, this software provides a clear and basic introduction to Solidity programming. And this contract executes the funtionality such as minting the token and burning the token.

## Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., NewContract.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
   string public name="SOLIDITY";
   string public abbrv="SOLID";
   uint public totalSupply = 0;

    // mapping variable here
   mapping(address => uint) public balances;

    // mint function
   function mint (address _address, uint _value) public{
      totalSupply += _value;
      balances[_address] += _value;
   }
    // burn function
   function burn (address _address, uint _value) public{
      if(balances[_address] >= _value){
         totalSupply -= _value;
         balances[_address] -= _value;
      }
   }
}

Select the "Solidity Compiler" tab from the sidebar on the left to begin compiling the code. Click the "Compile NewContract.sol" button after ensuring that the "Compiler" option is set to "0.8.18" (or another suitable version).

You may deploy the contract by selecting the "Deploy & Run Transactions" button from the left-hand sidebar once the code has been built. After choosing the "NewContract" contract from the drop-down menu, press the "Deploy" button.

Make use of the MyToken method to communicate with the contract after it has been deployed. The "MyToken" function may be accessed by clicking on the "NewContract" contract located in the left sidebar. To run the function and get the minting and burning the token transaction, click the "transact" button at the end.

## Authors
-https://twitter.com/metacraftersio

Metacrafter Chris
## License

This project is licensed under the MIT License 
