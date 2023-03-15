## Getting Started

To create a new web3 app, run command:
npx thirdweb@latest create --contract

name => framework: Hardhat => name of smart contract => empty contract

To use env variable:
cd web3 => npm install dotenv

get matamask wallet and modify hardhat.config.js file as:

module.exports = {
solidity: {
version: "0.8.9",
defaultNetwork: "goerli",
networks: {
hardhat: {},
goerli: {
url: "https://rpc.ankr.com/eth_goerli",
accounts: [`0x${process.env.PRIVATE_KEY}`],
},
},
settings: {
optimizer: {
enabled: true,
runs: 200,
},
},
},
};

To deploy the web3 app:
npm run deploy

=> connect wallet and do deploy

=> after deploy go to set front end app
