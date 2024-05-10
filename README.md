# Agoric Dapp Starter: Agoric Basics

This is a basic Agoric Dapp that contains three smart contracts `postal-service`, `sell-concert-tickets`, and `swaparoo` demonstrating different scenarios which can be implemented easily using Agoric SDK. There is also a UI for `sell-concert-tickets` contract that a user can use to buy three different types of concert tickets and pay through a wallet extension in the browser. 

## Getting started

Assuming all the required dependecies are already installed (including node, nvm, docker, Keplr - See [here](https://docs.agoric.com/guides/getting-started/) tutorial on how to install these dependecies.), here are the steps to run `dapp-agoric-basics`: 
- run `yarn install` in the `agoric-basics` directory, to install dependencies of the Dapp.
- run `yarn start:docker` to start Agoric blockchain from the container.
- run `yarn docker:logs` to to make sure blocks are being produced by viewing the Docker logs; once your logs ressemeble the following, stop the logs by pressing `ctrl+c`.
```
demo-agd-1  | 2023-12-27T04:08:06.384Z block-manager: block 1003 begin
demo-agd-1  | 2023-12-27T04:08:06.386Z block-manager: block 1003 commit
demo-agd-1  | 2023-12-27T04:08:07.396Z block-manager: block 1004 begin
demo-agd-1  | 2023-12-27T04:08:07.398Z block-manager: block 1004 commit
demo-agd-1  | 2023-12-27T04:08:08.405Z block-manager: block 1005 begin
demo-agd-1  | 2023-12-27T04:08:08.407Z block-manager: block 1005 commit
```
- run `yarn start:contract` to start the contracts.
- run `yarn start:ui` to start `sell-concert-tickets` contract UI.
- open a browser and navigate to `localhost:5173` to interact with the contract via UI.

To follow more detailed tutorial, go [here](https://docs.agoric.com/guides/getting-started/tutorial-dapp-agoric-basics.html).

## Contributing: Development, Testing

The UI is a React app started with the [vite](https://vitejs.dev/) `react-ts` template.
On top of that, we add

- Watching [blockchain state queries](https://docs.agoric.com/guides/getting-started/contract-rpc.html#querying-vstorage)
- [Signing and sending offers](https://docs.agoric.com/guides/getting-started/contract-rpc.html#signing-and-broadcasting-offers)

See [CONTRIBUTING](./CONTRIBUTING.md) for more on testing.
