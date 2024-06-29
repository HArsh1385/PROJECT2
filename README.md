# Token Creation

This is a Solidity Project "Token Creation" program.

## Description

The TokenCreation project creates a token that may be burned and minted. Users can mint new tokens to a specific address to increase the Total supply of the "Skull" token (SKL)," or burn existing tokens from that address to reduce the total supply.

## Getting Started

### Executing program

To run the program use Remix IDE, an Online Platform https://remix.ethereum.org/.

Once you are on the Remix website, create a new file and save the file with a .sol extension (like TokenCreation.sol). Copy and paste the code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract MyToken {

    // public variables here
    string public TName = "Harsh";
    string public TAbbrv = "Har";
    uint public TSupply = 0;

    // mapping variable here
    mapping( address => uint ) public balance;

    // mint function
    function mint (address _addr, uint _val) public {
        TSupply += _val;
        balance[_addr] += _val;
    }

    // burn function
    function burn (address _addr, uint _val) public {
        if ( balance[_addr] >= _val ) {
            TSupply -= _val;
            balance[_addr] -= _val;
        }        
    }
}
Compile the code and then deploy it
Add the address to mint/burn to add or burn the tokens.

## Authors

Anshu

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
- If needed, update the contract name and parameters in the `MyToken.sol` file.
- Set up the desired Ethereum network in `truffle-config.js`.

### Running the Program

#### How to Compile and Deploy
1. Compile the smart contract:
    ```bash
    truffle compile
    ```
2. Deploy the smart contract to the chosen Ethereum network:
    ```bash
    truffle migrate --network <network_name>
    ```
    Replace `<network_name>` with the network you set in `truffle-config.js`.

#### How to Interact with the Smart Contract
1. Open the Truffle console:
    ```bash
    truffle console --network <network_name>
    ```
2. Mint tokens:
    ```javascript
    let instance = await MyToken.deployed();
    await instance.mint('0xYourAddress', 1000);
    ```
3. Burn tokens:
    ```javascript
    await instance.burn('0xYourAddress', 500);
    ```

## Troubleshooting

### Common Issues and Fixes
- **Not Enough Gas:** Make sure you have enough ETH to pay for gas fees.
- **Invalid Opcode:** Check for mistakes in your contract code.
- **Network Problems:** Check the network settings in `truffle-config.js`.

## Authors
- Harsh Apoorva
  - GitHub: @HArsh1385

## License
This project is licensed under the MIT License.
