# eth_proof_beginner

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

Contract Details Public variables: myToken: A string variable that stores the token name. myShort: A string variable that stores the token abbreviation. total: A uint variable that tracks the total supply of tokens. Mapping variable: balance: A mapping that associates addresses with their token balances. Mint function: The mint function takes two parameters: _add (address) and _val (uint). It increases the total supply (total) by the specified _val amount. It increases the balance of the specified address (_add) by the specified _val amount. Burn function: The burn function takes two parameters: _add (address) and _val (uint). It first checks if the balance of the specified address (_add) is greater than or equal to the specified _val. If the condition is met, it deducts the specified _val from the total supply (total) and from the balance of the specified address.
We have to complete the above function to deploy the transaction protol.

Video Walkthrough

https://www.loom.com/share/67eb147374c84bcf94ae9e99a1717a68
