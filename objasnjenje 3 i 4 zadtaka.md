1. zadtaka
  OBJAŠNJENJE KODA:

1. Uključivanje biblioteka:
- #include <iostream>: Omogućuje unos podataka s tipkovnice (cin) i ispis na ekran (cout).
- using namespace std;: Omogućuje pisanje cout i cin bez prefiksa std::.

2. Funkcije za matematičke operacije:
- double zbroji, oduzmi, pomnozi, podijeli: Četiri zasebne funkcije. Svaka prima dva decimalna broja (a i b) i vraća izračunatu vrijednost u main preko naredbe return.

3. Funkcija za ispis:
- void ispisiRezultat(double rez): Tip void označava da funkcija ne vraća nikakvu vrijednost. Ona samo prima izračunati rezultat u parametar rez i prikazuje ga na ekranu.

4. Glavni program (main):
- int main(): Glavna funkcija od koje kreće izvršavanje programa.
- double a, b; char op;: Deklarira dva decimalna broja i jedan znak (char) u koji se sprema operator (+, -, *, /).
- cin >> a >> op >> b;: Učitava brojeve i operaciju od korisnika.
- if / else if grananje: Provjerava uneseni znak. Ovisno o znaku, poziva odgovarajuću funkciju i prosljeđuje rezultat funkciji za ispis.
- Provjera dijeljenja s nulom: Kod operacije '/' provjerava se je li drugi broj različit od nule (b != 0) kako bi se spriječila matematička greška.

  2. zadtaka

  OBJAŠNJENJE KODA:

1. Funkcija za parnost (jeParan):
- bool jeParan(int broj): Vraća logičku vrijednost (true ili false).
- return broj % 2 == 0;: Operator % računa ostatak pri dijeljenju s 2. Ako je ostatak 0, broj je paran i funkcija vraća true.

2. Funkcija za znak (provjeriZnak):
- int provjeriZnak(int broj): Vraća cijeli broj: 1 za pozitivan, -1 za negativan i 0 za nulu.

3. Funkcija za ispis (ispisiAnalizu):
- void ispisiAnalizu(bool paran, int znak): Ne vraća vrijednost (void). Prima rezultate analiza i ispisuje tekstualne poruke na temelju uvjeta (if/else).

4. Glavni program (main):
- int n;: Stvara varijablu za unos cijelog broja.
- cin >> n;: Učitava broj s tipkovnice.
- bool paran = jeParan(n); i int znak = provjeriZnak(n);: Poziva funkcije, analizira broj i sprema rezultate u lokalne varijable.
- ispisiAnalizu(paran, znak);: Poziva void funkciju za prikaz rezultata korisniku.

  3. zadatak OBJAŠNJENJE KODA:

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


zad 5 1. Funkcija za provjeru unosa (ispravanUnos):
- bool ispravanUnos(double cijena, double popust): Vraća true ako je cijena veća od 0 te ako je popust u rasponu od 0 do 100%.

2. Funkcije za izračun (izracunajUstedeturu i izracunajKonacnuCijenu):
- izracunajUstedeturu: Računa koliko novca se uštedjelo množenjem cijene s postotkom (popust / 100.0) i vraća iznos uštede.
- izracunajKonacnuCijenu: Oduzima izračunatu uštedu od početne cijene i vraća konačni iznos za plaćanje.

3. Funkcija za ispis (ispisiRacun):
- void ispisiRacun(...): Prima početnu cijenu, uštedu i konačnu cijenu te ih ispisuje na ekran u tri reda.

4. Glavni program (main):
- cin >> cijena >> popust;: Učitava ulazne podatke od korisnika.
- if (!ispravanUnos(...)): Ako su uneseni negativni brojevi ili nevažeći popust, ispisuje grešku i prekida izvršavanje.
- Poziv funkcija: Izračunava uštedu i konačnu cijenu te prosljeđuje rezultate void funkciji za ispis.
