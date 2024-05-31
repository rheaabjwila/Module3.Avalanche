Create-and-mint-token
For this project, you will write a smart contract to create your own ERC20 token and deploy it using HardHat or Remix. Once deployed, you should be able to interact with it for your walk-through video. From your chosen tool, the contract owner should be able to mint tokens to a provided address and any user should be able to burn and transfer tokens.

Description
This Solidity code defines a smart contract named RheasCookieToken that represents an ERC20 token with additional functionality.

Description Each Statement and Function
Imports:

ERC20.sol: This imports the ERC20 token standard from the OpenZeppelin Contracts library. The contract inherits from ERC20, allowing it to implement ERC20 token functionality.

Ownable.sol: This imports the Ownable contract from the OpenZeppelin Contracts library. The contract inherits from Ownable, which provides functionality for setting an owner and restricting access to certain functions to only the owner.

Contract Declaration: The contract RheasCookieToken is declared, inheriting from both ERC20 and Ownable.

Constructor: The constructor function is called when the contract is deployed. It takes one argument, Owner, which is the address of the initial owner of the contract. The Ownable constructor is called with this address to set the initial owner. Additionally, the ERC20 constructor is called to initialize the token with the name "RheasCookieToken" and the symbol "NTK". Inside the constructor, 50 * 10**18 tokens are minted to the contract deployer (msg.sender).

Mint Function: The mint function allows the contract owner to mint additional tokens and transfer them to a specified address. This function is only callable by the owner due to the onlyOwner modifier.

Transfer Function: The transfer function overrides the transfer function from the ERC20 contract to customize the transfer behavior. It transfers tokens from the sender's address to the specified recipient.

Burn Function: The burn function allows any address to burn its own tokens, effectively reducing the total supply of the token.
