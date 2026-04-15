# Repositório de Exercícios - C++

Este repositório contém uma série de exercícios focados em estruturas condicionais (`if`, `else`, `switch`) e operadores ternários desenvolvidos em C++.

---

## 1. Verificação de Número Positivo, Negativo ou Zero
Programa que recebe um número inteiro do usuário e verifica, usando estruturas condicionais simples, se ele é positivo, negativo ou igual a zero.

```cpp
#include <iostream>
using namespace std;

int main() {
    int numero;
    cout << "Digite um numero: ";
    cin >> numero;

    if (numero >= 1) {
        cout << "O numero esta positivo" << endl;
    }
    else if (numero < 0) {
        cout << "O numero esta negativo" << endl;
    }
    else {
        cout << "O numero é zero" << endl;
    }

    return 0;
}
```

---

## 2. Verificação de Intervalo (10 a 20)
Este código utiliza operadores lógicos (`&&`) para determinar se o valor inserido pelo usuário está estritamente dentro do intervalo entre 10 e 20.

```cpp
#include <iostream>
using namespace std;

int main () {
    int numero;
    cout << "Digite um numero: ";
    cin >> numero;

    if (numero >= 10 && numero <= 20) {
        cout << "O numero esta no intervalo de 10 a 20" << endl;
    } else {
        cout << "O numero esta fora do intervalo de 10 a 20" << endl;
    }
    
    return 0;
}
```

---

## 3. Dias da Semana com `switch case`
Conversor simples que recebe um número de 1 a 7 e imprime o dia da semana correspondente. Inclui tratamento de erro (default) para entradas inválidas.

```cpp
#include <iostream>
using namespace std;

int main() {
    int diaSemana;

    cout << "Digite o numero do dia da semana (1 a 7): ";
    cin >> diaSemana;

    switch (diaSemana) {
        case 1:
            cout << "Domingo" << endl;
            break;
        case 2:
            cout << "Segunda-feira" << endl;
            break;
        case 3:
            cout << "Terca-feira" << endl;
            break;
        case 4:
            cout << "Quarta-feira" << endl;
            break;
        case 5:
            cout << "Quinta-feira" << endl;
            break;
        case 6:
            cout << "Sexta-feira" << endl;
            break;
        case 7:
            cout << "Sabado" << endl;
            break;
        default:
            cout << "Numero de dia invalido." << endl;
    }

    return 0;
}
```

---

## 4. Par ou Ímpar (Operador Ternário)
Exemplo prático do uso de operador ternário (`? :`) em conjunto com o operador de módulo (`%`) para classificar um número como par ou ímpar em uma única linha de atribuição.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main () {
    int numero;

    cout << "Digite um numero: ";
    cin >> numero;

    string paridade = (numero % 2 == 0 ) ? "par" : "impar";

    cout << " O numero " << numero << " e " << paridade << endl;
    
    return 0;
}
```

---

## 5. Validação de Nota e Aprovação (Condicionais Aninhadas)
Este programa valida primeiramente se a nota inserida é possível (entre 1 e 10). Se for válida, ele entra em um segundo bloco de validação para verificar se o aluno foi aprovado ou reprovado.

```cpp
#include <iostream>
using namespace std;

int main() {
    int nota;

    cout << "Digite sua nota: ";
    cin >> nota;

    if (nota >= 1 && nota <= 10) {
        if (nota <= 5) {
            cout << "Reprovado" << endl;
        } else {
            cout << "Aprovado" << endl;
        }
    } else {
        cout << "Numero digitado invalido." << endl;
    }

    return 0;
}
```

---

## 6. Aprovação de Nota (Operador Ternário)
Versão simplificada da verificação de aprovação utilizando o operador ternário para atribuir o status de forma direta à variável.

```cpp
#include <iostream>
#include <string>
using namespace std;

int main () {
    int nota;

    cout << "Digite sua nota: ";
    cin >> nota;

    string paridade = (nota >= 6 ) ? "aprovado" : "reprovado";

    cout << " Voce tirou " << nota << " foi " << paridade << endl;
    
    return 0;
}
```
