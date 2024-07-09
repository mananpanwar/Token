# Token Contract with Minting and Burning Functions

## Description
This project implements a basic Ethereum smart contract written in Solidity (which is a programming language used to create smart contracts on the Ethereum blockchain) for a token named "Manan" with the abbreviation "Mn". The contract includes functionalities for minting and burning tokens. It maintains a public variable to store the total supply of tokens and uses a mapping to track token balances for each address. The mint function allows the creation of new tokens by increasing the total supply and adding tokens to a specified address. The burn function reduces the total supply and decreases the token balance of a specified address, ensuring the address has sufficient tokens to burn.

## Getting Started
Installing


Clone the repository from GitHub:
git clone https://github.com/mananpanwar/Token



### Executing program:
 
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Mytoken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.4;

contract MyToken {
    string public tokenName = "Manan";
    string public tokenAbbrv ="Mn";
    uint public totalCount = 0;

    mapping(address => uint)public balances;

    function mint (address _address, uint _value)public{
        totalCount += _value;
        balances[_address] += _value;
    }

     function burn (address _address, uint _value)public{
        if (balances[_address] >= _value){
        totalCount -= _value;
        balances[_address] -= _value;
    }
    }
}

```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by using the "Mint" and "Burn" functions.We need to pass address for that provided by REMIX by copying it from "ACCOUNT" box and then click on the "Mint" and "Burn" functions (according to your choice) and paste the  copied address and enter value according to your choice.
 Finally, click on the "transact" button to execute the function and retrieve the value of "TotalCount" and check balance


## HELP:
If you encounter any issues, ensure that:

You have the correct version of the Solidity compiler.
Your Ethereum client (like Ganache) is running and properly configured.
You are connected to the correct network (local, testnet, or mainnet).
For common problems or issues, refer to the Solidity and Ethereum documentation, or check community forums.


## Authors
Manan panwar - Contact: manancoder12213@gmail.com


## License
This project is licensed under the MIT License - see the LICENSE.md file for details.



