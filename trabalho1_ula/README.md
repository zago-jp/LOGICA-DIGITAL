# 🧮 Trabalho 1 — ULA (Unidade Lógica e Aritmética)

## 📘 Descrição Geral
Este trabalho tem como objetivo desenvolver uma **ULA de 32 bits** no **Logisim Evolution**, capaz de realizar operações aritméticas e lógicas básicas.  
A ULA foi projetada para receber dois operandos de 16 bits (`A` e `B`) e um sinal de controle (`AluOp`) que define qual operação será executada.

---

## ⚙️ Funcionalidades Implementadas

| **AluOp** | **Mnemônico** | **Resultado** | **Descrição** |
|:----------:|:--------------|:---------------|:---------------|
| `0000` | `add` | A + B | Addition |
| `0010` | `sub` | A - B | Subtraction |
| `0100` | `and` | A and B | Bitwise AND |
| `0101` | `or`  | A or B | Bitwise OR |
| `0110` | `xor` | A xor B | Bitwise XOR |
| `0111` | `nor` | A nor B | Bitwise NOR |
| `1010` | `slt` | (A - B)[31] | Set on Less Than |
| **Outros** | — | Don’t Care | — |

---

## 🧩 Estrutura do Circuito
- **Entradas:**
  - `A` (32 bits)
  - `B` (32 bits)
  - `AluOp` (4 bits)

- **Saída:**
  - `Result` (32 bits)
  - `Zero` (1 bit) – indica se o resultado é igual a zero

---

## 🧠 Lógica do Projeto
- As operações lógicas (AND, OR, XOR, NOR) são realizadas bit a bit.
- As operações aritméticas (ADD, SUB) utilizam somadores e inversores para suportar subtração por complemento de dois.
- A operação `SLT` retorna `1` se `A < B`, caso contrário `0`.

---

## 🧰 Ferramentas Utilizadas
- **Logisim Evolution** (versão recomendada: 3.8.0 ou superior)
- **Sistema de simulação digital** com barramentos e multiplexadores para seleção de operação.

---

## 📂 Estrutura de Arquivos

