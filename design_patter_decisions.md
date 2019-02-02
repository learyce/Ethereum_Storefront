1. The emergency stop pattern is implemented in the Administrators.sol contract, because it's the root level contract of my project (not withstanding the owned library brought in).  By adding the modifier to the root contract, I was able have all my methods that 
modify the contract state implement the onlyWhenNotStopped modifier, which prevents all state modifications when the contract is stopped.

2. Other design decisions I made, were to built the project incrementally.  The Administrators.sol contract is the lowest level and is only in charge of the emergency stop and keeping track of the current admins.  The StoreOwners contract modifies inherits that contract, so that it can know about the current admins, without needing the extra code.  The StoreOwners contrct is only in charge of keeping track of current storeOwners. 

The StoreFactory comes next is in charge of creating new Stores, storing the current stores and returning information about stores.  The ProductFactory comes next and is charge of adding/editing products, users purchasing products and creaing receipts for product purchases.  Currently the design only allows for a user to buy one product at a time and requires exact amounts.  The Storefront project is the highest level contract and is the one we interact with via web3.  It primarly serves up the bulk information about stores, products and receipts as well as handles withdrawls.