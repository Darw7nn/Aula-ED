# Coleção de Algoritmos em C++

Este repositório reúne exemplos práticos de manipulação de vetores, cálculos matemáticos e lógica de programação em C++.


```cpp
#include <iostream>
using namespace std;

int main() {
    int vetor[6];
    int maior, menor;

    cout << "Digite 6 numeros:" << endl;

    for(int i = 0; i < 6; i++) {
        cout << "Numero " << i + 1 << ": ";
        cin >> vetor[i];
    }

    maior = vetor[0];
    menor = vetor[0];

    for(int i = 1; i < 6; i++) {
        if(vetor[i] > maior) {
            maior = vetor[i];
        }
        if(vetor[i] < menor) {
            menor = vetor[i];
        }
    }

    cout << "Maior numero: " << maior << endl;
    cout << "Menor numero: " << menor << endl;

    return 0;
}



#include <iostream>
using namespace std;

int main() {
    int numero;
    cout << "Digite um numero inteiro positivo: ";
    cin >> numero;

    int contador = 0;
    int temp = numero;

    while (temp > 0) {
        temp = temp / 10;
        contador++;
    }

    cout << "O numero " << numero << " possui " << contador << " digitos." << endl;

    return 0;
}





#include <iostream>
using namespace std;

int main() {
    const int size = 5;
    int num[size] = {2, 4, 6, 8, 10};

    int sum = 0;
    for (int i = 0; i < size; ++i) {
        sum += num[i];
    }

    cout << "Soma dos elementos: " << sum << endl;

    return 0;
}


#include <iostream>
using namespace std;

int main() {
    int vetor[5];
    int soma = 0;
    float media;

    cout << "Digite 5 numeros:" << endl;

    for(int i = 0; i < 5; i++) {
        cout << "Numero " << i + 1 << ": ";
        cin >> vetor[i];
        soma += vetor[i];
    }

    media = soma / 5.0;

    cout << "Soma dos elementos: " << soma << endl;
    cout << "Media dos elementos: " << media << endl;

    return 0;
}
