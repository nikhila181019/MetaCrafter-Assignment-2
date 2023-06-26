# MetaCrafter-Assignment-2
Let's break down the code:

The contract is defined with the name "MyToken".
The SPDX-License-Identifier is set to MIT, indicating that the code is licensed under the MIT license.
The pragma directive specifies the version of the Solidity compiler to be used (0.8.18 in this case).
Next, the contract defines several components:

Public variables:

tokenName: A string variable that represents the name of the token (e.g., "META").
tokenAbbry: A string variable that represents the abbreviation of the token (e.g., "MTA").
totalSupply: An unsigned integer variable that represents the total supply of the token. It is initially set to 0.
Mapping variable:

balances: A mapping that associates addresses with their corresponding token balances. It maps an address to a uint value, representing the balance of tokens held by that address.
The contract then includes two functions:

mint function:

It takes two parameters: _address (the address to mint tokens to) and _value (the number of tokens to mint).
Inside the function, the totalSupply is increased by _value, effectively minting new tokens.
The balance of the _address is increased by _value as well, indicating that the _address now holds additional tokens.

burn function:

It takes two parameters: _address (the address to burn tokens from) and _value (the number of tokens to burn).
The function first checks if the balance of _address is greater than or equal to _value. If not, the burn operation is not executed to prevent burning more tokens than available.
If the balance check passes, the totalSupply is decreased by _value, effectively burning tokens.
The balance of the _address is also decreased by _value, reflecting the reduction of tokens held by the _address.
Overall, this contract allows for the creation (minting) and destruction (burning) of tokens by adjusting the totalSupply and individual balances stored in the balances mapping. The mint function increases the token supply and assigns tokens to a specified address, while the burn function decreases the token supply and reduces the balance of a specified address, provided the balance is sufficient to cover the burning amount.
