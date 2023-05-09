# Overview

 - A blockchain was created by a person (or group of people) using the name (or pseudonym) **Satoshi Nakamoto** in 2008 to serve as the public distributed ledger for bitcoin cryptocurrency transactions, based on previous work by Stuart Haber, W. Scott Stornetta, and Dave Bayer. 
 - The implementation of the blockchain within bitcoin made it the first digital currency to solve the double-spending problem without the need of a trusted authority or central server. The bitcoin design has inspired other applications and blockchains that are readable by the public and are widely used by cryptocurrencies. The blockchain may be considered a type of payment rail.
 - A blockchain is a distributed ledger with growing lists of records (blocks) that are securely linked together via cryptographic hashes. 
 - Each block contains a cryptographic hash of the previous block, a timestamp, and transaction data (generally represented as a Merkle tree, where data nodes are represented by leaves).
 - The timestamp proves that the transaction data existed when the block was created. 
 - Since each block contains information about the previous block, they effectively form a chain (compare linked list data structure), with each additional block linking to the ones before it. 
 - Consequently, blockchain transactions are irreversible in that, once they are recorded, the data in any given block cannot be altered retroactively without altering all subsequent blocks

**Source:** https://en.wikipedia.org/wiki/Blockchain

In other words we can say, it is a:
 - Digital record keeping system
 - Transactions are:
    - Immutable
    - Distributed
    - Duplicated
    - Decentralized

# Terminologies    
 - Coins
 - Tokens
   - Security Tokens
   - Utility Tokens
  
## Programming Languages:
 - https://www.simplilearn.com/blockchain-programming-languages-article

# Different Implementations

## Ethereum
 - Ethereum: Technology that can be used.
 - Ether - currency based on Ethereum
 - Language: Solidity (https://docs.soliditylang.org/en/v0.8.11/) 
 - Uses: Smart contracts
 - main advantage of a smart contract: It uses code to process rules without human intervention.
 - Solidity: https://docs.soliditylang.org/en/v0.8.11/introduction-to-smart-contracts.html#simple-smart-contract
 - Alternative to SOlidity is 

## DAML
Smart contracts key components:
 - People
 - Data
 - Asset
 - Logic

### Installation
 - https://docs.daml.com/getting-started/installation.html
   - Download the installer (~650 Mb, contains the VsCode within)
   - 
   
### Getting started
- https://docs.daml.com/getting-started/index.html

private blockchain:
 - Hyperledger Fabric
 - IBM Blockchain

A major difference between a permissionless blockchain and a permissioned blockchain is: control over access

Blockchain as a Service (BaaS) providers
 - Microsoft
 - Kaliedo

# Ethereum

## Development
 - https://hardhat.org/: Ethereum development environment for professionals
 - https://thegraph.com/en/: The Graph is an indexing protocol for querying networks like Ethereum and IPFS. Anyone can build and publish open APIs, called subgraphs, making data easily accessible.

## NFT
 - https://boredapeyachtclub.com/#/
 - Marketplace: https://opensea.io/

## Blockchain building:
 - https://solana.com/
 - https://polygon.technology/

## DApp: Decentralized App
 - https://aave.com/
 - https://www.dapp.com/topics/defi#banner
 - Defi: Chai, AAve
 
## DeFi:
Decentralized finance, or DeFi for short, refers to the financial smart contract, DApps (decentralized application), and financial protocols built on the blockchain. There are 5 categories of decentralized finance (DeFi) 
- Lending and borrowing (Chaai and Aave)
- Dex (decentralized crypto exchanges that offer access to digital assets without an intermediary) - Coinbase
- Derivatives (Crypto derivatives let investors place bets on the price changes of cryptocurrencies without owning the underlying asset. They provide leverage and the opportunity to profit from bullish and bearish market conditions, much like more conventional financial derivatives like options and futures)
- Payments (Binance)
- Assets (NFTs)

Lending and borrowing are the most popular use cases of DeFi. It is an extremely popular way that users can earn cryptos from lending and borrowing DeFi protocols. Most loans made in DeFi are secured loans with more collateral cryptos than borrowed value. The breakthrough of DeFi is that the financial service now can be real transparent and borderless with the help of crypto asset and the blockchain technology. People around the world can enjoy the benefit of it equally. The 5 category products of decentralized finance(DeFi) - decentralized exchanges, synthetic assets, payments, flash loans, and assets that are accessible by every user globally can only exist on blockchains.

Source: https://www.dapp.com/topics/defi#banner
 
## DApps Use cases:
 - DeFi: Decentralized FInance
 - Tokeniation
 - NFTs
 - DAOs: Decentralized Autonomous Orgainization
   - DApp vs DAO: https://medium.com/swlh/whats-the-difference-between-dapp-idapp-and-dao-and-why-they-are-the-future-of-blockchain-52758f50474e
 - Gaming
 - Other DApps

DApp vs Blockchain?

Ethereum
Solana
LAyer 2
Stacks

## Workflow
 - Develop Workflow

Language: Solidity
Smart Contract: contains the code, Backbone of blockchain development
Environmente: Ethereum Virtual Machine (Hosting environment)
  - Not deployed on Main Ethereum network (Main net -> cost involved to deploy here), its done on testing env
  - Ganache is used for development
    - 10 accounts are created with 100 ethers
Truffle: build tool -> Sets coding env with boilerplate network
web3js -> ui communicating withe Ethereum blockchain network
metamask -> wallet/gateway for transaction based on Ethereum (As browser does not support them out of the box)

# Blockchain for Finance

## Benefits of Blockchain

### Generic
 - Security: distributed consensus based architecture thus eliminating single point of failures
 - Transparency: Acts as single shared surce of truth for network participants
 - Trust
 - Programability: smart contracts is an example of code being executed when any condition is met
 - Privacy
 - High-performance: can be private networks, hyrid network
 - Scalability

### For Finance inddustry
 - Authenticity and scarcity
 - Programable capabilities
 - Streamlined processes
 - Economic Benefits
 - Market Reactivity
 - New products and markets
 

# What are smart contracts

## Contracts (In real world):
 - Contract is made when offer from one party is accepted by other party
 - Consideration is the price paid for the promise of the other party. The price may not necessarily involve money
	- eg1: if you bring me water i will give you choclate
	- eg2: if you bring me water i will pay you 20RS
	
## 3 steps of smart contract
 - Contract tems are agreed to
   - Hard coded and cannot be changed without both parties being aware
 - Smart contract placed on the blockchain
   - Publicly viewed and verified
 - Triggering event causes the contract to be automatically executed
   - Via if/then statemet coding


## Real world use cases: Insurace

### Scenario
Rakesh is about to fly from Mumbai to Paris and he buys on-time arrival insurance  
- He sends RS. 500 worth of cryptocurrency to the ABC insurance smart contracts and provides his flight number
- ABC insurance sends 9500 to the smart contract. so there is total RS. 10,000 total in msart contracts

### Workflow
 - If Rakesh's fligh is on time:
   - ABC insurance is automatically sent  RS. 10,000 from smart contract. This way ABC insurance made RS. 500
 - If flight is late:
   - RS. 10,000 is automatically sent to Rakesh from smart contract
 - Everything is automatic

### Details
 - Everything is automated via smart contracts, saving lots of time and money
 - Rakesh does not have to worry about collecting or fighting for his money from insurance company
 - ABC insurance does not need a lot of people to take orders and process these simple claims


## Potential issues with smart contracts
 - Blockchain and smart contracts are still an emerging area
 - Incorrect structuring of the smart contract via inaccurate coding and/or requirements
 - Insufficient cybersecurity protection to prevent hacking
 - Changes in legislation. 
   - Many governments are still working out the legislation to manage the crypto market, and changes can be applied that affect the contract structure
 - InEffiient use of contracts creating unnecessary costs
   - While Ethereum is not the only platfom to offer DeFi, it does have 80% of market
   - Smart contracts use "gas" () which is due each time a contract executes. This can result in unintended costs which make the DeFi application uneconomical and as a result unattactive to potential customers
 - Most organizations that have already implemented blockchain solutions  now recognize the value of smart contract audit in mitigating these potential risks
   - Specialized smart contract auditors help optimize smart contracts and identify threats and anomaliesin the smart contract code

# Blockchain application for finance

## Asset Management

### Problem
 - Slow and complex process
 - Multiple intermediaries
 - Legacy systems make institutions slow to react to ever-hanging:
   - Investor Demands
   - Increasingly stringent financial regulations   
 
### Solution
 - Blockchain technology can streamline entire asset issuance and lifecycle management process.
 - Can provide rapid secure and customizable issuance of digital assets, fully encoded and automated with investor rights and obligations, and also compliance attributes
 - The digitization of both traditional securities and new financial instruments allows the monetization of a wider range of assets
 - Fractionalized ownership of assets
 - Reduce cost for financial institutions
 - Broadens access to a wider market of potential investors, increasing market size, and encouraging robust liquidity plus secondary market opportunities

## Financial Product Distribution

### Problem
 - Firms traditionally depends on banks, brokers, and other intermediaries to distribute their products
 - Incurring supply chain middleman costs
 - Results is a less close relationship with their customers
 
### Solution
 - Blockchain providers can connect issuers directly with investors and facilitate peer-to-peer marktes, creating secondary market opportunities and promoting greater liquidity
 - Enable investments firms to take control over the entire asset management value chain, and eliminate transfer agent, asset servicing and proxy administartion fees in the process
 
 
# FAQs

## What is "gas" and is it applicble to protected networks?
- The concept of "gas" is specific to public blockchains, such as Ethereum, and is used to measure the computational effort required to execute a transaction or smart contract. The gas price is denominated in ether (ETH), the native cryptocurrency of the Ethereum blockchain, and is paid by the sender of the transaction to the miners who validate and process the transaction.
- In the case of protected blockchains, the gas concept is not mandatory or applicable. Protected blockchains are usually permissioned networks that require participants to be authenticated and authorized to access the network. The transaction fees, if any, are usually determined by the network administrators and can be denominated in a different currency or unit, depending on the design of the blockchain.
- However, some protected blockchains may still use a similar concept to gas to measure the cost of processing transactions or smart contracts. For example, Hyperledger Fabric, a popular permissioned blockchain framework, uses a concept called "chaincode" to define the smart contracts, and the cost of invoking a chaincode is measured in terms of "endorsement policies" and "commitment policies." The cost is paid by the participants who invoke the chaincode and is not related to a native cryptocurrency or token.
 
## Blockchain Types (Public vs Protected)
 - A public blockchain is a distributed ledger that is open to anyone and everyone on the internet. Anyone can read, write, and participate in the network. Bitcoin is an example of a public blockchain.
 - On the other hand, a private blockchain, also known as a permissioned blockchain, is restricted to a specific group of participants who have been given permission to access the network. This means that only authorized parties can read, write, and participate in the network. Private blockchains are often used by businesses and organizations to manage their internal processes and transactions.
 - A protected blockchain, also known as a consortium blockchain, is a hybrid of public and private blockchains. It is a permissioned blockchain that allows a group of organizations or entities to participate in the network. Participants are known and trusted, but the network is not open to the public. Protected blockchains are often used in industries such as finance and supply chain management, where multiple parties need to share data and transactions in a secure and transparent manner.
 - In summary, while public blockchains are open to everyone, private and protected blockchains are restricted to a specific group of participants. Private blockchains are often used for internal processes, while protected blockchains are used for sharing data and transactions among multiple trusted parties.

## High level steps to create permissioned blockchain
1. Define the network participants: Identify the entities or organizations that will participate in the blockchain network and determine their roles and responsibilities. This may involve establishing governance models, access control policies, and legal agreements among the participants.
2. Choose a blockchain platform: Select a blockchain platform that supports permissioned networks, such as Hyperledger Fabric, Corda, Quorum, or Ethereum Enterprise. Each platform has its own features, architecture, and programming models, so choose the one that best suits the requirements of your use case.
3. Set up the blockchain infrastructure: Set up the network infrastructure by deploying the nodes, or servers, that will run the blockchain software. This may involve configuring the hardware, software, and network components, as well as setting up the required security measures, such as firewalls and encryption.
4. Configure the consensus mechanism: Choose a consensus mechanism that governs how the nodes in the network agree on the validity of transactions and blocks. This may involve selecting a built-in consensus algorithm, such as Proof of Authority or Practical Byzantine Fault Tolerance (PBFT), or implementing a custom consensus protocol that fits the needs of your use case.
5. Define the smart contracts and applications: Develop the smart contracts, or business logic, that will define the rules and processes of the blockchain network. This may involve writing the smart contract code using a programming language such as Solidity or Go, or using a visual tool such as Hyperledger Composer. Develop and deploy the applications that will interact with the smart contracts, such as web or mobile apps.
6. Test and deploy the network: Test the blockchain network by running simulations, stress tests, and security audits. Deploy the network to the production environment, and monitor its performance and security.
These are just the general steps to create a permissioned blockchain. The specifics may vary depending on the platform, use case, and requirements of the network.

## Most popular blockchain platforms that support permissioned networks
1. Hyperledger Fabric: Fabric is an open-source framework for building permissioned blockchain networks, developed by the Linux Foundation. Fabric provides a modular architecture, flexible consensus options, and support for smart contracts written in multiple programming languages.

2. R3 Corda: Corda is a distributed ledger platform developed by R3 that focuses on privacy, scalability, and interoperability for enterprise use cases. Corda uses a unique approach called "flow framework" to define the business logic of the network.

3. Quorum: Quorum is an enterprise-grade version of the Ethereum blockchain developed by J.P. Morgan. Quorum is designed for private and consortium networks and includes features such as private transactions and permissioned voting.

4. Hyperledger Besu: Besu is an enterprise-grade Ethereum client developed by ConsenSys that supports both public and permissioned networks. Besu is written in Java and supports the Ethereum Virtual Machine (EVM) and Web3 API.

5. Ethereum Enterprise: Ethereum Enterprise is a version of the Ethereum blockchain that is optimized for enterprise use cases. Ethereum Enterprise includes features such as private transactions, permissioned access, and a customizable consensus mechanism.

6. Chain: Chain is a distributed ledger platform for financial services that supports permissioned networks. Chain uses a unique consensus mechanism called "Federated Consensus" that enables high throughput and low latency.

7. Stellar: Stellar is an open-source blockchain platform that supports permissioned networks for financial services and cross-border payments. Stellar uses a unique consensus mechanism called "Stellar Consensus Protocol" that enables fast and cheap transactions.

These are just a few examples of blockchain platforms that support permissioned networks. Other options include IBM Blockchain, Oracle Blockchain, and Digital Asset. The choice of platform often depends on the specific requirements and use case of the network.

# Integrating a cryptocurrency payment platform with your application:



## Resources
Sure, here's a high-level diagram that shows the steps involved in integrating a cryptocurrency payment platform with your application:

1. Choose a cryptocurrency payment platform
     - BitPay
     - Coinbase
     - CoinPayments

2. Create an account and set up API keys
     - Generate API keys

3. Integrate the APIs into your application
     - Create a payment request and send it to the platform's API endpoint
     - Receive a response containing details about the transaction

4. Test and deploy
     - Test the integration thoroughly
     - Deploy the changes to your production environment

5. Monitor and maintain
     - Monitor the integration for errors and ensure that payments are being processed correctly
     - Consult the platform's documentation or support resources for assistance if needed

    +---------------------+
    | Choose a cryptocurrency |
    | payment platform     |
    +---------------------+
               |
               | (2) Create an account and set up API keys
               v
    +---------------------+
    |  Integrate the APIs  |
    |    into your         |
    |    application       |
    +---------------------+
               |
               | (4) Test and deploy
               v
    +---------------------+
    | Monitor and maintain|
    +---------------------+

# Pending Items
- https://bitpay.com/docs/testing
- ERC 721 polygon
- Metamask
- https://artistaccelerator.mastercard.com/#/

Polkadot, substrate, Rust

ERC 51 NFT

IPSF

# Glossary
 - DEX: decentralized exchange 
 - DApps: decentralized application
 - DeFi: decentralized finance
 - DCL: Distributed Consensus Ledger

# Good Reads
 - https://www.blockchain-council.org/blockchain/solana-vs-polygon-vs-ethereum/
 - https://www.techtarget.com/searchcio/feature/Top-9-blockchain-platforms-to-consider
 - https://v1.cosmos.network/intro
 - https://www.ibm.com/topics/blockchain

# Resources
 - Learning path: https://www.linkedin.com/learning/paths/advance-your-skills-in-the-blockchain
 - Basics: https://www.linkedin.com/learning/blockchain-basics-14414119
 - https://www.linkedin.com/learning/building-an-ethereum-blockchain-app-1-introduction-to-blockchain
 - https://www.baeldung.com/java-blockchains
 - DApp University (Youtube channel)
 - https://docs.daml.com/
 - DAML 101: https://www.youtube.com/playlist?list=PLjLGVUzUMRxUqUXUGltc85HkB7CxsIYR4
 - [blockchain for finance blockchain smart contracts](https://epam.udemy.com/course/blockchain-for-finance-blockchain-smart-contracts)

DAML vs SOLIDITY:
https://blog.logrocket.com/daml-vs-solidity-choose-smart-contract-language/#:~:text=Daml%20code%20is%20considered%20a,%2C%20VMware%2C%20and%20Daml%20Hub.
https://blog.logrocket.com/smart-contract-programming-languages/

https://medium.com/programmers-blockchain/create-simple-blockchain-java-tutorial-from-scratch-6eeed3cb03fa
  - https://github.com/CryptoKass/NoobChain-Tutorial-Part-2/tree/master/src/noobchain
 
 https://www.baeldung.com/java-blockchain
https://github.com/ethereum/solidity
https://docs.soliditylang.org/en/v0.8.19/

https://www.linkedin.com/learning/building-web3-decentralized-apps-in-ethereum/the-dapp-stack?autoSkip=true&autoplay=true&resume=false&u=2113185

https://hardhat.org/
https://aave.com/
https://thegraph.com/en/

-------------


AWS CQRS With even sourcing:
https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/decompose-monoliths-into-microservices-by-using-cqrs-and-event-sourcing.html

https://web.microsoftstream.com/video/567e1370-cb56-4bc3-9d43-ee372e2a9f48?referrer=https:%2F%2Fstatics.teams.cdn.office.net%2F

https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-data-persistence/cqrs-pattern.html

cosmos?
Wallets: Metamask, keplr,Phantom, Exodus
DApp: Compound
NFT marketplace: OpenSea

https://phemex.com/academy/ethereum-vs-solana-vs-cardano-vs-polkadot

https://www.blockchain-council.org/ethereum/erc-token-standards/


# Hyperledger

## Indy
https://wiki.hyperledger.org/display/LMDWG/INDY


https://www.ibm.com/topics/blockchain

https://docs.cloud.coinbase.com/commerce/docs/welcome
https://www.youtube.com/watch?v=iTV89Tqfmgk&list=PLsyeobzWxl7rXr9qxVZPbaoU7uUqP7iPM
https://wiki.hyperledger.org/display/LMDWG/INDY

https://www.coinbase.com/learn/crypto-basics/what-is-lightning
