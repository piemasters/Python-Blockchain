# Python Blockchain

This project is a simple blockchain written in Python. 
Different nodes can be added to the chain, coins can be mined and transactions can be made between nodes.

## Run Node

The run a node run the following:
```
python node.py
```

The run a node on port 5001 run the following:
```
python node.py -p 5001
```

## Project Structure

### Block

* Defines a class for the structure of a single block.

### Blockchain

* Initializes blockchain and open transactions data from a file
* Saves blockchain and opens transactions snapshot to a file
* Generates a proof of work for the open transactions, the hash of the previous block and a random number
* Calculates and returns the balance for a participant
* Returns the last value of the current blockchain
* Appends a new value as well as the last blockchain value to the blockchain
* Creates a new block and adds open transactions to it
* Adds a block that was received via broadcasting to the local blockchain
* Checks all peer nodes' blockchains and replaces the local one with longer valid ones
* Adds a new node to the peer node set
* Removes a new node to the peer node set

### Transaction

* Defines a class for the structure of a single transaction

### Wallet

* Creates a new pair of private and public keys
* Saves the keys to a file
* Loads the keys from the wallet.txt file into memory
* Generates a new pair of private and public keys
* Signs a transaction and returns the signature
* Verifies the signature of a transaction

### Utility
* Hashes a block and returns a string representation of it
* Creates a SHA256 hash for a given input string
* Validates a proof of work number and sees if it solves the puzzle algorithm (two leading 0s)
* Verifies the current blockchain
* Verifies a transaction by checking whether the sender has sufficient coins

## Node & UI

The Wallet & Node page allows you to:

* Create or load a wallet
* Send coins to another user
* View the current blockchain
* View open transactions
* Mine coins 
* Resolve conflicts

The Network page allows you to:

* Add more nodes to the cluster
* Remove nodes from the cluster

Training Source

This Python blockchain is based off of the training course found here: https://www.udemy.com/learn-python-by-building-a-blockchain-cryptocurrency/learn/v4/overview

The course followed the following topics:

* Base Python syntax (variables, operators, functions, ...)
* Loops and conditional statements
* More complex data structures like tuples or dictionaries
* Built-in functions and the standard library Python ships with
* String manipulation
* How to work with files
* Error handling
* Debugging
* Object-oriented programming with classes and inheritance
* Internal & external modules (packages)
* How to spin up an Http server with the Flask package
* Handling Http requests (sending & receiving)

## Future

The following can be investigated to improve the blockchain:

* Improve Error Handling
* Improve Scalability
* Improve Broadcasting with Async Programming and/ or Scheduling
* Control Mining Difficulty (Dynamically)
* Add a Merkle Tree for Transaction
* Validation