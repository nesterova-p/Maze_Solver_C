## Cel projektu
Celem projektu jest stworzenie programu do znajdowania ścieżki przez labirynt wczytany z pliku tekstowego. Labirynt jest reprezentowany jako plik zawierający określone punkty:

Punkt wejścia („P”)
Punkt wyjścia („K”)
Ściany („X”)
Miejsca, po których można się poruszać (spacje).

## Przykład formatu labiryntu 10x10:
```
XXXXXXXXXXXXXXXXXXXXX
P           X     X X
XXX XXX XXX X XXX X X
X X X   X X   X X X X
X XXX XXX XXXXX X X X
X X   X       X   X X
X X XXX XXX X X XXX X
X   X X X   X X X   X
XXXXX X X XXX X X X X
X     X X X X X X X X
X XXXXX X X X X X X X
X X     X X   X   X X
X X XXXXX X XXXXXXX X
X   X   X X   X     X
X XXXXX X XXX X XXXXX
X X     X X   X   X X
X X X XXX XXXXXXX X X
X   X X   X     X   X
XXXXX X XXX XXX XXX X
X     X       X     K
XXXXXXXXXXXXXXXXXXXXX
```

## Wymagania dotyczące rozmiaru labiryntu
Maksymalny rozmiar labiryntu to 1024 x 1024 (liczony po możliwych do przejścia ścieżkach).

## Kompilacja i uruchamianie programu
Program można skompilować przy użyciu pliku Makefile, który zawiera reguły kompilacji oraz instrukcje łączenia plików w finalny plik wykonywalny. Aby skompilować program, wystarczy uruchomić komendę make w katalogu z plikiem Makefile.
Po skompilowaniu programu, należy przejść do katalogu exe i uruchomić program, podając nazwę pliku z labiryntem:

Dostępne parametry uruchamiania
- -f [nazwa_pliku.txt] – parametr obowiązkowy; określa plik wejściowy, który musi być poprawnie sformatowanym plikiem labiryntu.
- -o [nazwa_pliku.txt] – parametr opcjonalny; umożliwia zapisanie wyniku działania programu do wskazanego pliku (jeśli plik nie istnieje, zostanie utworzony).
- -h – parametr opcjonalny; wyświetla krótką pomoc dotyczącą obsługi programu.

## Przykładowe wywołania programu
```
 ./maze -f ../default_maps/10x10.txt -o last_test.txt
```
```
XXXXXXXXXXXXXXXXXXXXX
P           X     X X
XXX XXX XXX X XXX X X
X X X   X X   X X X X
X XXX XXX XXXXX X X X
X X   X       X   X X
X X XXX XXX X X XXX X
X   X X X   X X X   X
XXXXX X X XXX X X X X
X     X X X X X X X X
X XXXXX X X X X X X X
X X     X X   X   X X
X X XXXXX X XXXXXXX X
X   X   X X   X     X
X XXXXX X XXX X XXXXX
X X     X X   X   X X
X X X XXX XXXXXXX X X
X   X X   X     X   X
XXXXX X XXX XXX XXX X
X     X       X     K
XXXXXXXXXXXXXXXXXXXXX
```
```
FOWARD 11
TURNRIGHT
FOWARD 2
TURNLEFT
FOWARD 2
TURNLEFT
FOWARD 2
TURNRIGHT
FOWARD 4
TURNRIGHT
FOWARD 4
TURNRIGHT
FOWARD 2
TURNLEFT
FOWARD 6
TURNLEFT
FOWARD 2
TURNLEFT
FOWARD 4
TURNRIGHT
FOWARD 2
TURNRIGHT
FOWARD 6
TURNRIGHT
FOWARD 4
TURNLEFT
FOWARD 2
TURNLEFT
FOWARD 2
TURNRIGHT
FOWARD 2
TURNLEFT
FOWARD 2
TURNRIGHT
FOWARD 2
TURNLEFT
FOWARD 1
```


