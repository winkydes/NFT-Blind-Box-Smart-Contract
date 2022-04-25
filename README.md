# NFT-Blind-Box-Smart-Contract
This is a repo that contains a NFT blind box smart contract, with functions like activating sales, minting NFT and reveal box content. The contract has to be implemented on the blockchain in order to work. This repo is only for studying purpose and will not be used for any business purpose.

## Purpose
This repo is only served as a demo of a NFT blindbox event. You can follow the instructions below and try to create a NFT blindbox event.

## Resources
The image resources are stored in pinata cloud that is connected to the IPFS(Interplanetary File System). As this project is only for study purpose, the metadata files are also stored in the repo. To checkout the images by using the metadata, you can copy the CID under the "image" field (which is the string after "ipfs://" till the end) and use the pinata gateway (https://gateway.pinata.cloud/ipfs/<paste your CID here>/).

## How to compile the code
1. First install metamask on chrome, and create an account that links to the Rinkeby testnet network. After that get around 0.4-0.5 ETH from this website (https://faucets.chain.link/rinkeby)
2. Open the website for Remix (https://remix.ethereum.org/), and depending on your choice, you can either link with Github using this repo, or you can simply connect to localhost by following its instructions and clone the repo locally.
3. Make sure the compiler is up to date as specified in the file blindboxContract.sol, and deploy the contract. (Deploying contract charges gas fee on your metamask wallet, please make sure there is enough ETH in the wallet)
4. Setup the baseURI and notRevealedURI by uploading your images to pinata, and create a corresponding JSON file that contains detail on your NFT (such as name, description and attributes), the URI should be "ipfs://<pinataFileCID>/". (Please refer to side notes for more information about this step)
5. After updating the URI, you can try mint a NFT using the mintKeithMeta function specified in the contract, and remember to activate sales and send enough ETH to the transaction (default set to 0.3ETH)
6. Copy your contract address and go to the testnet version of OpenSea.io (https://testnets.opensea.io/), paste the contract address on searchbox to find your contract.
7. You should see the blindbox NFT by then. Use the flipReveal() function to unlock the blindbox.

## Technologies
1. Solidity (Programming language for smart contracts)
2. OpenZepplin (Open source smart contract templates)
3. IPFS with pinata (Decentralized file system that allows us to store our NFT)
4. Remix (IDE for compiling solidity)
  
## Side Note
About the 4th step in compiling the code, we have to upload the images and their corresponding JSON file to IPFS because this allows marketplaces like opensea to interpret the details we give to the NFT. The format of a basic NFT metadata JSON file can be referenced from the "metadata" file in the repo. In the contract, we have to set our own baseURI, which should be the CID of the file that contains all the NFT metadatas (except the unrevealed image and its metadata). You should also upload the unrevealed image and its metadata to pinata, and again use the metadata CID in URI and set it as the unrevealedURI.
