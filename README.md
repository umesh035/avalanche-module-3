# MyToken 

## Overview

The MyToken contract is an Ethereum-based ERC-20 token smart contract written in Solidity. It extends the functionality of the OpenZeppelin ERC20 contract and introduces additional features such as minting, burning, and transfer functions. The contract is designed to be owned by a specific address (tokenOwner), who has exclusive privileges to mint new tokens.

## SPDX-License-Identifier

This contract is released under the MIT License. Please refer to the SPDX-License-Identifier comment in the code for details.

## Contract Details

### MyToken Contract

#### Properties

- **tokenOwner:** The address that initially owns the contract and has exclusive minting privileges.
  
#### Events

- **TokensMoved:** An event emitted whenever tokens are minted, burned, or transferred. It provides details about the sender, receiver, and the amount of tokens involved.

#### Modifiers

- **onlyTokenOwner:** A modifier that restricts certain functions to be callable only by the token owner.

#### Constructor

- Initializes the contract with the specified token name, symbol, and initial token supply. The deployer of the contract becomes the initial token owner.

#### Functions

1. **MINT(address t0_add, uint256 tokenQuantity) external onlyTokenOwner:**
   - Mint new tokens and assign them to the specified address.
   - Emits a TokensMoved event indicating the movement of tokens from the zero address to the specified recipient.

2. **BURN(uint256 tokenQuantity) external:**
   - Burns a specified amount of tokens from the caller's balance.
   - Emits a TokensMoved event indicating the movement of tokens from the caller's address to the zero address.

3. **TRANSFER(address tokenReceiver, uint256 tokenAmount) external returns (bool):**
   - Transfers a specified amount of tokens from the caller's balance to the specified recipient.
   - Emits a TokensMoved event indicating the movement of tokens from the sender to the recipient.

## Author

Umesh 

umeshbkhushappanor@gmail.com
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
