# Waves Platform smart contracts

Waves Platform is a global public blockchain platform, providing functionality for implementing the most-needed scenarios for an account and token control. Waves smart contracts have a two-level mechanism with an own first-level language designed for smart contracts interaction, RIDE. On September 10th, Waves Platform released a new version of node \(block 1,190,000\) supporting their first implementation, Non-Turing complete Smart contracts.

![WAVESPLATFORM.COM](../.gitbook/assets/image%20%2810%29.png)

wavesplatform.com

RIDE has smart accounts and smart assets for embedding the calculation system. This level has a simple-syntax functional language for scripting with pre-calculated complexity due to Turing-incompleteness. Implementation of the smart contract language has 5 principal stages \(Begicheva & Smagin, 2018\):

1. Parsing,

2. Compilation,

3. Deserialization,

4. Cost computation,

5. Evaluation.

Kolin will incorporate a hybrid added value by using a hybrid Data Storage and Data processing system

Data Storage is represented by traditional databases for storing data off-chain. The blockchain provides distributed, immutable storage with built-in integrity checking; however, it has a maximum capacity based on the standard block size and block rate. To provide integrity verification for large amounts of data, it is common to store the data off-chain and store a hash of the data on-chain. This guarantees that the data is not been modified while protecting the blockchain from becoming bloated.

Data Processing is represented by an external system used for additional processing. Smart contracts execute on the blockchain, meaning that each member of the peer network must execute the code to remain in sync with the current state of the network. If smart contracts commonly require large amounts of processing power to complete, devices external to the peer network may be used to augment the processing power of the network.

