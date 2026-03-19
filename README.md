ala ma kota kot ma ale

Merge nie był fast forwart bo zmodyfikowalismy galaz dodajac plik README po tym jak utworzylismy galaz
feature - max

Zaczynamy testowac rebase
Odpowiedzi na pytania końcowe:

1. Kiedy Git wykona fast-forward, a kiedy powstaje merge commit?
Fast-forward dzieje się wtedy, kiedy na głównej gałęzi (main) nic się nie zmieniło
 od czasu, gdy stworzyliśmy naszą nową gałąź. Git po prostu "przewija" wskaźnik do
 przodu i nie robi dodatkowego commita.
Z kolei klasyczny merge commit powstaje, kiedy na obu gałęziach
 robiliśmy niezależne zmiany i historie się rozjechały. Git musi wtedy zrobić osobny
 commit scalający, żeby to wszystko połączyć, przez co na grafie historii robi się
 takie charakterystyczne "oczko".

2. Czym w praktyce różni się merge od rebase?
Merge po prostu łączy gałęzie, zostawiając w historii ślad po tym,
 jak dokładnie przebiegała praca – widać wszystkie odgałęzienia i 
powstaje nowy commit złączenia.
Za to rebase działa tak, że bierze nasze commity z nowej gałęzi i 
sztucznie doczepia je na samej górze docelowej gałęzi. Dzięki temu
 cała historia na grafie układa się w jedną prostą linię, co dużo 
łatwiej się czyta.

3. W jaki sposób został rozwiązany konflikt w Twoim repozytorium?
Konflikt wywaliło mi w pliku Program.cs, bo celowo zmieniłem pierwszą
 linijkę kodu na gałęzi main i dokładnie w tym samym miejscu na gałęzi
 feature-conflict. Żeby to naprawić, wszedłem ręcznie do tego pliku w 
Notatniku. Usunałem znaczniki i strzałki (<<<<<<<, =======, >>>>>>>),
 które wrzucił tam Git, i zostawiłem tylko właściwą wersję kodu. Na koniec
 zapisałem plik i puściłem commita scalającego, co rozwiązało sprawę.
 poprawny fragment kodu, zapisałem plik i zatwierdziłem rozwiązanie nowym commitem scalającym.