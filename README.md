# tix

git clone https://github.com/giulidb/ticket-meteor-dapp

follow instructions there usting >ganache-cli -p 7574 
changing port in truffles.js to 7545

add in truffles.js 
  contracts_build_directory: "~/ticket-meteor-dapp/imports/api/ethereum/truffle/build/contracts",
according  https://github.com/trufflesuite/truffle-migrate/issues/10


truffle develop
compile
migrate


try this now:
--------------
based on this
https://hackernoon.com/ethereum-development-walkthrough-part-2-truffle-ganache-geth-and-mist-8d6320e12269

mkdir tix
cd tix
truffle init
cp ../ticket-meteor-dapp/imports/api/ethereum/truffle/contracts/* contracts/.
add stuff to truffle.js according hackernoon
truffle develop
compile
migrate --network development

new window cd ticket-meteor/
meteor

in browser
localhost:3000


--------------


to solve some problems look at this stuff:


meteor update --release 1.7.1-beta.27

meteor npm install @babel/runtime@latest

meteor npm install --save babel-runtime

npm install react

meteor npm install --save react-mounter react-dom truffle-contract lodash web3 react-addons-css-transition-group react-numeric-input react-datepicker moment react-select

meteor npm install --save @babel/runtime meteor-node-stubs

meteor npm install --save web3 truffle-contract

meteor update --patch
meteor update
meteor update --all-packages
meteor npm install --save @babel/runtime

sudo apt --fix-broken install
sudo apt-get update
sudo apt-get -f upgrade

