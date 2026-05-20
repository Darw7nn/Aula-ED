markdown_content = """# Sistema de Gerenciamento de Fila de Atendimento (C++)

Este documento contém a implementação de um sistema de fila simples e uma fila com prioridade para idosos (idade > 60), utilizando a linguagem C++ e a biblioteca Standard Template Library (STL).

## Código Fonte

```cpp
#include <iostream>
#include <list>

using namespace std;

// Classe que representa uma Pessoa no sistema
class Pessoa {
public:
    string nome;
    int idade;

    Pessoa(string n, int i) {
        nome = n;
        idade = i;
    }
};

// Classe que gerencia a Fila de Atendimento
class Fila {
private:
    list<Pessoa> fila;

public:
    // Enfileiramento padrão (FIFO - First In, First Out)
    void enfileirar(string nome, int idade) {
        fila.push_back(Pessoa(nome, idade));
    }

    // Enfileiramento com regra de prioridade para maiores de 60 anos
    void enfileirarPrioridade(string nome, int idade) {
        Pessoa novaPessoa(nome, idade);
        if (idade > 60) {
            auto it = fila.begin();
            // Procura a posição correta: após os idosos já existentes
            while (it != fila.end() && it->idade > 60) {
                ++it;
            }
            fila.insert(it, novaPessoa);
        } else {
            // Se não for idoso, vai para o final da fila comum
            fila.push_back(novaPessoa);
        }
    }

    // Remove e atende a primeira pessoa da fila
    void desenfileirar() {
        if (fila.empty()) {
            cout << "Fila vazia!" << endl;
            return;
        }
        cout << "Atendendo: " << fila.front().nome << endl;
        fila.pop_front();
    }

    // Exibe todos os integrantes da fila no console
    void mostrarFila() {
        if (fila.empty()) {
            cout << "Fila vazia!" << endl;
            return;
        }
        cout << "\\nFila de atendimento:\\n";
        for (auto pessoa : fila) {
            cout << pessoa.nome
                 << " - Idade: "
                 << pessoa.idade << endl;
        }
    }
};

int main() {
    // --- TESTE 1: FILA NORMAL ---
    cout << "===== FILA SEM REGRA =====\\n";
    Fila filaNormal;

    filaNormal.enfileirar("Esnupi", 25);
    filaNormal.enfileirar("Charli", 40);
    filaNormal.enfileirar("Brow", 72);
    filaNormal.enfileirar("Ana", 33);
    filaNormal.enfileirar("Paulo", 65);
    filaNormal.enfileirar("Mina", 18);
    filaNormal.enfileirar("Fernanda", 55);
    filaNormal.enfileirar("Robertinho", 80);
    filaNormal.enfileirar("Hana", 29);
    filaNormal.enfileirar("Patricia", 45);
    filaNormal.enfileirar("Marquinho", 61);
    filaNormal.enfileirar("Maria", 37);
    filaNormal.enfileirar("Mavelyn", 20);
    filaNormal.enfileirar("Cesar", 50);
    filaNormal.enfileirar("Marcelle", 27);

    filaNormal.mostrarFila();
    cout << "\\nDesenfileirando...\\n";
    filaNormal.desenfileirar();
    filaNormal.mostrarFila();

    // --- TESTE 2: FILA COM PRIORIDADE ---
    cout << "\\n\\n===== FILA COM PRIORIDADE =====\\n";
    Fila filaPrioridade;

    filaPrioridade.enfileirarPrioridade("Ana", 25);
    filaPrioridade.enfileirarPrioridade("Carlos", 40);
    filaPrioridade.enfileirarPrioridade("Maria", 72);
    filaPrioridade.enfileirarPrioridade("Pedro", 33);
    filaPrioridade.enfileirarPrioridade("Lucia", 65);
    filaPrioridade.enfileirarPrioridade("Joao", 18);
    filaPrioridade.enfileirarPrioridade("Fernanda", 55);
    filaPrioridade.enfileirarPrioridade("Roberto", 80);
    filaPrioridade.enfileirarPrioridade("Julia", 29);
    filaPrioridade.enfileirarPrioridade("Patricia", 45);
    filaPrioridade.enfileirarPrioridade("Marcos", 61);
    filaPrioridade.enfileirarPrioridade("Paulo", 37);
    filaPrioridade.enfileirarPrioridade("Bianca", 20);
    filaPrioridade.enfileirarPrioridade("Ricardo", 50);
    filaPrioridade.enfileirarPrioridade("Clara", 27);

    filaPrioridade.mostrarFila();

    cout << "\\nDesenfileirando...\\n";
    filaPrioridade.desenfileirar();
    filaPrioridade.mostrarFila();

    return 0;
}
