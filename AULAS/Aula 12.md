#include <iostream>
#include <list>

using namespace std;

class Fila {
public:
    Fila() {}

    // Adiciona um elemento ao final da fila
    void enfileirar(int elemento) {
        lista.push_back(elemento);
    }

    // Remove o elemento do início da fila e o retorna
    int desenfileirar() {
        if (lista.empty()) {
            return -1; // Retorna -1 se a fila estiver vazia
        }

        int elemento = lista.front();
        lista.pop_front();
        return elemento;
    }

    // Verifica se a fila está vazia
    bool vazia() {
        return lista.empty();
    }

    // Percorre a lista e exibe todos os elementos
    void mostrarElementoFila() {
        for (auto i : lista) {
            cout << "Elemento: " << i << endl;
        }
    }

private:
    list<int> lista;
};

int main() {
    Fila fila;

    fila.enfileirar(1);
    fila.enfileirar(2);
    fila.enfileirar(3);
    
    // Remove o primeiro elemento (o número 1)
    fila.desenfileirar();

    // Deve mostrar apenas os elementos 2 e 3
    fila.mostrarElementoFila();

    return 0;
}




# Experimentos com Estruturas de Dados em C++ (Fila/Queue)

Este repositório contém diferentes implementações de filas utilizando `std::list`, explorando desde conceitos básicos até lógica de prioridade e processamento de strings.

---

## 1. Sistema de Pagamento de Aposentadoria (Processamento de Nomes)
Este código simula uma fila de espera para pagamentos. Ele demonstra como enfileirar nomes, processar a saída (pagamento realizado) e verificar o estado da fila.

```cpp
#include <iostream>
#include <list>
#include <string> 

using namespace std;

class Fila {
public:
    Fila() {}

    void enfileirar(string nome) {
        lista.push_back(nome);
        cout << nome << " entrou na fila." << endl;
    }

    string desenfileirar() {
        if (lista.empty()) {
            return "Erro: Fila Vazia";
        }

        string nome = lista.front();
        lista.pop_front();
        return nome;
    }

    bool vazia() {
        return lista.empty();
    }

    void mostrarElementoFila() {
        if (lista.empty()) {
            cout << "A fila está atualmente VAZIA." << endl;
            return;
        }

        cout << "\n--- Pessoas na Fila Atual ---" << endl;
        for (auto nome : lista) {
            cout << "Aguardando: " << nome << endl;
        }
        cout << "-----------------------------\n" << endl;
    }

private:
    list<string> lista;
};

int main() {
    Fila aposentadoria;

    cout << "PROCESSANDO PAGAMENTOS" << endl;
    aposentadoria.enfileirar("Joao");
    aposentadoria.enfileirar("Jose");
    aposentadoria.enfileirar("Maria");
    aposentadoria.enfileirar("Luiza");
    aposentadoria.enfileirar("Fatima");

    cout << "\nRemovendo quem ja recebeu..." << endl;
    for(int i = 0; i < 5; i++) {
        string saiu = aposentadoria.desenfileirar();
        cout << saiu << " recebeu o dinheiro e saiu." << endl;
    }

    aposentadoria.mostrarElementoFila();

    cout << "NOVAS CHEGADAS" << endl;
    aposentadoria.enfileirar("Pedro");
    aposentadoria.enfileirar("Eulalia");
    aposentadoria.enfileirar("Marcia");
    aposentadoria.enfileirar("Agenor");

    aposentadoria.mostrarElementoFila();

    return 0;
}

# Experimentos com Fila (Queue) em C++

Este repositório contém quatro implementações práticas de filas utilizando a biblioteca `std::list` em C++.

---

## 1. Fila Hospitalar (Regra de Prioridade 60+)

```cpp
#include <iostream>
#include <list>
#include <string>

using namespace std;

struct Paciente {
    string nome;
    int idade;
};

class FilaHospitalar {
private:
    list<Paciente> pacientes;

public:
    void enfileirar(string nome, int idade) {
        pacientes.push_back({nome, idade});
    }

    void aplicarPrioridade() {
        list<Paciente> prioritarios;
        list<Paciente> normais;
        for (const auto& p : pacientes) {
            if (p.idade >= 60) prioritarios.push_back(p);
            else normais.push_back(p);
        }
        pacientes.clear();
        pacientes.splice(pacientes.end(), prioritarios);
        pacientes.splice(pacientes.end(), normais);
    }

    void mostrarFila() {
        if (pacientes.empty()) return;
        for (const auto& p : pacientes) {
            cout << "[" << p.nome << " | " << p.idade << " anos] ";
        }
        cout << endl;
    }
};

int main() {
    FilaHospitalar hospital;
    hospital.enfileirar("Paciente 1", 20);
    hospital.enfileirar("Idoso A", 70);
    hospital.enfileirar("Paciente 2", 30);
    hospital.enfileirar("Idoso B", 65);
    hospital.mostrarFila();
    hospital.aplicarPrioridade();
    hospital.mostrarFila();
    return 0;
}
