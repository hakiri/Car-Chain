# EthereumDevEnvSetup
This repository contains script which will download and install tools required to setup up Ethereum solidity based dApp on your machine.


# Tools installed
- Geth
- Ethereum wallet in mist mode
- Geth miner

All these tools are required for the developement for Ethereum Solidity based dApps.

## Project structure
- src : project source folder.
- src/resources : contains resource files of project.
- src/script : contains project scripts.
- src/tools : geth, ethereum wallet are installed here.

## Prerequisite
- Linux machine
- unzip, tar and wget installed

# How to run

### Download geth, mist and initialize genesis block(One time task)
- cd EthereumDevEnvSetup
- chmod 777 src/scripts/*
- src/scripts/env.sh
- src/scripts/setup.sh
- src/scripts/init_genesis_block.sh

### Run geth and mist
- cd EthereumDevEnvSetup
- src/scripts/start.sh

This will create `process.txt` at `EthereumDevEnvSetup/src/tools` which contains pid's of `geth` and `mist` process.
Please create an account in mist before you start miner.

### Run miner
- Open new terminal, 
- `cd EthereumDevEnvSetup` 
- `src/scripts/miner.sh`

When miner will start it will ask you three options
- Start miner : press 1 to start miner. It will print `null` on console which is its expected behaviour.
- Stop miner : press 2 to stop miner. It returns boolean `true`.
- Enter manual command : Anything - [1, 2]. This opens up console in which you can enter manual commands.
