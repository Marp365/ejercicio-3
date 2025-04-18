#include <iostream>
using namespace std;

int main() {
    int arreglo[10];

    for (int i = 0; i < 10; i++) {
        cout << "Ingrese el número " << i + 1 << ": ";
        cin >> arreglo[i];
    }

    int ultimo = arreglo[9];
    for (int i = 9; i > 0; i--) {
        arreglo[i] = arreglo[i - 1];
    }
    arreglo[0] = ultimo;

    cout << "Arreglo rotado: ";
    for (int i = 0; i < 10; i++) {
        cout << arreglo[i] << " ";
    }
    cout << endl;

    return 0;
}
