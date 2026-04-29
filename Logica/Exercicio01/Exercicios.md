# Exercícios de Lógica de Programação — C# com .NET 10

Exercícios baseados no curso **C# COMPLETO — Programação Orientada a Objetos** (Nélio Alves, Udemy).

> **Pré-requisito:** conhecimento básico de entrada/saída, condicionais e laços em C#.  
> **Como criar um projeto:** `dotnet new console -n ExercicioXX && cd ExercicioXX && dotnet run`

---

## 🟢 Nível 1 — Entrada, Saída e Operadores

### Exercício 01 — Média de notas

Leia o nome de um aluno e suas 3 notas. Calcule a média aritmética e exiba a situação:

- Média ≥ 7 → **Aprovado**
- 5 ≤ média < 7 → **Recuperação**
- Média < 5 → **Reprovado**

### Exercício 02 — Conversor de temperatura

Leia uma temperatura em Celsius e exiba os equivalentes em Fahrenheit e Kelvin.

```
F = C * 9/5 + 32
K = C + 273.15
```

### Exercício 03 — Cálculo de salário

Leia o nome do funcionário, a quantidade de horas trabalhadas e o valor por hora. Exiba o salário bruto formatado em reais.

---

## 🟡 Nível 2 — Condicionais (`if/else`, `switch`)

### Exercício 04 — Classificação de triângulo

Leia 3 valores representando os lados de um triângulo. Verifique:

1. Se os lados formam um triângulo (desigualdade triangular)
2. Se sim, classifique como: **equilátero**, **isósceles** ou **escaleno**

### Exercício 05 — Calculadora com menu

Implemente uma calculadora usando `switch`. O programa deve:

- Ler dois números
- Ler a operação desejada: `+`, `-`, `*`, `/`
- Exibir o resultado
- Tratar divisão por zero com mensagem de erro

### Exercício 06 — Reajuste de salário

Leia o salário atual de um funcionário e aplique o reajuste conforme a tabela:

| Faixa salarial       | Reajuste |
|----------------------|----------|
| Até R$ 1.500,00      | 20%      |
| R$ 1.500,01 a R$ 3.000,00 | 15% |
| Acima de R$ 3.000,00 | 10%      |

Exiba: salário anterior, percentual de reajuste, valor do reajuste e novo salário.

---

## 🟠 Nível 3 — Laços (`while`, `for`, `do-while`)

### Exercício 07 — Tabuada

Leia um número inteiro e exiba sua tabuada de 1 a 10 formatada assim:

```
7 x  1 =  7
7 x  2 = 14
...
```

### Exercício 08 — Soma de ímpares

Leia um número inteiro N e calcule a soma de todos os números ímpares de 1 até N.

### Exercício 09 — Sequência de Fibonacci

Leia um número N e exiba os N primeiros termos da sequência de Fibonacci.

### Exercício 10 — Menu com repetição

Crie um programa de cadastro de produtos que, em loop, leia nome e preço de cada produto. Pergunte ao final de cada cadastro: `"Deseja cadastrar outro produto? (s/n)"`. Ao terminar, exiba todos os produtos e o valor total.

---

## 🔴 Nível 4 — Desafios que integram tudo

### Exercício 11 — Jogo de adivinhar número

O computador sorteia um número entre 1 e 100. O usuário tenta adivinhar. A cada tentativa, informe se o palpite é **maior** ou **menor** que o número sorteado. Conte as tentativas e parabenize ao acertar.

```csharp
// Dica:
Random rng = new Random();
int numero = rng.Next(1, 101);
```

### Exercício 12 — Relatório de vendas

Leia o nome e o valor vendido de N vendedores. Ao final, exiba:

- Total geral de vendas
- Maior venda (com nome do vendedor)
- Menor venda (com nome do vendedor)
- Média de vendas por vendedor

---

## 🟠 Nível 5 — Integradores (Médio)

### Exercício 13 — Caixa registradora

Um mercado vende produtos com ou sem desconto. Em loop, leia produtos (nome, preço unitário, quantidade) até o usuário digitar `"fim"`. Aplique **10% de desconto** se o total do item (preço × quantidade) for superior a R$ 50,00. Ao final, exiba:

- Subtotal de cada item (com indicação se teve desconto)
- Total geral
- Total de descontos concedidos

> **Dica:** use variáveis acumuladoras para desconto total e total geral.

---

### Exercício 14 — Verificador de CPF simplificado

Leia um CPF digitado pelo usuário (somente dígitos). Valide:

1. Se possui exatamente 11 caracteres numéricos
2. Se não são todos dígitos iguais (ex: `"11111111111"` é inválido)

Exiba `"CPF válido"` ou `"CPF inválido"` com o motivo.

> **Dica:** use `string.Length`, `char.IsDigit()` e um laço para verificar dígitos repetidos.

---

### Exercício 15 — Simulador de banco

Crie um sistema bancário simples. O usuário informa nome e saldo inicial. Em loop (`do-while`), exibe um menu:

```
1 - Depositar
2 - Sacar
3 - Ver saldo
4 - Sair
```

Regras:
- Impedir saques maiores que o saldo disponível
- Impedir valores negativos ou zero
- Ao sair, exibir o extrato completo com todas as operações realizadas

> **Dica:** acumule o histórico em uma `string` ou `List<string>`.

---

### Exercício 16 — Calculadora de IMC com histórico

Leia dados de N pessoas (nome, peso em kg, altura em m). Para cada uma, calcule e classifique o IMC:

| IMC              | Classificação     |
|------------------|-------------------|
| Abaixo de 18,5   | Abaixo do peso    |
| 18,5 a 24,9      | Peso normal       |
| 25,0 a 29,9      | Sobrepeso         |
| 30,0 ou mais     | Obesidade         |

Ao final, exiba:
- Pessoa com maior IMC
- Pessoa com menor IMC
- Média dos IMCs da turma
- Quantas pessoas estão com sobrepeso ou acima

> **Dica:** `IMC = peso / (altura * altura)`

---

## 🔴 Nível 6 — Integradores (Difícil)

### Exercício 17 — Torneio de futebol

Leia 4 times. Cada time joga contra todos os outros (turno único — 6 jogos no total). Para cada jogo, leia o placar dos dois times. Calcule para cada time: **pontos** (vitória=3, empate=1, derrota=0), **saldo de gols** e **gols marcados**. Exiba a tabela classificatória ordenada por pontos (desempate: saldo de gols).

> **Dica:** use arrays paralelos para nome, pontos, saldo e gols. Para ordenar, implemente um bubble sort simples.

---

### Exercício 18 — Gerador de tabuada em arquivo

Gere as tabuadas de 1 a 10 e salve em um arquivo `tabuadas.txt` com colunas alinhadas. Exemplo de formatação esperada:

```
 1 x  1 =  1    2 x  1 =  2    3 x  1 =  3  ...
 1 x  2 =  2    2 x  2 =  4    3 x  2 =  6  ...
```

Ao terminar, exiba no console quantas linhas foram escritas.

> **Dica:** use `PadLeft()` ou `PadRight()` para alinhar. Use `File.WriteAllText()` ou `StreamWriter`.

---

### Exercício 19 — Sistema de notas com aprovação parcial

Leia dados de N alunos com **4 notas bimestrais**. Calcule a média ponderada com os pesos: 1, 2, 3 e 4:

```
média = (n1×1 + n2×2 + n3×3 + n4×4) / 10.0
```

Classifique cada aluno:
- Média ≥ 7 → Aprovado
- 5 ≤ média < 7 → Recuperação
- Média < 5 → Reprovado

Gere um relatório final com: total de aprovados, reprovados, em recuperação, melhor e pior média da turma.

---

## 🏆 Nível 7 — Desafios

### Exercício 20 — Jogo da forca no console

Implemente o jogo da forca completo:

- O programa sorteia uma palavra de uma lista pré-definida (mínimo 10 palavras)
- O jogador tem **6 tentativas**
- A cada rodada, exibir:
  - As letras descobertas (`_ _ a _ a` para letras não descobertas)
  - As letras já tentadas
  - Tentativas restantes
- Ao fim, revelar a palavra e informar vitória ou derrota

> **Dica:** use um `char[]` para as letras tentadas. Use `Contains()` para verificar letras. Separe a lógica de exibição da lógica do jogo.

---

### Exercício 21 — Simulador de caixa eletrônico

Leia um valor de saque (múltiplo de R$ 10). O caixa dispõe de notas de:  
`R$ 200 | R$ 100 | R$ 50 | R$ 20 | R$ 10`

Calcule a **menor quantidade de notas** possível para compor o valor (algoritmo guloso) e exiba quantas notas de cada tipo serão entregues. Se o valor não puder ser formado, informe o erro.

> **Dica:** comece sempre pela maior nota.  
> `int notas200 = valor / 200; valor %= 200;` e assim por diante.

---

### Exercício 22 — Agenda de contatos com busca

Crie uma agenda com capacidade para 20 contatos usando **arrays paralelos** (nome, telefone, email). Implemente um menu:

```
1 - Adicionar contato
2 - Buscar por nome
3 - Listar todos
4 - Remover por nome
5 - Sair
```

Regras:
- Ao remover, deslocar os elementos restantes para não deixar posições vazias
- Busca deve ser **case-insensitive**
- Ao listar, exibir os contatos numerados

> **Dica:** use `int total` para rastrear quantos contatos estão cadastrados. Na remoção, desloque os elementos a partir do índice encontrado.

---

## Referências

- Curso: [C# COMPLETO — Programação Orientada a Objetos + Projetos](https://www.udemy.com/course/programacao-orientada-a-objetos-csharp/) — Nélio Alves (Udemy)
- Documentação oficial: [docs.microsoft.com/dotnet/csharp](https://docs.microsoft.com/dotnet/csharp)