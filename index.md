# How to interact with contracts on myhpbwallet.com


## How to vote for HPB nodes
0. If you are doing this with a Ledger, you need to ensure that you enable Contract Data in the settings of the HPB app on your Ledger.
1. Head over to https://myhpbwallet.com/#contracts
2. Under "Select Existing Contract", select "Vote"
3. Press the "Access" button
4. Under "Read / Write Contract", select "vote"
5. In the "voterAddr" field, input the public key of the wallet you are going to send your votes from (for example 0xA34dcE25B3DC41d68e7c909EC5c2AEAFbB097309).
6. In the "candidateAddr" field, input the public key of the node you are voting for (for example 0x6b668c559600186477baf091fc572ffdcca7d8ea to vote for Nicemans who is the creator of myhpbwallet.com)
7. In the "num" field, input the amount of HPB you wish to vote, in Wei. This means that if you want to give a node 1 HPB as a vote, you would input 1000000000000000000 in the "num" box. For easier conversion, you can use http://eth-converter.com/ - simply add the amount of HPB you wish to vote for in the "Ether" field, and then copy the corresponding number from the Wei field into the "num" field.
8. Select the method of which to access your wallet. Using Ledger or Trezor is Highly recommended for security reasons!
9. Press the "Write" button
10. A box will pop up. Ensure the amount of send is 0 (this is the amount of HPB you would send to the contract address), and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
11. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
12. Check your transaction history on http://hpbscan.org/address/YOURPUBLICKEY and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you have tried to vote with a wrong amount (remember to input in Wei, and verify you have the correct amount of coins on your wallet).


## How to cancel a vote for a HPB node
Follow the same steps as "How to vote", but select cancelVoteForContract in point 3.



## How Nodes can set new holder address
### This function is to set a different coin holder address than the address assigned to your BOE and used on the Node. A  scenario could be that you wish to use a hardware wallet like Trezor or Ledger to store the coins that are taken into consideration for your node holdings.

1. Head over to https://myhpbwallet.com/#contracts
2. Under "Select Existing Contract", select "Set Node holder address"
3. Press the "Access" button


#### First you will need to show that you own the address in question that is holding your coins (your new Ledger/Trezor wallet), which is done with "setApproval".
4. If you are doing this with a Ledger, you need to ensure that you enable Contract Data in the settings of the HPB app on your Ledger.
5. Under "Read / Write Contract", select "setApproval"
6. In the "to" field, input the public key of your BOE
7. On the "approved" bool, select "True"
8. Select the method of which to access your holding wallet. Using Ledger or Trezor is Highly recommended for security reasons!
9. Press the "Write" button
10. A box will pop up. Ensure the amount of send is 0 (this is the amount of HPB you would send to the contract address), and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
11. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
12. Check your transaction history on http://hpbscan.org/address/YOURPUBLICKEY and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you have inputted the Ledger/Trezor public key in the "to" input field


#### Secondly you need to tell the about the new holding address, and this part is done with the private key for the wallet which is bound to your BOE
13. Under "Read / Write Contract", select "setHolderAddress"
14. In the "coinBase" field, input the public key of your BOE.
15. In te "holderAddr" field, input the public key of your new holder address (Trezor/Ledger address)
16. Select the way you want to authenticate your BOE Wallet (Keystore or private key)
17. Press the "Write" button
18. A box will pop up. Ensure the amount of send is 0 (this is the amount of HPB you would send to the contract address), and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
19. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
20. Check your transaction history on http://hpbscan.org/address/YOURPUBLICKEY and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you inputted the wrong data or the approval was not done correctly from the holder address.
