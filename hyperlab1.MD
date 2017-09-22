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



$ docker ps

dev-peer0.org1.example.com-fabcar-1.0-5c906e402ed29f20260ae42283216aa75549c571e2e380f3615826365d8269ba   "chaincode -peer.a..."   40 minutes ago      Up 40 minutes                                                        dev-peer0.org1.example.com-fabcar-1.0
-bash: 16d3c1e02a1f: command not found
Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ 809d03239e16        hyperledger/fabric-tools                                                                                 "/bin/bash"              40 minutes ago      Up 40 minutes                                                        cli
-bash: 809d03239e16: command not found
Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ bbbef8d78798        hyperledger/fabric-peer                                                                                  "peer node start"        40 minutes ago      Up 40 minutes       0.0.0.0:7051->7051/tcp, 0.0.0.0:7053->7053/tcp   peer0.org1.example.com
-bash: 7051/tcp,: No such file or directory
Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ 93f76ba1fef7        hyperledger/fabric-ca                                                                                    "sh -c 'fabric-ca-..."   40 minutes ago      Up 40 minutes       0.0.0.0:7054->7054/tcp                           ca.example.com
-bash: 7054/tcp: No such file or directory
Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ b62da84c854a        hyperledger/fabric-orderer                                                                               "orderer"                40 minutes ago      Up 40 minutes       0.0.0.0:7050->7050/tcp                           orderer.example.com
-bash: 7050/tcp: No such file or directory
Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ 5240655d2bf1        hyperledger/fabric-couchdb                                                                               "tini -- /docker-e..."   40 minutes ago      Up 40 minutes       4369/tcp, 9100/tcp, 0.0.0.0:5984->5984/tcp       couchdb
-bash: 5984/tcp: No such file or directory
Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ 
-bash: Arnes-MacBook-Pro:fabcar: command not found
Arnes-MacBook-Pro:fabcar arnelennartfrantzell$ 5240655d2bf1        hyperledger/fabric-couchdb                                                                               "tini -- /docker-e..."   40 minutes ago      Up 40 minutes       4369/tcp, 9100/tcp, 0.0.0.0:5984->5984/tcp       couchdb







