# Interact-with-ethereum-using-GETH-client
1. Connecting to ethereum
Following commands are used to install ethereum on instance,ubuntu here.
```
sudo apt-get update
sudo apt-get install software-properties-common
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install -y ethereum
```
2.Start the geth node
```
geth --rinkeby
```
3. Interact with the network.Open another terminal window and run the same ssh command from above, and attach it to Geth.
```
geth attach /home/ubuntu/.ethereum/rinkeby/geth.ipc
```
4.Following message is received after attachment.
```
Welcome to the Geth JavaScript console!
instance: Geth/v1.7.3-stable-4bb3c89d/linux-amd64/go1.9
modules: admin:1.0 clique:1.0 debug:1.0 eth:1.0 miner:1.0 net:1.0
personal:1.0 rpc:1.0 txpool:1.0 web3:1.0
```
5.We can interact with Geth like a local instance! It takes some time to sync with the Ethereum blockchain. The syncing status can be checked as follows:
```
> eth.syncing
{
  currentBlock: 1083241,
  highestBlock: 1410116,
  knownStates: 2890515,
  pulledStates: 2890515,
  startingBlock: 0
}
```
6.Initialize Chain Data
```
geth --datadir ~// init genesis.json
```
7. We can check things like peerCount to see how many nodes we are directly connected to.
```
> net
{
  listening: true,
  peerCount: 12,
  version: "4",
  getListening: function(callback),
  getPeerCount: function(callback),
  getVersion: function(callback)
}
```

8.Exit geth console.
```
> exit
```
9.Terminate Geth node
```
Ctrl-C
```
