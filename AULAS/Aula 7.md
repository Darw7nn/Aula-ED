# Aula 07 - Programação Orientada a Objetos (POO) em C++

```cpp
#include <iostream>
#include <string>

using namespace std;

// ==========================================
// REVISÃO DE FUNÇÕES
// ==========================================

void imprimirMensagem() {
    cout << "Olá, Mundo!" << endl;
}

void dobrarPorReferencia(int &numero) {
    numero *= 2;
}

void lerEntradaUsuario(int &valor) {
    cout << "Digite um número: ";
    cin >> valor;
}

int soma(int a, int b) {
    return a + b;
}

double calcularMedia(double numero1, double numero2) {
    return (numero1 + numero2) / 2.0;
}

bool ehPar(int numero) {
    return numero % 2 == 0;
}

// ==========================================
// DESAFIO 1: CLASSE PESSOA (COM CPF E RG)
// ==========================================

class Pessoa {
private:
    string nome;
    int idade;
    string endereco;
    string profissao;
    string cpf;
    string rg;

public:
    Pessoa(string nome, int idade, string endereco, string profissao, string cpf, string rg) {
        this->nome = nome;
        this->idade = idade;
        this->endereco = endereco;
        this->profissao = profissao;
        this->cpf = cpf;
        this->rg = rg;
    }

    void setNome(string novoNome) { nome = novoNome; }
    string getNome() { return nome; }

    void setIdade(int novaIdade) { idade = novaIdade; }
    int getIdade() { return idade; }

    void setEndereco(string novoEndereco) { endereco = novoEndereco; }
    string getEndereco() { return endereco; }

    void setProfissao(string novaProfissao) { profissao = novaProfissao; }
    string getProfissao() { return profissao; }

    void setCpf(string novoCpf) { cpf = novoCpf; }
    string getCpf() { return cpf; }

    void setRg(string novoRg) { rg = novoRg; }
    string getRg() { return rg; }

    void mostrarInfo() {
        cout << "##" << endl;
        cout << "Nome: " << nome << endl;
        cout << "Idade: " << idade << " anos" << endl;
        cout << "Endereço: " << endereco << endl;
        cout << "Profissão: " << profissao << endl;
        cout << "CPF: " << cpf << endl;
        cout << "RG: " << rg << endl;
    }
};

// ==========================================
// DESAFIO 2: CLASSE CARRO
// ==========================================

class Carro {
private:
    string marca;
    string modelo;
    string cor;
    int ano;

public:
    Carro(string marca, string modelo, string cor, int ano) {
        this->marca = marca;
        this->modelo = modelo;
        this->cor = cor;
        this->ano = ano;
    }

    void setMarca(string novaMarca) { marca = novaMarca; }
    string getMarca() { return marca; }

    void setModelo(string novoModelo) { modelo = novoModelo; }
    string getModelo() { return modelo; }

    void setCor(string novaCor) { cor = novaCor; }
    string getCor() { return cor; }

    void setAno(int novoAno) { ano = novoAno; }
    int getAno() { return ano; }

    void mostrarInfoCarro() {
        cout << "\n## Informações do Veículo ##" << endl;
        cout << "Marca: " << marca << endl;
        cout << "Modelo: " << modelo << endl;
        cout << "Cor: " << cor << endl;
        cout << "Ano: " << ano << endl;
    }

    void acelerar() {
        cout << "O " << modelo << " está acelerando! Vrummm!" << endl;
    }
};

// ==========================================
// EXECUÇÃO PRINCIPAL (MAIN)
// ==========================================

int main() {
    // Testes Iniciais (Funções)
    imprimirMensagem();
    
    // Teste Desafio 1 (Pessoa)
    Pessoa pessoa1("João", 30, "Rua Principal, 123", "Engenheiro", "111.222.333-44", "12.345.678-9");
    pessoa1.mostrarInfo();

    pessoa1.setNome("Maria");
    pessoa1.setIdade(25);
    pessoa1.setEndereco("Avenida Secundária, 456");
    pessoa1.setProfissao("Médica");
    pessoa1.setCpf("999.888.777-66");
    pessoa1.setRg("98.765.432-1");
    pessoa1.mostrarInfo();

    // Teste Desafio 2 (Carro)
    Carro carro1("Mitsubishi", "Lancer Evolution", "Amarelo", 2012);
    carro1.mostrarInfoCarro();
    carro1.acelerar();

    return 0;
}
