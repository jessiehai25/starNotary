# Ethereum Smart Contracts, Tokens and Dapps
**PROJECT: Decentralized Star Notary Service Project** - For this project, you will create a DApp by adding functionality with your smart contract and deploy it on the public testnet.

### Token
- Token Name: Star Token
- Token Symbol: STR
- Token Address: 0x2B4D46029558dbFA261AcA01B5d3da9D6b6aCdC9

### Dependencies
For this project, you will need to have:
1. **Node and NPM** installed - NPM is distributed with [Node.js](https://www.npmjs.com/get-npm)
```bash
# Check Node version
node -v
# Check NPM version
npm -v
```


2. **Truffle v5.5.16** - A development framework for Ethereum. 
```bash
# Unsinstall any previous version
npm uninstall -g truffle
# Install
npm install -g truffle
# Specify a particular version
npm install -g truffle@5.0.2
# Verify the version
truffle version
```

3. **Other mandatory packages**:
Ganache v^7.1.0
Solidity v0.5.16 (solc-js)
Node v16.16.0
Web3.js v1.5.3
openzeppelin-solidity@2.3
truffle-hdwallet-provider@1.0.17
```bash
cd app
# install packages
npm install --save  openzeppelin-solidity@2.3
npm install --save  truffle-hdwallet-provider@1.0.17
npm install webpack-dev-server -g
npm install web3
```


### Run the application
1. Clean the frontend 
```bash
cd app
# Remove the node_modules  
# remove packages
rm -rf node_modules
# clean cache
npm cache clean
rm package-lock.json
# initialize npm (you can accept defaults)
npm init
# install all modules listed as dependencies in package.json
npm install
```


2. Start Truffle by running
```bash
# For starting the development console
truffle develop
# truffle console

# For compiling the contract, inside the development console, run:
compile

# For migrating the contract to the locally running Ethereum network, inside the development console
migrate --reset

# For running unit tests the contract, inside the development console, run:
test
```

3. Frontend - Once you are ready to start your frontend, run the following from the app folder:
```bash
cd app
npm run dev
```

---

### Important
When you will add a new Rinkeyby Test Network in your Metamask client, you will have to provide:

| Network Name | New RPC URL | Chain ID |
|---|---|---|
|Private Network 1|`http://127.0.0.1:9545/`|1337 |

The chain ID above can be fetched by:
```bash
cd app
node index.js
```

## Troubleshoot
#### Error 1 
```
'webpack-dev-server' is not recognized as an internal or external command
```
**Solution:**
- Delete the node_modules folder, the one within the /app folder
- Execute `npm install` command from the /app folder

After a long install, everything will work just fine!


#### Error 2
```
ParserError: Source file requires different compiler version. 
Error: Truffle is currently using solc 0.5.16, but one or more of your contracts specify "pragma solidity >=0.X.X <0.X.X".
```
**Solution:** In such a case, ensure the following in `truffle-config.js`:
```js
// Configure your compilers  
compilers: {    
  solc: {      
    version: "0.5.16", // <- Use this        
    // docker: true,
    // ...
```

## Raise a PR or report an Issue
1. Feel free to raise a [Pull Request](https://github.com/udacity/nd1309-p2-Decentralized-Star-Notary-Service-Starter-Code/pulls) if you find a bug/scope of improvement in the current repository. 

2. If you have suggestions or facing issues, you can log in issue. 

---

