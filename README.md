[//]: # (SPDX-License-Identifier: CC-BY-4.0)

# Walkthrough to run the changed Chaincode

1.The first step is to get the hyperledger fabric test-network running:
	Test-network may already be running, to shut it down, first change directory to fabric-samples/test-network and then run `./network.sh down`. 
	
	To Start the network again, while also creating the channel: 

	./network.sh up createChannel -c mychannel -ca

2.  Deploy the updated chaincode to the channel
 
	./network.sh deployCC -ccn basic -ccp ../asset-transfer-basic/chaincode-javascript -ccl javascript  

Where : basic is the name of the chaincode,  ../asset-transfer-basic/chaincode-javascript is the directory of the chaincode and javascript  is the language of the source code of chaincode.

3. Change directory to fabric-samples/asset-transfer-basic/application-javascript . Open your preferred code editor and open a terminal within it and run `npm install`
 And then to run the main code use the command `node app.js`.

You will get the desired output.


