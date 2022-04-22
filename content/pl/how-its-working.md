--- 
title: Jak to działa
weight: 2
type: docs
notoc: true
--- 

Zakłady TerraMarkets odbywają się w rundach trwających określony czas. 

Każda z rund przedstawiona jest w aplikacji przy pomocy oddzielnej karty. Obrazuje to  poniższy zrzut ekranu aplikacji:

&nbsp;
{{< img-center
src="/bets-2.png"
alt="zrzut ekranu" >}}
&nbsp;


Od lewej strony widzimy tu:

* dwie zamknięte rundy (oznaczone w lewym górnym rogu jako **Closed**). Dla tych rund ustalono już ceny kryptowaluty i rozliczono zakłady
* aktualnie trwającą rundę zakładów (oznaczoną jako **Live**). Ta runda oczekuje na zakończenie i rozliczenie zakładów dla niej zawartych i nie umożliwia już zawierania zakładów
* kolejną rundę (oznaczoną jako **Next**), dla której można zawierać zakłady
		
&nbsp;

Zasadę działania i tworzenia rund TerraMarkets przedstawimy na przykładzie kryptowaluty LUNA/UST i rundy trwającej 5 minut.

W takiej sytuacji: 

1. Co 5 minut w aplikacji pojawia się nowa runda, dla której można zawierać zakłady.
   Runda ta oznaczona jest jako **Next** 
2. Po upływie 5 minut runda ta zmienia oznaczenie na **Live**.  Jednocześnie:
   	- smart kontrakt zapisuje w danych rundy informacje o bieżącej cenie kryptowaluty 
   	- cena ta przedstawiona jest na karcie rundy jako **Locked price**
   	- locked price jest ceną referencyjna umożliwiająca ustalenie kierunku zmiany ceny na koniec rundy
   	- dla rundy o statusie Live nie jest możliwe zawieranie zakładów
3. Po upływie kolejnych 5 minut następuje zamknięcie rundy i zmienia ona oznaczenie na **Closed**
	- smart kontrakt TerraMarkets ustala cenę kryptowaluty w momencie zamknięcia rundy
	- cena ta widoczna jest na karcie rundy jako **Last price** 
	- w zależności od tego czy cena Last price jest wyższa czy niższa od ceny Locked price (ustalonej w punkcie 2) smart kontrakt ustala kierunek zmiany ceny i rozlicza zakłady dla danej rundy ustalając wygrane
