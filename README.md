# eth_proof_beginner

MyToken contract

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
       
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    
    2. Your contract will have a mapping of addresses to balances (address => uint)
    
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
       
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
       
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here

    // mapping variable here

    // mint function

    // burn function

}

Contract Details Public variables: 

myToken: A string variable that stores the token name. 

myShort: A string variable that stores the token abbreviation. 

total: A uint variable that tracks the total supply of tokens. 

Mapping variable: balance: A mapping that associates addresses with their token balances. 

Mint function: The mint function takes two parameters: _add (address) and _val (uint). It increases the total supply (total) by the specified _val amount. It increases the balance of the specified address (_add) by the specified _val amount. 

Burn function: The burn function takes two parameters: _add (address) and _val (uint). It first checks if the balance of the specified address (_add) is greater than or equal to the specified _val. If the condition is met, it deducts the specified _val from the total supply (total) and from the balance of the specified address.

We have to complete the above function to deploy the transaction protol.


Executing program
To execute this Solidity contract (i.e., "MyToken"), you need to deploy it on the Ethereum network. Here's a step-by-step guide:

1. **Setting Up Your Development Environment**:
   - Install [Node.js](https://nodejs.org/en/download/).
   - Install Truffle using npm (Node Package Manager) by running:
     ```
     npm install -g truffle
     ```

2. **Starting a New Truffle Project**:
   - Create a new directory for your project.
   - Navigate to this directory using your terminal or command prompt and initiate a new Truffle project by running:
     ```
     truffle init
     ```

3. **Adding Your Contract**:
   - Within the newly created project directory, you'll find a `/contracts` folder. Copy and paste your "MyToken" contract into a new file, say `MyToken.sol`.

4. **Compiling the Contract**:
   - Navigate to your project directory in the terminal.
   - Compile the contract using:
     ```
     truffle compile
     ```

5. **Setting up Ganache (For Local Testing)**:
   - Install [Ganache](https://www.trufflesuite.com/ganache), which is a personal Ethereum blockchain useful for testing purposes.
   - Start Ganache.
   - Create a new workspace or just use the default settings.

6. **Migrate (Deploy) Your Contract**:
   - Edit `truffle-config.js` in your Truffle project directory. Under `networks`, add configuration for Ganache (usually the default configuration is fine).
   - Create a new file in the `/migrations` directory named `2_deploy_contract.js`. In this file, add:
     ```javascript
     const MyToken = artifacts.require("MyToken");

     module.exports = function(deployer) {
       deployer.deploy(MyToken);
     };
     ```
   - In your terminal, run:
     ```
     truffle migrate --network development
     ```

7. **Interact with Your Contract**:
   - Open the Truffle console:
     ```
     truffle console --network development
     ```
   - Interact with your deployed contract. Here's how you can mint some tokens:
     ```javascript
     let instance = await MyToken.deployed();
     await instance.mint("<Your_Ethereum_Address>", 1000); // Replace <Your_Ethereum_Address> with your address from Ganache.
     ```

8. **Deploying to the Main Ethereum Network**:
   - For deploying to the main network or any Ethereum testnets, you would typically use a service like [Infura](https://infura.io/) and a HD Wallet provider. This step is more involved and can incur costs, as you will have to pay gas fees.

9. **Final Notes**:
   - This simple token does not comply with the standard ERC20 interface. If you plan to make this token widely accepted or interact with other smart contracts/dapps, you'd want to use or extend a standard ERC20 interface.
   - Always test your contracts extensively on testnets before deploying to the main network.


Video Walkthrough

https://www.loom.com/share/1afe0fa95e9640abaff28b47a702666c?sid=b6695608-9d83-4777-917a-b989f0f88d1c
