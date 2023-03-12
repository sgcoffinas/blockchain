# Blockchain
Simple blockchain implemented in Python to help learn how blockchains work.

### Proof of Work
Using a simple PoW algorithm as follows: the hash of the previous proof combined with the current proof should yield a solution with 4 leading zeroes.

### Consensus
Longest chain of valid blocks will be considered authoritative.

### How to Interact
Included is a simple REST API built in Flask to interact with the blockchain.
##### Deploy
1. Install dependencies via requirements.txt `pip install -r requirements.txt`
2. Run server.py to deploy the API. By default, server runs on port 5000 `python server.py`

##### Endpoints
- `/mine` takes a GET request and will mine a block.
- `/transactions/new` takes a POST request and will create a new transaction on the current block. The body should contain `sender`, `recipient`, and `amount`. 
- `/chain` takes a GET request and will return the full blockchain.
- `/nodes/register` takes a POST request and will register a new node onto the network. Note that if you're running two nodes from the same machine, you will have to change the port of the second node to differ from the first.
- `/nodes/resolve` takes a GET request and will determine the correct chain amongst all of the nodes.
