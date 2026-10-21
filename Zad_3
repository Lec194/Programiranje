#include <iostream>
#include <cmath>
using namespace std;

double udaljenost(double x1, double y1, double x2, double y2) {
    double dx = x2 - x1;
    double dy = y2 - y1;
    return sqrt(dx * dx + dy * dy);
}

void ispisiUdaljenost(double r) {
    cout << "Udaljenost izmedu tocaka: " << r << endl;
}

int main() {
    double x1, y1, x2, y2;
    cout << "Unesi koordinate prve tocke (x1 y1): ";
    cin >> x1 >> y1;
    cout << "Unesi koordinate druge tocke (x2 y2): ";
    cin >> x2 >> y2;

    double d = udaljenost(x1, y1, x2, y2);
    ispisiUdaljenost(d);

    return 0;
}
