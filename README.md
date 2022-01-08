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
