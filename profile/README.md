# DOOKIES

Take full control of your cookies with dookies - anonymous, ZKP-based and incentivized data analytics and tracking for all users with better ad personalization at the same time.

## Overview
The main criteria of dookies, as mentioned in the short description, is to have ZK-cookies associated with an anonymous decentralized unique identifier (such as a wallet address) that can be chosen to b traded (for the purpose of data analytics) with companies that need this data. 
In our implementation for the project the primary actors are the user and the advertiser. Account abstraction is used to not only uniquely identify each of these actors but also allow the advertisers to make payments in crypto and the users, should they choose to, to participate in the incentives program.
The selective disclosure of data (ZK cookies) is done using sismo connect's communication protocol where, in simple terms, the user's cookie data is encrypted in such a way that the company requesting said data can receive an attestation of it without finding out about the source of the data that has been generated. This not only preserves user privacy but also allows for companies to provide more targeted ads since they are more likely to receive legitimate data without redundancy, 
Finally, for amount of data shared by a user or for ad publishing websites hosting ads for these users, smart contracts are written for these advertisers to automatically make payments to them in crypto.
Additionally, we have also designed an ads engine using cartesi for ad targetting with data collected from our ZK cookies.

## Implementation
For the first part of the project, account abstraction is done using polygon's account abstraction based on ERC-4337 and the identifiers are connected to a dookie wallet which is based on Ethereum Foundation's Trampoline Wallet. 
 - https://github.com/D00ki3s/account-abstraction 

Next, sismo connect is used for the main purpose - trading of data in groups by means of data gems. The user's data vaults generate attestation evidence for data that is stored their in order to work as a ZK cookie. 
 - https://github.com/D00ki3s/user-sismo-connect
 - https://github.com/D00ki3s/user-backend
 
The Advertisers use Aave GHO to make the payments.
 - https://github.com/D00ki3s/dookies-advertiser

