# Setup

Kill and remove all running containers, including all previously created Hyperledger Fabric chaincode images:
* docker kill $(docker ps -q)
* docker rm $(docker ps -aq)
* docker rmi $(docker images dev-* -q)

# Create a Blockchain network
* git clone https://github.com/hyperledger/fabric-samples.git
* cd fabric-samples/fabcar
* ./startFabric.sh
This command launches a peer node, ordering node, Certificate Authority and CLI container. It then 
creates a channel and joins the peer to the channel.
It installs smart contract (i.e. chaincode) onto the peer’s file system and instantiates said chaincode on the channel; It then starts a chaincode container and calls the initLedger function to populate the channel ledger with 10 unique cars

