# Atividades de Programação em C++

Este repositório contém os exemplos de sala e os desafios resolvidos propostos na disciplina.

---

## 📌 Exemplos

### Exemplo 1: Passagem por Referência
```cpp
#include <iostream>
using namespace std;

void dobrarPorReferencia(int &numero){
    numero *=2;
}

int main (){
    int valor = 5;
    dobrarPorReferencia(valor);

    cout << "O valor dobrado é: " << valor << endl;

    return 0;
}
```

### Exemplo 2: Leitura de Entrada do Usuário
```cpp
#include <iostream>
using namespace std;

void lerEntradaUsuario(int &valor){
    cout << "Digite um numero: ";
    cin >> valor;
}

int main(){
    int numero;
    lerEntradaUsuario(numero);

    cout << "Voce digitou: " << numero << endl;

    return 0;
}
```

---

## 🚀 Desafios

### Desafio 1: Calculadora Básica (Funções)
```cpp
#include <iostream>
using namespace std;

int sub(int a, int b){
    int resultado = a - b;
    return resultado;
}
int divi(int a, int b){
    int resultado = a / b;
    return resultado;
}
int mult(int a, int b){
    int resultado = a * b;
    return resultado;
}

int soma(int a, int b){
    int resultado = a + b;
    return resultado;
}

int main (){
    int x = 5;
    int y = 3;
    int resultadoSoma = soma (x,y);
    int resultadoMult = mult (x,y);
    int resultadoDivi = divi (x,y);
    int resultadoSub = sub (x,y);

    cout << " A soma de "<< x << " e " << y << " e: " << resultadoSoma << endl;
    cout << " A multiplicacao de "<< x << " e " << y << " e: " << resultadoMult << endl;
    cout << " A divicao de "<< x << " e " << y << " e: " << resultadoDivi << endl;
    cout << " A subtracao de "<< x << " e " << y << " e: " << resultadoSub << endl;

    return 0;
}
```

### Desafio 2: Calcular Média
```cpp
#include <iostream>
using namespace std;

double calcularMedia(double numero1, double numero2){
    double resultado = (numero1 + numero2)/2;
    return resultado;
}

int main (){
    double numero1 = 5.5;
    double numero2 = 7.0;

    double resultadoFinal = calcularMedia (numero1,numero2);

    cout << "A media de " << numero1 << " e " << numero2 << " e " << resultadoFinal << endl;

    return 0;
}
```

### Desafio 3: Verificar se o Número é Par
```cpp
#include <iostream>
using namespace std;

bool ehPar(int numero){
    
    return numero % 2 ==0 ;
}

int main(){
    int numero = 7;
    if(ehPar(numero)){
        cout << numero << " e um numero par." << endl;
    }else{
        cout << numero << " nao e um numero par"<< endl;
    }

    return 0;
}
```

### Desafio 4: Soma dos Elementos de um Vetor
```cpp
#include <iostream>
using namespace std;

int calcularSoma(int vetor[], int tamanho) {
    int soma = 0;

    for (int i = 0; i < tamanho; i++) {
        soma += vetor[i];
    }

    return soma;
}

int main() {

    int numeros[] = {10, 20, 30, 40, 50};
    int tamanhovetor = 5;

    int resultado = calcularSoma(numeros, tamanhovetor);

    cout << "A soma de todos os elementos do vetor e: " << resultado << endl;

    return 0;
}
```
