PROJECT TITLE
Token Contract with Minting and Burning Functions

Description
This project implements a basic Ethereum smart contract for a token named "Manan" with the abbreviation "Mn". The contract includes functionalities for minting and burning tokens. It maintains a public variable to store the total supply of tokens and uses a mapping to track token balances for each address. The mint function allows the creation of new tokens by increasing the total supply and adding tokens to a specified address. The burn function reduces the total supply and decreases the token balance of a specified address, ensuring the address has sufficient tokens to burn.

Getting Started
Installing


Clone the repository from GitHub:
git clone 



Executing program:


* Navigate to the directory containing the smart contract file.
* Compile the smart contract using your preferred Solidity compiler (Using Remix IDE).
* Deploy the contract:
You can use Remix IDE or another Ethereum development environment.
Load MananToken.sol file, compile, and deploy the contract using a JavaScript VM or connect to your Ethereum node.
Use the deployed contract instance to call functions such as Mint and Burn.
Code block for mint :
function mint (address _address, uint _value)public{
        totalCount += _value;
        balances[_address] += _value;
    }
Code block for burn:
 function burn (address _address, uint _value)public{
        if (balances[_address] >= _value){
        totalCount -= _value;
        balances[_address] -= _value;
    }





HELP:
If you encounter any issues, ensure that:

You have the correct version of the Solidity compiler.
Your Ethereum client (like Ganache) is running and properly configured.
You are connected to the correct network (local, testnet, or mainnet).
For common problems or issues, refer to the Solidity and Ethereum documentation, or check community forums.


Authors
Manan panwar - Contact: manancoder12213@gmail.com
License
This project is licensed under the MIT License - see the LICENSE.md file for details.



