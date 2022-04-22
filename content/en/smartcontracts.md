--- 
title: Smart contracts 
weight: 5
type: docs
notoc: true
--- 

# How prices are set

The prices used in TerraMarkets contracts are determined by the oracles that control the operation of TerraMarkets contracts.

Due to the fact that the blockchain creates blocks at irregular intervals (for Terra it is about 6-15 seconds), it is assumed that the price for a given point in time is determined on the basis of the block that was produced first after a given time point.

Example:

- if the TerraMarkets round was opened for betting at 12:00:00 
- change of the status of the round to live takes place at 12:05:00.
- if the Terra blockchain produces more blocks at hours
	- 12:04:53
	- 12:05:05
- the TerraMarkets contract setting the price (here locked price) will accept the price written in the first block with a time greater than 12:05:00, i.e. in this example the price written in the block at 12:05:05

&nbsp;
# TerraMarkets Smart Contract Specification

### luna-ust-m5
 - contract for LUNA/UST price
 - round duration: 5 minutes 
 - method of determining the price:  	
	The price is determined on the basis of the price of the exchange_rate read from the Terra blockchain.
 - tax charged by the contract: 1%

| Network  | Contract address                             |
| -------- | -------------------------------------------- |
| Testnet  | terra1ryl9atvsn4mmeet2ualt307cygspwgwmvcjutc |
| MainNet  | not deployed yet  |
	
### btc-usd-m5
 - contract for btc/USD price
 - round duration: 5 minutes 
 - method of determining the price:  
 	Price determined on the basis of the ChainLink oracle. Due to the frequency of updates, a datafeed from the Polygon(Matic) network with a 0xc907e116054ad103354f2d350fd2514433d57f6f address was used.  
 - tax charged by the contract: 1%

| Network  | Contract address                             |
| -------- | -------------------------------------------- |
| Testnet  | terra1mzxva82k989ue63yf5we6kh3fq5uk6gh0acmjn |
| MainNet  | not deployed yet  |
	