# Baza wiedzy 1.1-1.5
owoc(jablko).
owoc(gruszka).
owoc(sliwka).
kolor(jablko,czerwony).
kolor(gruszka,zielony).
kolor(sliwka,fioletowy).
## L1.Cw1.1 PODSTAWOWE. Napisz zapytanie zwracające kolor gruszki w zmiennej Kolor.
kolor(gruszka, Opis).
## L1.Cw1.2 PODSTAWOWE. Znajdź produkt o kolorze czerwonym, nie wpisując jego nazwy.
kolor(Opis,czerwony).
## L1.Cw1.3 DODATKOWE. Sprawdź owoc(banan)., a następnie dopisz fakt owoc(banan). przy innych faktach owoc/1. Porównaj wyniki.
owoc(banan). → false, a po dodaniu faktu → true.
## L1.Cw1.4 DODATKOWE. Uruchom kolor(_,niebieski). Czy wynik mówi cokolwiek pewnego o wszystkich owocach w rzeczywistości?
kolor(_,niebieski). - false; brak dowodu nie znaczy że nie istnieje.
## L1.Cw1.5 DODATKOWE. Porównaj kolor(gruszka,x). i kolor(gruszka,X). Wyjaśnij różnicę między x i X.
kolor(gruszka,x). - false; kolor(gruszka,X). - X = zielony. x nie= X
# Baza danych 2.1-2.5
posiada(anna,ksiazka(hobbit,tolkien)).
posiada(marek,ksiazka(diuna,herbert)).
posiada(anna,ksiazka(solaris,lem)).
## L1.Cw2.1 PODSTAWOWE. Wypisz tytuły książek Anny, ignorując ich autorów.
posiada(anna,ksiazka(Tytul,_)).
## L1.Cw2.2 PODSTAWOWE. Znajdź autora książki diuna bez podawania właściciela.
posiada(_,ksiazka(diuna,Autor)).
## L1.Cw2.3 DODATKOWE. Uzgodnij odczyt(dzwonek,K,glosny) = odczyt(dzwonek,sluch,P). Podaj K i P.
(dzwonek,K,glosny) = (dzwonek,sluch,P). - K = sluch, P = glosny.
## L1.Cw2.4 DODATKOWE. Sprawdź, czy odczyt(lampa,wzrok,jasny) można zunifikować z odczyt(_,sluch,_). Wyjaśnij wynik.
odczyt(lampa,wzrok,jasny) = odczyt(_,sluch,_).  - false, ponieważ wzrok i sluch to co innego.
## L1.Cw2.5 DODATKOWE. Uruchom osobno para(X,X) = para(ania,marek). oraz para(X,X) = para(ania,ania). Kiedy unifikacja jest możliwa?
Pierwsze - false; drugie - X = ania.
