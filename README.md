# NFT-Blind-Box-Smart-Contract
This is a repo that contains a NFT blind box smart contract, with functions like activating sales, minting NFT and reveal box content. The contract has to be implemented on the blockchain in order to work. This repo is only for studying purpose and will not be used for any business purpose.

## Resources
The image resources are stored in pinata cloud that is connected to the IPFS. As this project is only for study purpose, the metadata and image files are also stored in the repo.

## How to compile the code
1. First install metamask on chrome, and create an account that links to the Rinkeby testnet network. After that get around 0.4-0.5 ETH from this website (https://faucets.chain.link/rinkeby)
2. Open the website for Remix (https://remix.ethereum.org/), and depending on your choice, you can either link with Github using this repo, or you can simply connect to localhost by following its instructions and clone the repo locally.
3. Make sure the compiler is up to date as specified in the file blindboxContract.sol, and deploy the contract. (Deploying contract charges gas fee on your metamask wallet, please make sure there is enough ETH in the wallet)
4. Setup the iamge URI by uploading your images to pinata, the URI should be "ipfs://<pinataImageCID>/".
5. After updating the URI, you can try mint a NFT using the mintKeithMeta function specified in the contract, and remember to activate sales and send enough ETH to the transaction (default set to 0.3ETH)
6. Copy your contract address and go to the testnet version of OpenSea.io (https://testnets.opensea.io/), paste the contract address on searchbox to find your contract.
7. You should see the blindbox NFT by then. Use the flipReveal() function to unlock the blindbox.

## Technologies
1. Solidity
2. OpenZepplin
