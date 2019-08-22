# Krawlcat Guide 

## Krawlcat Network Description 

Krawlcat is a Layer-2 decentralized oracle protocol that is built on the Ethereum blockchain. Anyone can participate in the network through the hardware device 'Krawlcat' which runs a nodejs server that communite with open cryptocurrency APIs. With client side validation in place the average values of prices are taken and posted to the smart contract from each individual 'Krawlcat' unit.

In order to participate in the Krawlcat network, a proof of stake is required where the unit holder is asked to deposit 5000 tokens before contributing data to the network. This is to prevent arbitary or polluted data enter the network. The participant can unstake anytime and withdraw itself from the network. Once unstaked, the unit is unable to contribute to the network and post data to the smart contract.

Everytime new data is posted into the network, the smart contract calculates the median and stores it as a singular value. This value can be read and accessed by third parties as a source of truth. With positive contribution to the network the units are rewarded in ERC20 tokens. Large deviations from the current price while posting is handled in the client side. The units are required to post at-least one data point every 2 hours. If they are unable to do so, their rewards are penalized and decreases in amount.

### Build projects using the Krawlcat Oracle Network 

```
Network - Ropsten 

Current Medianizer Address 0x03898c688e6168F3600da15bc53e2eeb673Ca5B9
```

### Interaction steps for retrieving the Oracle data 


1. Use ABI and contract address with web3.js library to interact with the Medainizer contract 

2. Use the read() function to retrieve asset value from the decentralized oracle network
    -  marketId (0 for BTC, 1 for ETH markets)
    -  market price of the assest represented in 10^18 format 

3. Build anything you wish with the Oracle Price! 





