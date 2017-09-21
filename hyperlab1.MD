# Setup

Kill and remove all running containers, including all previously created Hyperledger Fabric chaincode images:
* _docker kill $(docker ps -q)_
* _docker rm $(docker ps -aq)_
* _docker rmi $(docker images dev-* -q)_

# Create a Blockchain network
* _git clone https://github.com/hyperledger/fabric-samples.git_
* _cd fabric-samples/fabcar_
* _./startFabric.sh_

This command launches a peer node, ordering node, Certificate Authority and CLI container. It then 
creates a channel and joins the peer to the channel.
It installs smart contract (i.e. chaincode) onto the peer’s file system and instantiates said chaincode on the channel; It then starts a chaincode container and calls the initLedger function to populate the channel ledger with 10 unique cars

Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ node query.js
Create a client and set the wallet location
Set wallet path, and associate user  PeerAdmin  with application
Check user is enrolled, and set a query URL in the network
Make query
Assigning transaction_id:  ddfeacf1d25275acc7ca525a85055c771a2c63b9c8a388cf3502360ff260e273
returned from query
Query result count =  1
Response is  

*[{"Key":"CAR0", "Record":{"colour":"blue","make":"Toyota","model":"Prius","owner":"Tomoko"}},

*{"Key":"CAR1", "Record":{"colour":"red","make":"Ford","model":"Mustang","owner":"Brad"}},
*{"Key":"CAR2", "Record": {"colour":"green","make":"Hyundai","model":"Tucson","owner":"Jin Soo"}},
*{"Key":"CAR3", "Record": {"colour":"yellow","make":"Volkswagen","model":"Passat","owner":"Max"}},
*{"Key":"CAR4", "Record":{"colour":"black","make":"Tesla","model":"S","owner":"Adriana"}},
*{"Key":"CAR5", "Record":{"colour":"purple","make":"Peugeot","model":"205","owner":"Michel"}},
*{"Key":"CAR6", "Record":{"colour":"white","make":"Chery","model":"S22L","owner":"Aarav"}},
*{"Key":"CAR7", "Record":{"colour":"violet","make":"Fiat","model":"Punto","owner":"Pari"}},
*{"Key":"CAR8", "Record":{"colour":"indigo","make":"Tata","model":"Nano","owner":"Valeria"}},
*{"Key":"CAR9", "Record":{"colour":"brown","make":"Holden","model":"Barina","owner":"Shotaro"}}]
