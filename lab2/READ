1. Napisać funkcję, która bierze typ i wypisuje jego graf dziedziczenia np. w formie "Any-->Number-->Real-->AbstractFloat-->Float16" (3pkt)

2. Stworzyć typ będący grupą algebraiczną zamkniętą ze względu na mnożenie mod N (12 pkt). Takie grupy mają znaczenie w kryptografii.

Dodatkowe wyjaśnienie:

    Zakładamy konwencję, że jeśli x jest typu Gn{N} to znaczy, że jest elementem grupy zamkniętej ze względu na mnożenie mod N
    Grupa jako całośc jest reprezentowana przez typ Gn{N}, który sam jest obiektem typu Type{Gn{N}}. Patrz wykład oraz wyjasnienie singleton types.
    W zrozumieniu idei singleton types warto zobaczyć przykład wykorzystania w funkcji convert(). 

Szczegóły zadania:

    Typ powinien być parametryzowany liczbą N wg zasady: Liczba x należy do grupy (czyli x jest typu Gn{N}) dla konkretnego N, jeśli:
        jest mniejsza od N
        nie ma wspólnych podzielników z N poza 1 i N. 
    Uwaga: liczba 1 zawsze należy do grupy.

    Stworzyć odpowiedni konstruktor sprawdzający warunki utworzenia obiektu danej grupy. Jeśli liczba jest za duża należy:
        wyliczyć jej resztę z dzielenia przez N
        jeśli reszta nie ma podzielników wspólnych z N poza 1 i N, to należy z niej utworzyć obiekt typu Gn{N}.
        Jesli liczba ma wspólne podzielniki należy rzucic wyjątek DomainError. 

    Taka grupa jest zamknięta ze względu na mnożenie modulo N czyli:
        jeśli a należy do Gn{N} i b należy do Gn{N} to c=(a*b)mod N też należy do Gn{N}.
        Napisać metody funkcji '*' dla obu argumentów typu Gn{N} jak również mieszanych: typu Gn{N} i dowolnych pochodnych typu Integer. Uwaga: pamiętac o zaimportowaniu funkcji "*" modułu Base, inaczej przesłonimy domyślne mnożenie i będą dziać się dziwne rzeczy import Base.* 

    napisać funkcję konwertujacą liczby typu Int64 do typu Gn{N} oraz liczby typu Gn{N} do typu Int64. Przetestowac działanie poprzez wymuszenie konwersji. Pamiętać o zaimportowaniu Base.convert.

    napisać regułe promocji dla liczb typu Gn{N} i dowolnego pochodnego typu Integer. Sprawdzić czy działa poprzez promote_type. Pamiętać o zaimportowaniu Base.promote_rule.

    napisac funkcję realizującą działanie a^x mod N dla a typu Gn{N} i x będącą dowolną pochodna typu Integer korzystając z poprzedniej funkcji. Upewnić się, że w trakcie nie są tworzone duże liczby (duże potęgi liczby a), należy pamiętać, że wystarczy mnożyć reszty, nie trzeba "całych" liczb.

    korzystając z poprzedniej funkcji napisać funkcję obliczającą okres danej liczby typu G{N} czyli najmniejszą liczbę naturalną r, taką, że a^r mod N =1. Wskazówka: można to zrobić sprawdzająć po kolei wszystkie możliwości, można też skorzystać z twierdzenia, że r musi dzielić ilość elementów w grupie.

    napisac funkcję obliczającą element b odwrotny do a, czyli taki, że (a*b) mod N =1. Wskazówka: mozna to zrobić sprawdzając po kolei wszystkie możliwości albo stosując rozszerzony algorytm Euklidesa.

    napisać funkcję obliczającą ilość elementów w grupie modulo N. Funkcja powinna przyjmować jako parametr typ Gn{N} (a nie zmienną typu Gn{N}).

    Przetestuj złamanie wiadomości zaszyfrowanej RSA poprzez obliczenie okresu w odpowiedniej grupie
        Mamy dany klucz publiczny składający się z liczb N=55 oraz c=17 oraz zakodowaną wiadomość b=4
        oblicz okres r wiadomości b w Gn{N}
        oblicz d - odwrotność do c w Gn{r}. Jest to klucz prywatny
        rozkoduj wiadmość a=b^d mod N
        sprawdz, ze faktycznie ta wiadomość była zakodowana kluczem (N,c) czyli, że b = a^c mod N 
