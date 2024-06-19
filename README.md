# poly-mod-1

---

## NFT Collection Deployment and Migration README

This README provides instructions for deploying an NFT collection on the Ethereum Goerli Testnet, storing images on IPFS via Pinata Cloud, mapping the collection to the Polygon network using token mapper, and finally, transferring and bridging the NFTs from Ethereum to Polygon Mumbai.

## Requirements

- DALLE 2 or Midjourney for generating a 5-item collection.
- IPFS account for storing images, utilizing Pinata Cloud.
- Hardhat for scripting and interacting with Ethereum and Polygon networks.
- Ethereum Goerli Testnet and Polygon Mumbai Testnet accounts with test ETH/MATIC.

## Steps

### 1. Generate Collection Using DALLE 2 or Midjourney

Use either DALLE 2 or Midjourney to generate a collection of 5 unique items.

### 2. Store Items on IPFS Using Pinata Cloud

Upload the generated images to IPFS using Pinata Cloud and obtain the IPFS hashes.

### 3. Deploy ERC721 Contract to Ethereum Goerli Testnet

Deploy an ERC721 contract on Ethereum Goerli Testnet. Include a `promptDescription` function in the contract to return the prompt used for generating the images.

### 4. Map Your NFT Collection Using Polygon Token Mapper

Map your ERC721 contract to the Polygon network using the token mapper. This step is optional but recommended for cross-chain visualization.

### 5. Write Hardhat Script to Batch Mint NFTs

Write a Hardhat script to batch mint all 5 NFTs. Utilize ERC721A for optimal gas usage.

### 6. Write Hardhat Script to Batch Transfer NFTs to Polygon Mumbai

Create a Hardhat script to batch transfer all NFTs from Ethereum Goerli Testnet to Polygon Mumbai Testnet using the FxPortal Bridge.

### 7. Approve and Deposit NFTs to the Bridge

Implement approval mechanisms in the ERC721 contract to allow the NFTs to be transferred. Then, initiate the deposit of NFTs to the FxPortal Bridge for transfer to Polygon Mumbai Testnet.

## Scripts and Contracts

- **Deployment Script**: `deploy.js` handles deployment of ERC721 contract and mapping.
- **Minting Script**: `mint.js` facilitates batch minting of NFTs.
- **Transfer Script**: `transfer.js` manages batch transfer of NFTs to Polygon Mumbai.
- **Contract Code**: ERC721 contract code (`MyNFT.sol`) includes the `promptDescription` function and necessary ERC721A interfaces.

## Additional Notes

- Ensure you have sufficient test ETH/MATIC for gas fees on Ethereum Goerli and Polygon Mumbai Testnets.
- Modify scripts and contract addresses for mainnet deployment if transitioning from testnets.

---

