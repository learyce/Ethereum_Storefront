
# Ethereum Storefront.  

- Use Npm run dev to run this project's lite server. 

- A collection of online stores were buyers and sellers can interact.

- The contract has one owner, which allowed to add or remove any number of admins.  Those admins (as well as the owner) are able
to add or remove from another group of addresses which designate store owners.  A storeowner is able to create new stores as well as
add/edit products to their existing stores.  A storeowner is also able to withdraw funds from any one of their stores, 
assuming that store has funds to withdraw.  Any user is allowed to shop and purchase products from any store.


- The UI consists of four sections.  Owner, Admin, Storeowner and Shopper.  All users have access to the shopper section
and the other tabs should only be present if the current web3 address exists in the admin/store owner groups or is the contract owner.

- The Owner/Admin tabs allow a user to add or remove admins/store owners respectively.  The storeowner tab allows a user to create new store,
create new products, edit existing products and withdraw funds from a store.

- The shopper tab allows a user to buy goods and displays a receipt for each good that they've purchased.
