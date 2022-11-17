# DOTcelerator


## Abstract
 
 
Initial fundraising and token allocation for candidate parachain projects (ICO) is managed and under full control of the project team. The current model suffers from a lack of transparency and exposes the contributors to a risk of fraud. 
Our proposal is to create a DotAccelerator, a parachain that allows contributors to exchange KSM/DOT for the candidate  parachain project token. 
Once the candidate  parachain project wins the parachain auction the token is distributed to the ICO participants.
In the future we envision that the base functionality can include governance and effectively allow parachain project treasury to exist on the DotAccelerator parachain, in order to distribute funds and support ongoing parachain project development. 
Milestones




I Proof of Concept - discovery and ideation phase
Build a treasury parachain  (Vasilije Markovic, Przemyslaw Swiatowiec)
Create treasury pallet that can mint a new token in exchange for DOT
Use XCMP for sending preseeded tokens (Alexandre Samartino, Sergey Kulyakhtin)

II Project refinement - functionality extension 
Treasury parachain optimisation:
Enable treasury to allocate funds for development or other project purposes
Enable voting on the treasury parachain as a mean of controlling treasury
Use XCMP to standardise asset teleport to other chains and teleport coins minted by treasury


### Team members and responsibilities

Sergey Kulyakhtin
Vasilije Markovic
Przemyslaw Swiatowiec
Alexandre Samartino
Pallets

### Treasury pallet: 

Minting and distributing tokens proportional to the contribution during ICO and predefined founders share

Tracking the transfers of  tokens which it mints and updating the record of ownership

Teleport pallet:
Pallet using XCMP to teleport tokens on DotCelerator to the parachain project after its launch



Proposal 
![alt text](https://github.com/serkul/DOTcelerator/blob/master/System.png?raw=true)

## Roadmap

- [ ] Come up with minimal functionality which can be achieved within DevCamp
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
