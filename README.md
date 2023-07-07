## Deploying Rain Contracts
Set up the environment by creating a .env file and populating it with 
```sh
DEPLOYMENT_KEY= 

ALCHEMY_KEY_MUMBAI=
ALCHEMY_KEY_POLYGON=
ALCHEMY_KEY_SEPOLIA=
ALCHEMY_KEY_GORELI= 

POLYGONSCAN_API_KEY=
ETHERSCAN_API_KEY=
SNOWTRACE_KEY=
```

Once you have ennvironment setup, follow the steps : 

#### Deploying Contracts

The script clones the contract deployed on one network to another. 
To deploy contracts **run** the following command in shell from the **root of the project**.

To deploy contract to **Avalanche Mainnet** run : 
```sh
ts-node scripts/1-pilot/deployContracts.ts --from mumbai --to avalanche
``` 

To deploy contract to **Avalanche Testnet** run : 
```sh
ts-node scripts/1-pilot/deployContracts.ts --from mumbai --to snowtrace
``` 

To deploy contract to **Goerli Testnet** run : 
```sh
ts-node scripts/1-pilot/deployContracts.ts --from mumbai --to goerli
```

Where arguments for the script are:

- `--from, -f <network name>` : Network name of originating network. Any of ["goerli","snowtrace","mumbai","sepolia","polygon","avalanche"]. Usally this will be a test network.
- `--to, -t <network name>` : Network name of target network where new contract is to be deployed.Any of ["goerli","snowtrace","mumbai","sepolia","polygon","avalanche"]. Usally this will be a main network for a chain.

Wait for all the contracts to be deployed and verified.


