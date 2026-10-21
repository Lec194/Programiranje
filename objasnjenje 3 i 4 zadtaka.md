OBJAŠNJENJE KODA:

Uključivanje biblioteka:

#include : Omogućuje unos podataka s tipkovnice (cin) i ispis na ekran (cout).

#include : Uključuje matematičku biblioteku u kojoj se nalazi funkcija sqrt() za računanje kvadratnog korijena.

using namespace std;: Omogućuje izravno pisanje cout i cin bez prefiksa std::.

Funkcija za računanje udaljenosti:

double udaljenost(double x1, double y1, double x2, double y2): Funkcija prima 4 decimalna broja (koordinate dviju točaka) i vraća izračunatu udaljenost ako double.

double dx = x2 - x1; i double dy = y2 - y1;: Računaju razliku po X i Y osi.

return sqrt(dx * dx + dy * dy);: Množi dx i dy same sa sobom (dx^2 i dy^2), zbraja ih i izvlači kvadratni korijen pomoću sqrt(). Rezultat vraća u main.

Funkcija za ispis:

void ispisiUdaljenost(double rez): Tip void označava da funkcija ne vraća vrijednost (nema return), već samo prima izračunatu vrijednost u parametar rez i ispisuje je na ekran.

Glavni program (main):

int main(): Glavna funkcija od koje počinje izvršavanje programa.

double x1, y1, x2, y2;: Deklarira 4 decimalne varijable za koordinate.

cin >> x1 >> y1; i cin >> x2 >> y2;: Učitavaju koordinate s tipkovnice.

double d = udaljenost(x1, y1, x2, y2);: Poziva funkciju udaljenost s unesenim koordinatama i sprema rezultat u varijablu d.

ispisiUdaljenost(d);: Šalje varijablu d funkciji za ispis.

return 0;: Signalizira uspješan završetak programa.



Zad4
OBJAŠNJENJE KODA:

Uključivanje biblioteka:

#include : Omogućuje unos podataka (cin) i ispis (cout).

using namespace std;: Omogućuje izravno korištenje standardnih funkcija bez prefiksa std::.

Funkcija za provjeru ispravnosti unosa:

bool ispravanUnos(int b, int m): Vraća logičku vrijednost (true ili false).

return m > 0 && b >= 0 && b <= m;: Provjerava je li maksimalan broj bodova veći od 0 te jesu li ostvareni bodovi između 0 i maksimuma.

Funkcija za izračun postotka:

double izracunajPostotak(int b, int m): Vraća postotak kao decimalni broj.

return 100.0 * b / m;: Množi bodove s 100.0 (kako bi dijeljenje bilo decimalno, a ne cjelobrojno) i dijeli s maksimumom.

Funkcija za određivanje ocjene:

int odrediOcjenu(double p): Vraća cjelobrojnu ocjenu (1-5) na temelju postotka p.

Redom provjerava pragove (<50, <65, <80, <90). Ako nijedan uvjet nije ispunjen, automatski vraća 5.

Funkcija za ispis izvještaja:

void ispisiIzvjestaj(int b, int m, double p, int o): Funkcija koja ne vraća vrijednost (void), već prima sve podatke i ispisuje ih u više redaka koristeći \n.

Glavni program (main):

int main(): Početak programa.

int b, m;: Deklaracija varijabli za bodove i maksimum.

if (!ispravanUnos(b, m)): Ako unos nije ispravan, ispisuje grešku i prekida program s return 0.

double p = izracunajPostotak(b, m);: Računa postotak ako je unos ispravan.

ispisiIzvjestaj(b, m, p, odrediOcjenu(p));: Poziva funkciju za ispis i direktno unutar nje šalje rezultat funkcije odrediOcjenu(p).

return 0;: Signalizira uspješan završetak programa.
