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


meteor reset
--------

$ rm -rf node_modules/bcrypt
$ npm install
according to https://stackoverflow.com/questions/46384591/node-was-compiled-against-a-different-node-js-version-using-node-module-versio


updates
----------------

sudo apt --fix-broken install
sudo apt-get update
sudo apt-get -f upgrade

or 
sudo dpkg --configure -a
sudo apt update && sudo apt-get autoclean && sudo apt-get clean && sudo apt-get autoremove
sudo apt dist-upgrade -y

ethereum updates
----------------
replace web3.toWei()
with
web3.utils.toWei()
in imports/startup/server/loader.js
and change 0.7 to 7 etc according to https://github.com/OpenSTFoundation/openst-platform/issues/32

also rm the lines with userRegistry.json
https://github.com/giulidb/ticket-meteor-dapp/search?q=userRegistry.json&unscoped_q=userRegistry.json
