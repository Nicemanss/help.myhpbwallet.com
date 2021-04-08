# How to interact with contracts on <https://myhpbwallet.com>


## How to vote for HPB nodes
0. If you are doing this with a Ledger, you need to ensure that you enable Contract Data in the settings of the HPB app on your Ledger.
1. Head over to <https://myhpbwallet.com/#contracts>
2. Under "Select Existing Contract", select "Vote"
3. Press the "Access" button
4. Under "Read / Write Contract", select "Batch Vote"
5. In the "voterAddr" field, input the public key of the wallet you are going to send your votes from (for example 0xA34dcE25B3DC41d68e7c909EC5c2AEAFbB097309).
6. In the "candidateAddr" field, input the public key of the node you are voting for.

If you wish to support me (Nicemans) for further development, you vote for 0x6b668c559600186477baf091fc572ffdcca7d8ea .
I have so far done the following for the community:
* Got HPB added to https://blocktivity.info
* Created the raffle bot for "HPB Price" chat that uses HPB and its Hardware Random Number Generator: http://verify.myhpbwallet.com
* Assisted Toasty Leaf with integrating HPB into the MMORPG Tale of Toast <https://taleoftoast.com>
* Created the first web and desktop wallet at <https://myhpbwallet.com>
* Created hardware wallet support for Ledger and Trezor
* Created voting ability for Ledger and Trezor
* Created a Unity3d SDK so game developers can implement HPB in their games
* Created SDKs for Ruby, Python and NodeJS
* Created Twitter and Telegram HPB tip bots
* Created Wang Gang the game which runs on HPB: <http://game.myhpbwallet.com>
* Launched the first HPB community website at <https://hpb.community>
* And much more to come.


7. In the "num" field, input the amount of HPB you wish to vote, in Wei. This means that if you want to give a node 1 HPB as a vote, you would input 1000000000000000000 in the "num" box. For easier conversion, you can use <http://eth-converter.com/> - simply add the amount of HPB you wish to vote for in the "Ether" field, and then copy the corresponding number from the Wei field into the "num" field.
8. Select the method of which to access your wallet. Using Ledger or Trezor is Highly recommended for security reasons!
9. Press the "Write" button
10. A box will pop up. Ensure the amount of send is 0 (this is the amount of HPB you would send to the contract address), and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
11. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
12. Check your transaction history on <http://hpbscan.org/address/YOURPUBLICKEY> and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you have tried to vote with a wrong amount (remember to input in Wei, and verify you have the correct amount of coins on your wallet).


## How to cancel a vote for a HPB node
Follow the same steps as "How to vote", but select cancelVoteForContract in point 3.



## How Nodes can set new holder address
### This function is to set a different coin holder address than the address assigned to your BOE and used on the Node. A  scenario could be that you wish to use a hardware wallet like Trezor or Ledger to store the coins that are taken into consideration for your node holdings.

0. First transfer the funds from your BOE wallet to the new (hardware) wallet.
1. Head over to <https://myhpbwallet.com/#contracts>
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
12. Check your transaction history on <http://hpbscan.org/address/YOURPUBLICKEY> and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you have inputted the Ledger/Trezor public key in the "to" input field


#### Secondly you need to tell the about the new holding address, and this part is done with the private key for the wallet which is bound to your BOE. It is recommended that this is done through the "Modify Address" inside the HPB Mobile Wallet, but if for some reason you are unable to use the mobile wallet you can read below how to do it on myhpbwallet.com
13. Under "Read / Write Contract", select "setHolderAddress"
14. In the "coinBase" field, input the public key of your BOE.
15. In te "holderAddr" field, input the public key of your new holder address (Trezor/Ledger address)
16. Select the way you want to authenticate your BOE Wallet (Keystore or private key)
17. Press the "Write" button
18. A box will pop up. Ensure the amount of send is 0 (this is the amount of HPB you would send to the contract address), and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
19. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
20. Check your transaction history on <http://hpbscan.org/address/YOURPUBLICKEY> and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you inputted the wrong data or the approval was not done correctly from the holder address.

21. Verify that your Node address now differs from the Binding address by opening your node on <http://hpbscan.org/nodes>


## Community Vote
### How to vote For or Against the 6 month node election period
0. If you are doing this with a Ledger, you need to ensure that you enable Contract Data in the settings of the HPB app on your Ledger.
1. Head over to <https://myhpbwallet.com/#contracts>
2. Under "Select Existing Contract", select "Burn Vote"
3. Press the "Access" button
4. Under "Read / Write Contract", select "voteProposal"
5. In the "no" field, input: 3fa0648a1bf1431b85690fd2110fd6d6
6. In the "flag" field, input 1 if you wish to vote YES, or 0 if you wish to vote NO.

7. In the "num" field, input the amount of HPB you wish to vote, in *Wei*. Minimum you can vote is 100, and if you wish to vote 100 you would input 1000000000000000000 in the "num" box. For easy conversion, you can use <http://eth-converter.com/> - simply add the amount of HPB you wish to vote for in the "Ether" field, and then copy the corresponding number from the Wei field into the "num" field.
8. Select the method of which to access your wallet. Using Ledger or Trezor is Highly recommended for security reasons!
9. Press the "Write" button
10. A box will pop up. Ensure the amount of send is 0 (this is the amount of HPB you would send to the contract address), and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
11. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
12. Check your transaction history on <http://hpbscan.org/address/YOURPUBLICKEY> and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you have tried to vote with a wrong amount (remember to input in Wei , and verify you have the amount of coins on your wallet).

## Node Lock
### How to Lock 30 000 HPB for your Node. Only use this if you are a node! !!! Pay CLOSE attention to the process so you do not lose 30 000 HPB!!!
0. If you are doing this with a Ledger, you need to ensure that you enable Contract Data in the settings of the HPB app on your Ledger.
1. Head over to <https://myhpbwallet.com/#contracts>
2. Under "Select Existing Contract", select "Node Lock"
3. Press the "Access" button
4. Under "Read / Write Contract", select "stake"
5. In the "nodeAddr" field, input the address which is physically bound to your BOE (Binding Address)
6. Press the "Write" button
7. Open the wallet assigned as your "Node Address" for your physical BOE.
8. A box will pop up. Ensure the amount is set to 30 000 (this is the amount of HPB you would send to the contract address), and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
9. Verify that the address you are sending the 30 000 HPB to is correct on your physical Ledger/Trezor. It should be 0x9c52535541ace93950636649dab6f2892f02ea75.
10. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
11. Check your transaction history on <http://hpbscan.org/address/YOURPUBLICKEY> and verify that it did not fail for some reason.


## Stake HPB
### To stake HPB, use the function below. Current annual return is 5%. If you stake 1000 HPB for the staking period and then have less than 1000 HPB then you do not get any return.
0. If you are doing this with a Ledger, you need to ensure that you enable Contract Data in the settings of the HPB app on your Ledger.
1. Head over to <https://myhpbwallet.com/#contracts>
2. Under "Select Existing Contract", select "Stake HPB"
3. Press the "Access" button
4. Under "Read / Write Contract", select "addHpbLock"
5. In the "addr" field, input the address of your wallet
6. In the "lockNum" field, input the amount of HPB you wish to stake, in WEI. For easy conversion from HPB to WEI you can use <http://eth-converter.com/> - simply add the amount of HPB you wish to vote for in the "Ether" field, and then copy the corresponding number from the Wei field into the "num" field.
7. In the "stageNum", input "2" (without the quotes) as this is the second staking period.
8. Press the "Write" button
9. Open the wallet you inputted in the "addr" field.
10. A box will pop up. Ensure the amount of HPB to send is 0 and that the Gas Limit is not -1 (it should auto generate the required Gas Limit, but if not you can input 8000000 as limit).
11. Check the transaction, and if all looks good press the "Yes, I am sure! Make transaction." button
12. Check your transaction history on <http://hpbscan.org/address/YOURPUBLICKEY> and verify that it did not fail for some reason. If it fails you will see a red exclamation mark next to the transaction. Most likely you have tried to vote with a wrong amount (remember to input in Wei , and verify you have the amount of coins on your wallet).
