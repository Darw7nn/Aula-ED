# Aula: Estruturas de Repetição em C++ (O Laço `for`)

Estruturas de repetição são o coração da automação em qualquer software. Construir uma base de lógica sólida em C++ agora no 3º semestre de Análise e Desenvolvimento de Sistemas vai te dar muita vantagem técnica, tanto para organizar os repositórios dos projetos da faculdade quanto para se destacar nas vagas da área de tecnologia.

Hoje, vamos focar em como fazer o computador trabalhar para você, repetindo tarefas automaticamente.

---

## O que são Estruturas de Repetição?

Na programação, muitas vezes precisamos executar uma mesma ação várias vezes. Em vez de escrevermos a mesma linha de código 10, 100 ou 1000 vezes, usamos os "laços" (ou *loops*). Eles avaliam uma condição e continuam executando um bloco de código até que essa condição deixe de ser verdadeira.

A estrutura mais comum e amigável para quando sabemos exatamente quantas vezes queremos repetir algo é o **`for`**.

## Dissecando o Laço `for`

O `for` em C++ é composto por três partes principais dentro dos parênteses, separadas por ponto e vírgula (`;`):

1. **Inicialização:** Onde criamos e damos um valor inicial à nossa variável de controle (geralmente chamada de `i`, `j`, `k`). Isso acontece apenas uma vez no início.
2. **Condição:** A regra que determina se o laço deve continuar. Enquanto for verdadeira (`true`), o código dentro do bloco `{}` será executado.
3. **Incremento/Decremento:** O que acontece com a variável de controle após cada volta do laço (ex: soma 1, subtrai 1).

## Exemplo Prático

Vamos analisar o código da nossa aula. Ele é um excelente exemplo de um laço simples e direto:

```cpp
#include <iostream>
using namespace std;

int main(){
	for (int i = 1; i <=5 ; ++i){
		cout << i << " ";
	}
}
```

### O que está acontecendo passo a passo?

* **`int i = 1`**: O laço começa criando uma variável inteira `i` valendo 1.
* **`i <= 5`**: O C++ se pergunta: "1 é menor ou igual a 5?". Sim. Então ele entra no laço.
* **`cout << i << " ";`**: O programa imprime o valor de `i` (que é 1) seguido de um espaço.
* **`++i`**: O laço termina sua primeira volta e incrementa `i` em 1. Agora `i` vale 2.
* **O ciclo se repete:** "2 é menor ou igual a 5?" Sim. Imprime 2. Incrementa para 3... e assim por diante.
* **O fim:** Quando `i` for incrementado para 6, a condição `6 <= 5` será falsa (`false`). O laço é interrompido imediatamente, e o programa segue seu curso (neste caso, finaliza).

**Saída esperada no terminal:**
`1 2 3 4 5 `
