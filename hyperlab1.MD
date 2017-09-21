# Setup

Kill and remove all running containers, including all previously created Hyperledger Fabric chaincode images:
* docker kill $(docker ps -q)
* docker rm $(docker ps -aq)
* docker rmi $(docker images dev-* -q)

# Create a Blockchain network
* git clone https://github.com/hyperledger/fabric-samples.git
* cd fabric-samples/fabcar
* ./startFabric.sh
