# Krawlcat-documentation

## Krawlcat Network Description 

Krawlcat is a Layer-2 decentralized oracle protocol that is built on the Ethereum blockchain. Anyone can participate in the network through the hardware device 'Krawlcat' which runs a nodejs server that communite with open cryptocurrency APIs. With client side validation in place the average values of prices are taken and posted to the smart contract from each individual 'Krawlcat' unit.

In order to participate in the Krawlcat network, a proof of stake is required where the unit holder is asked to deposit 5000 tokens before contributing data to the network. This is to prevent arbitary or polluted data enter the network. The participant can unstake anytime and withdraw itself from the network. Once unstaked, the unit is unable to contribute to the network and post data to the smart contract.

Everytime new data is posted into the network, the smart contract calculates the median and stores it as a singular value. This value can be read and accessed by third parties as a source of truth. With positive contribution to the network the units are rewarded in ERC20 tokens. Large deviations from the current price while posting is handled in the client side. The units are required to post at-least one data point every 2 hours. If they are unable to do so, their rewards are penalized and decreases in amount.

## Read the data from the Krawlcat test network with the following steps

### Current Medianizer Address 0x03898c688e6168F3600da15bc53e2eeb673Ca5B9

### Current Token Address 0xb271E35114A4994D6471EDF5f0a832c851051233

### Pre Requirements and Interaction Steps 

 You will need KCT tokens to deposit into the Medianizer first in order to read the correct value from the Oracle Network. 
 
 Here are the following steps:

1. Create a pull request with your Metamask Ropsten account address and we will deposit 10 KCT tokens to your account shortly

2.  Load ABI and contract address on to My Ether Wallet - https://www.myetherwallet.com

3. Use the read() function to read data from the decentralized oracle network
    -  marketId (0 for BTC, 1 for ETH markets)
    -  you will see a large garbage value as you have not subscribed to the oracle network yet

4.  Once you receive the KCT tokens, use the 10 KCT tokens with the function subscribe() in the following order:
    - _amount (uint256): 10000000000000000000 (10 KCT tokens in 10^18 format)
    - _expiry (uint256): timestamp in the future (e.g. 1577836800 for 2020/01/01)

3. Once the transaction goes through for your subscription, use the read() function to view prices for BTC or ETH markets. The returned result is the price of the assest in big number (10^18)

4. Build anything you wish with the Oracle Price! 


### Resources 

* Build according to swagger documentation - https://swagger.io/docs/

* Examples include - chainlink documentation -> https://docs.chain.link/docs/welcome-to-chainlink
    



