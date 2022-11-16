# DOTcelerator
Polkadot DevCamp project: a parachain or substrate pallet or ... to make fundraising in Polkadot/Kusama ecosystem easier.

## Idea
The fundraising for blockchain projects often involves Initial Coin Offering (ICO). The presale of tokens is often done on an existing blockchains. When the startup project goes life, the presale tokens have to be transferred on the new chain when the project goes life. This often involves token claims which can be troublesome. Polkadot/Kusama ecosystem has XCMP (Cross Consensus Message Passing) which can alleviates this issue by making a hassle-free token transfer. There are additional benefits for ICO to be done on a parachain or smart contract inside Polkadot/Kusama:
* Onchain governance is possible even while the project is underdevelopment
* Presale tokens can be transferred before their native chain goes life
* Initial spenders can change during the process
* ...

Put all relevant info and references here [Readings](#readings)


## Roadmap

- [ ] Come up with minimal functionality which can be achieved within DevCamp
Proposal 
![alt text](https://github.com/serkul/DOTcelerator/blob/master/System.png?raw=true)
- [ ] Get a green flag from instructors
- [ ] Mock the system and experiment with PolkadotJS on Rococo
- [ ] Set up testing environment, e.g. private parachains 

### Readings
XCM description from Polkadot Wiki:
https://wiki.polkadot.network/docs/learn-xcm

The above has a link to XCM format description including available instructions set https://github.com/paritytech/xcm-format

A series of articles explaining motivation and mechanisms of XCM format in details:

[XCM: The Cross-Consensus Message Format](https://medium.com/polkadot-network/xcm-the-cross-consensus-message-format-3b77b1373392)

[XCM Part II: Versioning and Compatibility](https://medium.com/polkadot-network/xcm-part-ii-versioning-and-compatibility-b313fc257b83) 

[XCM Part III: Execution and Error Management](https://medium.com/polkadot-network/xcm-part-iii-execution-and-error-management-ceb8155dd166)



#### Relevant pallets
https://github.com/paritytech/cumulus/tree/master/pallets/xcm
https://github.com/paritytech/cumulus/tree/master/pallets/xcmp-queue
https://github.com/paritytech/polkadot/tree/master/xcm/pallet-xcm


#### Tangential useful info

https://www.youtube.com/watch?v=5cgq5jOZx9g&ab_channel=ParityTech
https://medium.com/polkadot-network/xcm-the-cross-consensus-message-format-3b77b1373392
https://medium.com/oak-blockchain/polkadot-xcm-cross-chain-asset-transfer-demo-53aa9a2e97a7
https://medium.com/polkadot-network/xcm-part-ii-versioning-and-compatibility-b313fc257b83
https://substrate.stackexchange.com/search?q=xcm
https://substrate.stackexchange.com/questions/109/how-do-parachain-crowdloan-accounts-work?rq=1
https://substrate.stackexchange.com/questions/2328/can-we-mint-burn-statemint-assets-on-other-parachains?rq=1
