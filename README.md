# OnlineNewsPopularity

## Wstęp
Repozytorium zawiera cztery modele uczenia maszynowego dla bazy "Online news popularity".

Baza zawiera 61 atrybutów w tym 2 nie służące do predykcji ("url", "timedelta") oraz 1 target ("shares").

Celem projektu jest wytrenowanie kilku modeli uczenia maszynowego, które będą przewidywać jak często dane artykuły będą udostępniane w internecie na podstawie określonych atrybutów.
Problem jest bardziej złożony, ponieważ baza zawiera ogromną ilość danych, które nie chcą współpracować z utworzonymi modelami.

Projekt zawiera jeden plik opisujący teorie, a także cztery notatniki Jupytera, które obrazują kroki wykonane w celu wytrenowania modeli w języku programowania Python z użyciem biblioteki sklearn.

#### Optymalizacja danych:
- Usunięcie wartości nie biorących udziału w procesie predykcji,
- Usunięcie wartości odstających,
- Zastosowanie standaryzacji danych metodą MinMaxScaler.

#### Utworzone modele uczenia:
- Regresja liniowa -> 12% dokładności,
- Regresja liniowa z zastosowaniem redukcji wymiarowości (40 wymiarów z 58) -> PCA 9%, TruncatedSVD 8% dokładności,
- Sieć neuronowa -> 14% dokładności,
- Sieć neuronowa z zastosowaniem redukcji wymiarowości (40 wymiarów z 58) -> PCA 4%, TruncatedSVD 10% dokładności.


## Wniosek
1.	Najlepszy wynik uzyskano z modelu sieci neuronowej (14%), choć dalej jest to wynik poniżej oczekiwań.
2.	Pomimo zastosowania wielu optymalizacji danych, maksymalny wynik wytrenowania uzyskany z wszystkich utworzonych modeli to 14%, co jest wynikiem zdecydowanie zbyt niskim.
3.	Bez optymalizacji badanego zestawu danych, wynik wariancji trenowanego modelu wynosił około 3%. W porównaniu do najlepszego modelu uczenia maszynowego, różnica między nimi wyniosła 10 punktów procentowych. 
4.	Ogromna liczba różnych danych na których przeprowadzaliśmy nasze badania sprawia, że wytrenowanie modelu na poziomie 60-70% dokładności, wymagało by jeszcze większej optymalizacji zestawu danych.
5.	Model sieci neuronowej z zastosowaniem redukcji wymiarowości szkolił się najdłuższą ilość czasu.
6.	Redukcja wymiarowości nie poprawia wyniku wyuczenia modelu.
7.	Baza danych, na podstawie której został utworzony projekt sprawia, że ciężko jest utworzyć dokładny model uczenia maszynowego.
8.	W sieciach neuronowych istnieje możliwość uzyskania trochę lepszego wyniku odpowiednio określając ilość warstw oraz parametrów uczących w metodzie MLPRegressor.


##### Informacje
Więcej informacji na temat projektu od strony teoretycznej, a także wszelkie analizy i wnioski znajdują się
w pliku o nazwie "Projekt_OnlineNewsPopularity.pdf"

##### Autor:
- Arkadiusz Pajor
