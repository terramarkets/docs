--- 
title: Zakładka bets
weight: 3
type: docs
notoc: true
--- 

Zakładka bets umożliwia zawieranie zakładów.

&nbsp;
{{< img-center
src="/bets-1.png"
alt="zrzut ekranu" >}}
&nbsp;

# Najważniejsze elementy 

1. Pole wyboru kryptowaluty. Umożliwia wybranie kryprowaluty, dla którą będziemy zawierać zakłady 
2. Zegar pokazujący czas upływający do momentu gdy możliwe jest zawarcie zakładów dla następnej rundy
3. Informacja o tym jak długo trwa poszczególna runda
4. Karty przedstawiające ostatnio zamknięte rundy
5. Karta przedstawiająca aktualną rundę zakładów **Live**
6. Karta umożliwiająca zawarcie zakładów na kolejną rundę


&nbsp;
# Informacje na karcie rundy:

&nbsp;
{{< img-center
src="/round-live.png"
alt="zrzut ekranu" >}}
&nbsp;

1. Status rundy (lewy góry róg karty rundy). Może mieć jedną wartości:
    * **Closed**: runda historyczna, dla której zakłady zostały już rozliczone
    * **Live:** runda aktualnie trwająca, dla takiej rundy ustalono cenę początkową kryptowaluty (locked price), po zakończeniu rundy 
    ustalone zostaną wygrane w zależności od ceny (last price) jaką osiągnie kryptowaluta w danym okresie
    * **Next**: kolejna runda, dla której można obstawiać zakłady
2. Numer rundy. Jest to numer bloku sieci Terra, w którym smart kontrakt TerraMarkets utworzył daną rundę. 
   Jednoznacznie ustala on czas, rozpoczęcia i zakończenia rundy a co za tym idzie również ceny kryptowaluty umożliwiające rozliczenie rundy
3. Last price: zawiera ostatnią cenę kryptowaluty. Cena ta może ulegać zmianie dopóki runda ma status Live
4. Locked price: zawiera cenę kryptowaluty ustaloną w momencie gdy runda zmieniła swój status na Live, jest to cena referencyjna dla określenia w jakim kierunku nastąpi zmiana ceny na końcu rundy
5. Price pool: łączna kwota zakładów zawartych w danej rundzie
6. Payout: mnożniki spodziewanej nagrody dla danego kierunków zakładów. Przykładowo jeśli zawarłeś zakład na kwotę 10 UST a mnożnik
   dla kierunku zakładu, który wybrałeś pokazuje 2.5 możesz spodziewać się wygranej wypłaty 25 UST. Oczywiście jeśli tylko jeśli prawidłowo obstawiłeś kierunek zmiany ceny:)
