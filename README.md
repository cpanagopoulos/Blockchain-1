# Blockchain-1
## Background
You have just landed a new job at ZBank, a small, innovative bank that is interested in exploring what
blockchain technology can do for them and their customers.
Your first project at the company is to set up a private testnet that you and your team of developers
can use to explore potentials for blockchain at ZBank. You have decided on setting up a testnet because 
there is no real money involved, which will give your team of developers the freedom to experiment.

## Challenge
* Puppeth, to generate your genesis block.

* Geth, a command-line tool, to create keys, initialize nodes, and connect the nodes together.

* The Clique Proof of Authority algorithm.

# Instructions

1. Creat accounts for two nodes using separate datadir using geth for the network.

2. Generate a geneisis block

* To generate a genesis block, run puppeth, name your network, and select the option to configure new genesis block.
* Choose the clique (Proof of Authority) consensus algorithm.
* Paste both account addresses from step 1 at a time into the lists of accounts to seal (make sure to remove 0X from account adresses).
* Paste the same addresses in the list of accounts to prefund. And because they are no blowck rewards in POA, you'll need to pre-fund.
* Complete the rest of the prompts (hitting enter).
* Once back at the main menu choose the " Manage existing Genesis" option.
* Export configurations. This will faill to create two of the files, but only one is needed "smbank.json".

3. After completing the genesis block creation, we will initialize the nodes with the genesis' json file previously created.

4. Nodes can be used to begin mining blocks.

  Nodes should be run in different terminal windows with the commands.

  NOTE: Type your password and hit enter even if you can not see it visually.
  
5. Open two separate terminal windows, one for each node.
  * In the first terminal copy and paste node1 ./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --http --allow-insecure-unlock
  * Once prompted, enter your password. As the first node is running, enter node2 in the second terminal window ./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
  * NOTE: you will need to grab the complete enode address from terminal one inorder to update the node2 line before completing step 2
  * Once the nodes are running successfully, open the MyCrypto app to send a tx!

6. Once the MyCrypto app loads, you will need to change the network setting before sending a transaction:
  * Click _Change Network_ at the bottom left of the app, and select _+ Add Custom Node_ and fill out the fields asssociated with your network

7. Now you will need to open your node address to send a tx:
  * you will get a prompt that says you are sending yourself a transaction. This is OK as we are testing the process.

8. Once completed you should receive a green banner at the bottom of the app confirming the transaction was successfully sent.
