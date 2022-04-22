--- 
title: Smart kontrakty 
weight: 5
type: docs
notoc: true
--- 

# Sposób ustalania cen

Ceny używane w kontraktach TerraMarkets ustalane są poprzez wyrocznie sterujące działaniami kontraktów TerraMarkets.

Ze względu na to, że blockchain tworzy bloki w nieregularnych odstępach czasowych (dla Terra jest to około 6-15 sekund) przyjęto, że cena dla danego punktu w czasie ustalana jest na podstawie bloku, który został wyprodukowany jako pierwszy po danym punkcie czasowym.

Przykładowo:

- jeśli runda TerraMarkets została otwarta dla zakładów o godzinie 12:00:00 
- zmiana statusu rundy na live następuje o godzinie 12:05:00.
-  jeśli blockchain Terra wyprodukuje kolejne bloki o godzinach
	- 12:04:53
	- 12:05:05
- kontrakt TerraMarkets ustalając cenę (tu locked price) przyjmie cenę zapisaną w pierwszym bloku o czasie większym od 12:05:00 czyli w tym przykładzie cenę zapisaną w bloku o godzinie 12:05:05

&nbsp;
# Specyfikacja smart kontraktów TerraMarkets

###  luna-ust-m5
 - kontrakt dla ceny LUNA/UST
 - czas trwania rundy: 5 minut 
 - sposób ustalania ceny:  
 	Cena ustalana na podstawie ceny exchange_rate odczytywanej z blockchaina Terra.
 - podatek pobierany przez kontrakt: 1%
	
| Sieć     | Adres kontraktu                              |
| -------- | -------------------------------------------- |
| Testnet  | terra1ryl9atvsn4mmeet2ualt307cygspwgwmvcjutc |
| MainNet  | jeszcze niedostępny |
	
	
###  btc-usd-m5
 - kontrakt dla ceny BTC/USD
 - czas trwania rundy: 5 minut 
 - sposób ustalania ceny:  
 	Cena ustalana na podstawie wyroczni ChainLink. Ze względu na częstotliwość aktualizacji użyty został datafeed z sieci Polygon(Matic) o adresie 0xc907e116054ad103354f2d350fd2514433d57f6f.  
 - podatek pobierany przez kontrakt: 1%

| Sieć     | Adres kontraktu                              |
| -------- | -------------------------------------------- |
| Testnet  | terra1mzxva82k989ue63yf5we6kh3fq5uk6gh0acmjn |
| MainNet  | jeszcze niedostępny |

	