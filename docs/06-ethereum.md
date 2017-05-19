#### Ethereum

 "Ethereum is a public blockchain-based distributed computing platform, featuring smart contract functionality. It provides a decentralized virtual machine, the Ethereum Virtual Machine (EVM), that can execute peer-to-peer contracts using a cryptocurrency called ether."[[15]](14-references.md)

 Ethereum implements smart contracts. In the context of the a real property transaction, in exchange for a payment in bitcoin or ether to the seller of the real property, the smart contract transfers ownership from the seller to the buyer, and stores this information on the blockchain.

 There are two possible uses of DLTs that are presented below. The first is to use Ethereum's smart contracts as the ownership transfer mechanism combined with bitcoin as payment, (Diagram 3). The second is to use Ethereum for both sides of the transaction: ownership transfer and payment, (Diagram 4). Both these use cases could be implemented.

 Bitcoin and Ethereum have separate blockchains. So to implement the first use case a 'bridge' is needed between the blockchains to verify the bitcoin transaction on the Ethereum blockchain by relaying the bitcoin transaction to the smart contract. This bridge has been implemented in Ethereum and is called BTC Relay.[[16]](14-references.md)

 The following diagram shows the real property transaction processs in the first use case:

  Diagram 3: Arrow Flow Diagram of buyer/seller transaction process. Ownership transfer: Ethereum; Payment: Bitcoin

   Seller calls smart contract, advertising their real property and their bitcoin address >
   Buyer sends bitcoin to sellers bitcoin address >
   BTC Relay verifys buyers bitcoin transaction to sellers bitcoin address >
   Ethereum contract executes registering the buyers new ownership of the property  
   
   time taken: < 60 minutes   

 In the first step of the above diagram, the relevant smart contract is called by the seller. Only the owner can call the smart contract and therefore put the real property up for sale. The smart contract would check the data sent with the owners transaction against the ownership details stored in the smart contract.

 Before a contract can be called it must be written and deployed to the blockchain, which is done only once. The contract in this case would be written by the Land Registry. Once a contract is deployed on the blockchain it is permanent and immutable. But contracts can call other contracts. Also a variable in a contract can be coded that allows mutable links to any contract. That means that any data that changes over time could be pointed to in a new smart contract, for example tax rates.

 In the second step the buyer sends a bitcoin transaction to the sellers bitcoin address, given by the seller. The transaction contains a field called OP\_RETURN that can hold data. This data field would contain identifier details of the buyer: the buyers Ethereum address, the real property address and the buyers name. Other data could be added but because of the size contraints of the data field it may be necessary to store this data as a hash.

 "A cryptographic hash function is a hash function which takes an input (or 'message') and returns a fixed-size alphanumeric string, which is called the hash value (sometimes called a message digest, a digital fingerprint, a digest or a checksum)."[[17]](14-references.md)

 The third step involves relaying the confirmation of the bitcoin transaction to the above mentioned smart contract. Bitcoin has been used as the payment in this example, but if ether was used in step 2 this process would be simpler. i.e. removes the need for BTC Relay.

 The fourth step is where the contract executes, putting the buyers details on the blockchain. Smart contracts are immutable but they also contain a small amount of mutable storage. A hash of the buyer's identifiers, mentioned above, would be put here. A contract can hold 2^261 possible records[[18]](14-references.md) of real properties. Each hash would represent the current owner of an individual real property, and would be stored in one of these records. This data would be the proof of ownership of a real property.

 Real property ownership and transfer can be tracked through time on the blockchain by searching for the various transactions on the Bitcoin and Ethereum blockchains, so the Land Registry could query these databases finding the chain of current and past ownership of every real property. It is the data fields in transactions as well as the storage in the smart contract that would contain a complete history and record of ownership and transfer of real properties.

 The following diagram shows the real property transaction processs in the second use case:

  Diagram 4: Arrow Flow Diagram of buyer/seller transaction process. Ownership transfer: Ethereum; Payment: Ether

   Seller calls smart contract, advertising their real property and their ether address >
   Buyer sends ether to sellers ether address >
   Ethereum contract executes registering the buyers new ownership of the property  
   
   time taken: < 6 minutes   
   
 The process shown in Diagram 4 is simpler than Diagram 3 in both design and use. It uses ether as the payment currency and therefore BTC relay is not needed. Implementing the Ethereum only option would be the 'easier' solution, but offering both solutions would provide redundency and flexibility.

 While presenting the major steps in the real property transaction process the above two diagrams are a simplified overview. Current processes such as property price negotiation, funding, including deposit, surveys, conveyancing searches, and the property chain (as distinct from the blockchain) that are currently handled by intermediaries would need to be developed around this new blockchain model and coded into Ethereum's smart contracts.

 The way in which the real property would be added to the blockchain by the Land Registry is through the form AP1.

 