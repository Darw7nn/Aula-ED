# 💻 Desafios de Programação: Manipulação de Listas em C++

**Instituição:** FATEC  
**Curso:** Análise e Desenvolvimento de Sistemas (ADS) - 3º Semestre  
**Disciplina:** [Nome da Disciplina]  
**Autor:** [Seu Nome]  

---

## 📌 Sobre o Repositório
Este repositório contém a resolução de três desafios práticos em **C++**, focados no uso e manipulação da estrutura de dados `std::list` (listas duplamente encadeadas). O objetivo é demonstrar conceitos fundamentais como inserção, iteração, inversão e ordenação de dados.

---

## 🚀 Desafio 1: Soma e Multiplicação de Elementos
**Objetivo:** Criar uma lista com 5 números inteiros e calcular a soma e a multiplicação de todos os elementos da lista.

```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {
    list<int> minhaLista;

    minhaLista.push_back(2);
    minhaLista.push_back(3);
    minhaLista.push_back(4);
    minhaLista.push_back(5);
    minhaLista.push_back(6);

    int soma = 0;          
    int multiplicacao = 1; 

    for(int numero : minhaLista) {
        soma = soma + numero;               
        multiplicacao = multiplicacao * numero; 
    }

    cout << "A soma de tudo deu: " << soma << endl;
    cout << "A multiplicacao de tudo deu: " << multiplicacao << endl;

    return 0;
}
```

---

## 🚀 Desafio 2: Invertendo uma Lista de Strings
**Objetivo:** Criar uma lista de 5 elementos do tipo `string` e apresentar a ordem dos elementos de forma invertida utilizando os métodos nativos da estrutura.

```cpp
#include <iostream>
#include <list>
#include <string> 

using namespace std;

int main() {
    list<string> palavras;

    palavras.push_back("Primeiro");
    palavras.push_back("Segundo");
    palavras.push_back("Terceiro");
    palavras.push_back("Quarto");
    palavras.push_back("Quinto");

    cout << "Lista na ordem normal:" << endl;
    for(string palavra : palavras) {
        cout << palavra << " ";
    }
    cout << endl << endl;

    palavras.reverse(); 

    cout << "Lista na ordem invertida:" << endl;
    for(string palavra : palavras) {
        cout << palavra << " ";
    }
    cout << endl;

    return 0;
}
```

---

## 🚀 Desafio 3: Combinando e Ordenando Listas
**Objetivo:** Criar duas listas (A e B) de 5 elementos de números inteiros, combiná-las em uma única lista C e ordená-la em ordem crescente.

```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {
    list<int> listaA;
    list<int> listaB;
    list<int> listaC; 

    listaA.push_back(10);
    listaA.push_back(3);
    listaA.push_back(7);
    listaA.push_back(1);
    listaA.push_back(5);

    listaB.push_back(8);
    listaB.push_back(2);
    listaB.push_back(6);
    listaB.push_back(9);
    listaB.push_back(4);

    for(int numero : listaA) {
        listaC.push_back(numero);
    }

    for(int numero : listaB) {
        listaC.push_back(numero);
    }

    listaC.sort();

    cout << "A lista C combinada e ordenada fica assim:" << endl;
    for(int numero : listaC) {
        cout << numero << " ";
    }
    cout << endl;

    return 0;
}
```
