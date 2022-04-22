--- 
title: Bets tab
weight: 3
type: docs
notoc: true
--- 

The bets tab allows you to place bets.

&nbsp;
{{< img-center
src="/bets-1.png"
alt="screenshot" >}}
&nbsp;


# Key elements 

1. Cryptocurrency checkbox. Allows you to select the cryptocurrency for which we will place bets 
2. Clock showing the time left until it is possible to place bets for the next round
3. Information on how long a particular round lasts
4. Cards showing recently closed rounds
5. Card showing the current round of **Live** bets
6. Next Round Bet Card

&nbsp;
# Information on the round card:

&nbsp;
{{< img-center
src="/round-live.png"
alt="screenshot" >}}
&nbsp;


1. Round status (top left corner of the round card). It can have one value:
    * **Closed**: the historical round for which bets have already been settled
    * **Live:** round currently in progress, for such a round the initial price of the cryptocurrency (locked price) was set, after the end of the round 
    winnings will be determined depending on the price (last price) that the cryptocurrency will reach in a given period
    * **Next**: the next round for which you can place bets
2. Round number. This is the block number of the Terra network in which the TerraMarkets smart contract created the round. 
   It clearly determines the time, start and end of the round and thus also the price of the cryptocurrency enabling the settlement of the round
3. Last price: contains the last price of the cryptocurrency. This price may change as long as the round has Live status
4. Locked price: contains the price of the cryptocurrency set when the round changed its status to Live, this is the reference price to determine in which direction the price will change at the end of the round
5. Price pool: the total amount of bets placed in a given round
6. Payout: multipliers of the expected prize for a given betting direction. For example, if you have placed a bet of 10 UST and the multiplier
   for the direction of the bet you have chosen shows 2.5 you can expect a winning payout of 25 UST. Of course, if only if you have correctly bet on the direction of price change:)
