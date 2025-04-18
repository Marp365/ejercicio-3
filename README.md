Escribe un programa que permita al usuario ingresar 10 números enteros en un arreglo. Luego, rota los elementos una posición hacia la derecha, de modo que el último pase a ser el primero, y muestra el resultado.

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
