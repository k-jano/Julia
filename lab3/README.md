1. Napisać prosty program i przetestować na nim działanie profilera. (5pkt)

    Program powinien wywoływać przez jakiś czas (np. 500 razy) na przemian dwie funkcje, które wykonują w pętli różną liczbę instrukcji. Np. funkcja1 alokuje 100000 stringów, a funkcja2 10000 stringów.
    W efekcie funkcja1 powinna zajmować 10 razy więcej czasu wykonania programu niż funkcja2.
    Prześledzić działanie programu, używając narzędzi do generowania raportów (Profile.print oraz ProfileView.view()).
    Sprawdzić, jak zmieniają się wyniki profilowania dla różnych wartości delay profilera. Kiedy proporcje ilości czasu spędzonego w każdej z funkcji przestają odpowiadać rzeczywistości?



2. Zoptymalizować program pod kątem wydajności (15 pkt):

    Pobrać przygotowany kod niezoptymalizowanego programu. Jest to prosta biblioteka do reprezentacji grafów, która zawiera funkcje do tworzenia grafów w reprezentacji tablicowej i obiektowej, a także przykłady operacji wykonywanych na grafach (bfs, sprawdzanie cyklu Eulera) i funkcje wypisujące elementy grafu.
    Na podstawie materiałów z ćwiczeń i wykładu znaleźć i poprawić fragmenty, które zostały napisane niezgodnie z zasadami tworzenia wydajnych aplikacji w Julii. Aby dostać maksymalną liczbę punktów, należy wykonać przynajmniej 5 (różnych) optymalizacji.
    Pomocniczo kolekcja Set
    W celu weryfikacji poprawek należy użyć narzędzi do pomiaru czasu i alokowanej pamięci.
    Proszę skorzystać z dowolnej metody introspekcji i poddać badaniu optymalizowaną funkcję. Należy wykazać, że zmiany kodu mają wpływ na generowany kod pośredni lub maszynowy.
