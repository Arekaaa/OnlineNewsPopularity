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
- Regresja liniowa -> 7% dokładności,
- Regresja liniowa z zastosowaniem redukcji wymiarowości (40 wymiarów z 58) -> PCA 5%, TruncatedSVD 6% dokładności,
- Sieć neuronowa -> 9% dokładności,
- Sieć neuronowa z zastosowaniem redukcji wymiarowości (40 wymiarów z 58) -> PCA 1%, TruncatedSVD 3% dokładności.


## Wniosek
1. Najlepszy wynik uzyskano z modelu sieci neuronowej (9%), choć dalej jest to wynik poniżej oczekiwań.
2. Pomimo zastosowania wielu optymalizacji danych, maksymalny wynik wytrenowania wszystkich utworzonych modeli to 9%, co jest wynikiem zdecydowanie zbyt niskim.
3. Baza danych, na podstawie której został utworzony projekt sprawia, że ciężko jest utworzyć dokładny model uczenia maszynowego.

##### Informacje
Więcej informacji na temat projektu od strony teoretycznej, a także wszelkie analizy i wnioski znajdują się
w pliku o nazwie "Projekt_OnlineNewsPopularity.pdf"

#### Autorzy:
- Arkadiusz Pajor
- Mateusz Ornat
