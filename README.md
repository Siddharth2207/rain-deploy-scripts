## Deploying Rain Contracts

Once you have ennvironment setup, follow the steps : 

#### Deploying Contracts

The script clones the contract deployed on one network to another. 
To deploy contracts **run** the following command in shell from the **root of the project**.

```sh
ts-node scripts/1-pilot/deployContracts.ts --from mumbai --to avalanche
```
Where arguments for the script are:

- `--from, -f <network name>` : Network name of originating network. Any of ["mumbai","sepolia","polygon","avalanche"]. Usally this will be a test network.
- `--to, -t <network name>` : Network name of target network where new contract is to be deployed.Any of ["mumbai","sepolia","polygon","avalanche"]. Usally this will be a main network for a chain.

Wait for all the contracts to be deployed and verified.


