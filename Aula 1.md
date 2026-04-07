#include <iostream>
using namespace std;

int main() {
    int i, vet[6], menor, maior;
    
    for (i = 0; i < 6; i++) {
        cout << "Digite um num: ";
        cin >> vet[i];
    }
    
    menor = vet[0];
    maior = vet[0];
    
    for (i = 0; i < 6; i++) {
        if (vet[i] < menor) {
            menor = vet[i];
        }
        if (vet[i] > maior) {
            maior = vet[i];
        }
    }
    
    cout << "\n--- Resultados ---" << endl;
    cout << "Menor numero do vetor: " << menor << endl;
    cout << "Maior numero do vetor: " << maior << endl;
    
    return 0;
}
