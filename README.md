# 🚦 Desafio Controle de Fluxo

Este projeto foi desenvolvido como parte dos exercícios de prática em Java, com foco no conteúdo de **Controle de Fluxo**.

## 🧠 Descrição do Desafio

O objetivo do programa é receber dois números inteiros via terminal e realizar uma contagem simples utilizando estrutura de repetição (`for`).

### ✔️ Regras:

- O programa deve ler **dois números inteiros** via entrada do usuário.
- O sistema deve imprimir uma contagem a partir de 1 até a diferença entre os dois números.
- Se o **primeiro número** for **maior que o segundo**, o programa deve lançar uma exceção personalizada chamada `ParametrosInvalidosException`.

---

## 💻 Exemplo de Execução

### Entrada:
Digite o primeiro parâmetro
12
Digite o segundo parâmetro
30

### Saída:
Imprimindo o número 1
Imprimindo o número 2
...
Imprimindo o número 18
---

## 📂 Estrutura do Projeto

DesafioControleFluxo/
├── Contador.java
└── ParametrosInvalidosException.java
---

## 📌 Código

### `ParametrosInvalidosException.java`

```java
public class ParametrosInvalidosException extends Exception {
    public ParametrosInvalidosException(String message) {
        super(message);
    }
}
Contador.java
import java.util.Scanner;

public class Contador {
    public static void main(String[] args) {
        Scanner terminal = new Scanner(System.in);
        System.out.println("Digite o primeiro parâmetro");
        int parametroUm = terminal.nextInt();

        System.out.println("Digite o segundo parâmetro");
        int parametroDois = terminal.nextInt();

        try {
            contar(parametroUm, parametroDois);
        } catch (ParametrosInvalidosException exception) {
            System.out.println("O segundo parâmetro deve ser maior que o primeiro");
        }

        terminal.close();
    }

    static void contar(int parametroUm, int parametroDois) throws ParametrosInvalidosException {
        if (parametroUm > parametroDois) {
            throw new ParametrosInvalidosException("O segundo parâmetro deve ser maior que o primeiro");
        }

        int contagem = parametroDois - parametroUm;
        for (int i = 1; i <= contagem; i++) {
            System.out.println("Imprimindo o número " + i);
        }
    }
}
🚀 Tecnologias Utilizadas
Java 17+

IDE: IntelliJ IDEA / Eclipse / VSCode

Terminal de comando

## 🏁 Como Executar
Clone o repositório:

git clone https://github.com/seu-usuario/DesafioControleFluxo.git
Compile e execute a classe Contador:

javac Contador.java ParametrosInvalidosException.java
java Contador


## 📚 Conceitos Aplicados
Estrutura de repetição for

Leitura de entrada com Scanner

Criação de exceções personalizadas em Java

Encapsulamento de lógica em métodos

📝 Autor
Desenvolvido por Manu Moreira ✨
