PROJECT TITLE: SMART CONTRACT FOR MINTING AND BURNING TOKENS

DESCRIPTION: The project is a basic implementation of an Ethereum smart contract that creates a token named "DigitalLandToken" with the abbreviation "DLToken" and the symbol "DLT". This smart contract is written in Solidity and is designed to manage the minting and burning of these tokens.

PUBLIC VARIABLES

tokenName: Stores the name of the token.

tokenAbb: Stores the abbreviation of the token, set to "DLToken".

symbol: Stores the symbol of the token, set to "DLT".

totalSupply: Keeps track of the total number of tokens in circulation. Initially set to 0.

MAPPING balances: A mapping that associates addresses with their respective token balances. It uses an address as the key and a uint as the value to store the balance.

MINT FUNCTION The mintToken function is used to create new tokens and assign them to a specified address. It takes two parameters:

addr: The address to which the new tokens will be assigned.

val: The number of tokens to be created and added to the total supply.

BURN FUNCTION

The burnToken function is used to destroy tokens from a specified address, reducing both the total supply and the balance of the address. It also takes two parameters:

addr: The address from which the tokens will be burned.

val: The number of tokens to be burned.
