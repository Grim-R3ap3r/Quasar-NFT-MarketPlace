# `Quasar-NFT-Marketplace` [![Website shields.io](https://img.shields.io/website-up-down-green-red/http/shields.io.svg?style=for-the-badge)](http://shields.io/)

This Project is a fork of Ethereum Boilerplate and demostrates how you can build your own NFT Marketplace. This project of course work on any EVM-compatible blockchain such as Polygon, Avalanche, Binance Smart Chain and other such chains.
<br/>
<br/>
[Link to Quasar](https://quazar.netlify.app/)

![s2](https://user-images.githubusercontent.com/62543734/167544497-658bd04d-3b99-42ae-a0c7-83e9a8566d17.png)




# 🚀 Quick Start

📄 Clone or fork `ethereum-nft-marketplace`:
```sh
git clone https://github.com/Grim-R3ap3r/Quasar-NFT-MarketPlace.git
```
💿 Install all dependencies:
```
cd ethereum-nft-marketplace
npm install 
```
✏ Rename `.env.example` to `.env` in the main folder and provide your `appId` and `serverUrl` from Moralis ([How to start Moralis Server](https://docs.moralis.io/moralis-server/getting-started/create-a-moralis-server)) 
Example:
```jsx
REACT_APP_MORALIS_APPLICATION_ID = xxxxxxxxxxxx
REACT_APP_MORALIS_SERVER_URL = https://xxxxxx.grandmoralis.com:2053/server
```

🔎 Locate the MoralisDappProvider in `src/providers/MoralisDappProvider/MoralisDappProvider.js` and paste the deployed marketplace smart contract address and ABI
```jsx
const [contractABI, setContractABI] = useState();
const [marketAddress, setMarketAddress] = useState();
```

🔃 Sync the `MarketItemCreated` event `/src/contracts/marketplaceBoilerplate.sol` contract with your Moralis Server, making the tableName `MarketItems`
```jsx
event MarketItemCreated (
  uint indexed itemId,
  address indexed nftContract,
  uint256 indexed tokenId,
  address seller,
  address owner,
  uint256 price,
  bool sold
);
```


🚴‍♂️ Run your App:
```
npm start
```


