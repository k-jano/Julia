Napisać program rozwiązujący równania różniczkowe modelu Lotka-Volterra. (6 pkt):
Należy skorzystać z metod rozwiązywania równań różniczkowych zwyczajnych (ODE) oraz algorytmu Rungego-Kutty (RK4).
Program powinien umożliwiać uruchamianie dla różnych parametrów (a, b,c, d, warunki początkowe)
Wynik programu powinien być zapisywany do pliku CSV.
Przykład pliku wyjściowego:
t, x, y, experiment
0.0, 8.0, 4.0, exp1
0.01, 7.794658491266778, 4.200806038699347, exp1
0.02, 7.579314194908448, 4.4024190488284916, exp1
0.03, 7.355084374135755, 4.603574534941281, exp1
0.04, 7.123200666740109, 4.802950130262052, exp1
0.05, 6.884987187517405, 4.999190420559182, exp1
gdzie exp1 to identyfikator eksperymentu.


Wykonać serię eksperymentów dla różnych parametrów modelu L-V i wykonać analizę danych (6 pkt):
Należy wykonać co najmniej 4 eksperymenty dla różnych kombinacji parametrów.
Dane z wszystkich eksperymentów (pochodzące z osobnych plików CSV) należy umieścić w jednej tabeli (DataFrame).
Dla każdego eksperymentu wypisać minimalną, maksymalną oraz średnią liczbę drapieżników i ofiar.
Wyliczyć różnicę między liczbą drapieżników i ofiar jako nową kolumnę.


Narysować wykresy (8 pkt):
Grupę wykresów po jednym dla każdego eksperymentu, pokazujące zależności czasowe dla wszystkich kolumn danych (korzystając z Geom.subplot_grid).
Złożony wykres przestrzeni fazowej z nałożonymi seriami z wszystkich eksperymentów przykład.
Na każdym wykresie należy umieścić podpisy osi oraz legendy, zawierające parametry eksperymentów.
