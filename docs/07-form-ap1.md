Form AP1
Currently, changes to the state of the register in the database at the Land Registry, representing transfer of ownership, are done through the form AP1.  Form AP1 can be submitted in paper medium, but the Land Registry now offers the electronic Document Registration Service (e-DRS) accepting the form in electronic form with an electronic signature.
The form AP1, in both formats, would be replaced by the blockchain technology mentioned above, but like the transfer of records to the blockchain being a measured process, and the need to use the form to put the first instance of the real property record on the blockchain, the form will be around for some time.  But after this first instance the form will no longer be necessary for that real property, as future transfers will be done by the smart contract.
To implement the transfer to the blockchain the elctronic version of the form would have another two fields.  One for the associated Bitcoin address and the other for the associtated Ethereum address.  Both are an alpha-numberic string of characters.  Both are long,
and are ideally, and really only, meant for copy and paste due to their length and the importance of what they represent and the significant value they store and transfer.
Bitcoin addresses start with a 1 or 3, and Ethereum addresses start with an 0x.  This distinction is important, so that they
are not mixed up.  The current Land Registry database would add two columns to include these two addresses as fields.
Each property record would then be updated when a completed AP1 form was submitted.
After reception of a completed modified AP1 form from a solicitor, with one of it's Ethereum addresses the Land Registry would call the relevant smart contract with the intention to transfer
the ownership information of the property to the associated Ethereum address.  The Land Registry would basically put the property 'up for
sale' on the blockchain, but only the associated Ethereum address that was registered via the AP1 form and
in the Land Registry database could 'buy' the property.  The owner would send a token Bitcoin or Ethereum payment to the Land
Registry and the ownership would be transferred through the transaction.  This token amount could be set to cover 
Land Registry costs.  Once this is done the property is on the blockchain.  The Land Registry would need to make a note of which properties had been transferred to the blockchain.  Maybe through the use of a flag on each affected record in it's database.
One important feature of the Bitcoin and Ethereum addresses mentioned above, is that they will be Multisignature.  One of the reasons for this is that a very important part of the real property transaction process is the source of funding.  The way in which financial intermediaries secure and maintain control over their loan in the absense of a title deed, and an important role for solicitors, is discussed in the section below, Multisignature.
