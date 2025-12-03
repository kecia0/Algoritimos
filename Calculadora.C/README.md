#  Calculadora Científica em C

![C](https://img.shields.io/badge/Language-C99-blue?style=flat-square&logo=c)
![Math](https://img.shields.io/badge/Lib-math.h-orange?style=flat-square)
![Build](https://img.shields.io/badge/Build-GCC-green?style=flat-square)

> **"Mais do que somar e subtrair: uma ferramenta completa para álgebra, trigonometria e cálculo matricial."**

## 📝 Sobre o Projeto
Este software é uma calculadora científica desenvolvida em **Linguagem C**, focada em modularidade e estruturação de dados. Diferente de calculadoras simples, este projeto implementa um **Histórico de Operações** persistente durante a execução e manipulação de **Matrizes**.

## 🚀 Funcionalidades

O sistema foi dividido em módulos de competência:

| Módulo | Operações Disponíveis |
| :--- | :--- |
| **🔢 Aritmética Básica** | `+` Adição, `-` Subtração, `*` Multiplicação, `/` Divisão |
| **📐 Trigonometria** | `sin` Seno, `cos` Cosseno (Entrada em Graus) |
| **🧪 Funções Avançadas** | `x!` Fatorial, `x^y` Potência, `sqrt` Raiz Quadrada, `ln` Logaritmo Natural |
| **🎲 Álgebra Linear** | Soma de Matrizes [2x2] |
| **💾 Memória** | Histórico das últimas 10 operações (Buffer Circular) |

---

## ⚙️ Destaques Técnicos

### 1. Histórico Inteligente (Structs)
Utilizei `typedef struct` para criar objetos de operação que armazenam não apenas o resultado, mas os operandos e o tipo da conta realizada.
```c
typedef struct {
    char tipo[50];
    double a, b;
    double resultado;
    int id;
} Operacao;
2. Validações de Segurança
🚫 Prevenção de divisão por zero.
🚫 Tratamento de raízes de números negativos.
🚫 Limite de overflow para cálculo de fatoriais (Max: 20).
💻 Como Compilar e Rodar
Como o projeto utiliza a biblioteca <math.h>, é necessário linkar o binário matemático ao compilar no Linux/MacOS.
code
Bash
# Compile o código
gcc main.c -o calculadora -lm

# Execute
./calculadora
<div align="center">
<sub>Desenvolvido para a disciplina de Algoritmos e Programação.</sub>
</div>
```
