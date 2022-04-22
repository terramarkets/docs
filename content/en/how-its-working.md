--- 
title: How it works
weight: 2
type: docs
notoc: true
--- 

TerraMarkets bets take place in rounds lasting a certain period of time. 

Each of the rounds is presented in the application using a separate card. The following screenshot of the application illustrates this:

&nbsp;
{{< img-center
src="/bets-2.png"
alt="screenshot" >}}
&nbsp;

From the left we can see here:

* two closed rounds (labeled in the upper left corner as **Closed**). For these rounds, cryptocurrency prices have already been set and bets have been settled.
* the current betting round (labeled as **Live**). This round is awaiting the completion and settlement of bets placed and no longer allows bets to be placed
* another round (labeled as **Next**) for which bets can be placed
		
&nbsp; 

The principle of operation and creation of TerraMarkets rounds will be presented on the example of the LUNA/UST cryptocurrency and a round lasting 5 minutes.

In this situation: 

1. Every 5 minutes, a new round appears in the app for which bets can be placed.
   This round is labeled as **Next** 
2. After 5 minutes, this round shall be redesignated as **Live**.  Simultaneously:
    - smart contract saves information about the current price of the cryptocurrency in the round data 
   	- this price is shown on the round card as **Locked price**
   	- locked price is a reference price that allows you to determine the direction of price change at the end of the round
   	- for a round with Live status it is not possible to place bets
3. After another 5 minutes, the round closes and changes to **Closed**
	- TerraMarkets smart contract sets the price of the cryptocurrency at the time of closing the round
	- this price is visible on the round card as **Last price** 
	- depending on whether the Last price is higher or lower than the Locked price (set in point 2), the smart contract determines the direction of price change and settles bets for a given round by determining winnings
