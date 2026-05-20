```cpp
// 1. CONTAGEM REGRESSIVA RECURSIVA
#include <iostream>
using namespace std;
void regressiva (int i) {
    cout << i << endl;
    if (i <= 0) {
        return;
    }
    else{
        regressiva ( i - 1);
    }
}
int main (){
    regressiva (10);
    return 0;
}

// ---------------------------------------------------------
// 2. IMPRESSÃO DE SEQUÊNCIA
#include <iostream>
using namespace std;

void imprimir_sequencia (int n) {
    if (n == 0) {
        return;
    }
    else{
        cout << n << endl;
        imprimir_sequencia (n - 1);
    }
}
int main (){
    imprimir_sequencia (5);
    return 0;
}

// ---------------------------------------------------------
// 3. REPETIÇÃO SIMPLES (FOR)
#include <iostream>
using namespace std;

int main () {
    for (int i = 0; i < 5; i++) {
        cout << "recursao" << endl;
    }
    return 0;
}

// ---------------------------------------------------------
// 4. IMPRESSÃO RECURSIVA (STRING)
#include <iostream>
using namespace std;

void imprimir_recursivamente(int n) {
    if (n == 0){
        return;
    } else {
        cout << "recursao" << endl;
        imprimir_recursivamente(n - 1);
    }
}

int main () {
    imprimir_recursivamente(5);
    return 0;
}

// ---------------------------------------------------------
// 5. SOMA ITERATIVA (FOR)
#include <iostream>
using namespace std;

int soma_for (int n) {
    int soma = 0;
    for (int i = 0; i <=n; i++) {
        soma+= i;
    }
    return soma;
}

int main () {
    cout << soma_for(5) << endl;
    return 0;
}
