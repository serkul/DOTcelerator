# DOTcelerator
Polkadot DevCamp project: a parachain or substrate pallet or ... to make fundraising in Polkadot/Kusama ecosystem easier

## Idea
The fundraising for blockchain projects often involves Initial Coin Offering (ICO). The presale of tokens is often done on an existing blockchains. When the startup project goes life, the presale tokens have to be transferred on the new chain when the project goes life. This often involves token claims which can be troublesome. Polkadot/Kusama ecosystem has XCMP (Cross Consensus Message Passing) which can alleviates this issue by making a hassle-free token transfer. There are additional benefits for ICO to be done on a parachain or smart contract inside Polkadot/Kusama:
* Onchain governance is possible even while the project is underdevelopment
* Presale tokens can be transferred before their native chain goes life
* Initial spenders can change during the process
* ...

Put all relevant info and references here [Readings](#readings)
Describe functionality of substrate pallets which need to be implemented for DOTcelerator functionality [here](#substrate-pallets-for-dotcelerator)  


## Roadmap

- [ ] Come up with minimal functionality which can be achieved within DevCamp
Proposal 
![alt text](https://github.com/serkul/DOTcelerator/blob/master/System.png?raw=true)
- [ ] Get a green flag from instructors
- [ ] Mock the system and experiment with PolkadotJS on Rococo
- [ ] Set up testing environment, e.g. private parachains 


## Substrate pallets for DOTcelerator
### Treasury Account Pallet
Treasury Account is the main tool for raising and allocating funds. It is a multisig account with the purpose of giving control of the project funds to the token holders from the day one. The main functions of Treasury account are:
1. [Initial Coin Offering (ICO)](#ico)
2. [Dilution](#dilution)
2. [Allocation of treasury funds](#allocation-of-treasury-funds)
3. [Keep records of token owners](#keep-records-of-token-owners)

#### ICO
ICO can be initiated only once by founders as follows:
1. Create a Treasury Account. 
2. Deposit sufficient funds, DOT/KSM, to register a new token on Statemint and pay associated fees.
3. Sign ICO extrinsic sent from Treasury Account (the extrinsic defines, founders share, sale duration, amount of tokens, minimum (and maximum) raised amount, minimal deposit...).
4. Treasury Account mints tokens.
5. Any Polkadot/Kusama account can send funds, to Treasury Account.
6. After the duration of sale is over or maximum raised amount is reached:
    - if the minimum raised amount is not reached, Treasury Account returns the contributions to the participants (minus fees) 
    - otherwise, Treasury Account sends the predefined founders share to the founders, and the rest to the contributors proportional to funds deposited. The records of ownership are kept on Treasury account.
#### Dilution
Dilutions can be initiated by majority of token holders:  
1. Dilution extrinsic is sign by majority of token holders (the extrinsic defines duration, dilution percentage, minimum (and maximum) raised amount ...)
2. Treasury Account mints new tokens.
3. Any Polkadot/Kusama account can send funds, to Treasury Account.
4. After the duration of sale is over or maximum raised amount is reached:
    - if the minimum raised amount is not reached, Treasury Account returns the contributions to the participants (minus fees)
    - otherwise, Treasury Account distributes minted tokens to the contributors proportional to the funds deposited. The records of ownership are kept on Treasury account.
	 
#### Allocation of treasury funds
Treasure account can transfer funds to support project goals. The extrinsic must be signed by majority of token holder (alternatively, yay/nay count in a given period).
#### Keep records of token owners
Treasury account must support ownership transfers by listening to token transfers, which it mints, and updating the records of ownerships 

## Readings
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
https://substrate.stackexchange.com/search?q=xcm
https://substrate.stackexchange.com/questions/109/how-do-parachain-crowdloan-accounts-work?rq=1
https://substrate.stackexchange.com/questions/2328/can-we-mint-burn-statemint-assets-on-other-parachains?rq=1
