# Escalonador de Sistemas Operacionais

[![Java](https://img.shields.io/badge/Java-17%2B-orange?logo=openjdk\&logoColor=white)](https://www.java.com/)
[![Operating System](https://img.shields.io/badge/Operating%20System-Scheduling-blueviolet)](#)
[![USP](https://img.shields.io/badge/USP-EACH-red)](https://www5.each.usp.br/)

> Implementação de um **escalonador de processos** para simulação de algoritmos de escalonamento de CPU em sistemas operacionais.

Projeto desenvolvido para a disciplina **Sistemas Operacionais**, da Universidade de São Paulo (USP — EACH), com foco na implementação e análise do comportamento de processos submetidos a diferentes estratégias de escalonamento.

## Sobre o projeto

O projeto implementa um **escalonador de processos**, responsável por determinar a ordem de execução dos processos e controlar a utilização da CPU de acordo com os parâmetros definidos para a simulação.

Um dos principais parâmetros utilizados é o **quantum**, que determina o intervalo máximo de tempo durante o qual um processo pode permanecer em execução antes de ceder a CPU para outro processo.

A execução pode receber o quantum diretamente pela linha de comando ou utilizar o valor definido no arquivo de configuração do projeto.

```text
Processos → Escalonador → Processo A / Processo B / ... → CPU
```

## Estrutura do Repositório

```text
operating-system-scheduler/
│
├── docs/
│   └── requisitos_projeto.pdf
|
├── output/
│   └── ...
|
├── programas/
│   └── ...
|
├── src/
│   └── com/
│       └── escalonador/
│           └── ...
│
├── .gitignore
├── run.sh
├── run_all_quantums.sh
└── README.md
```

### Diretórios

| Diretório / Arquivo   | Descrição                                                           |
| --------------------- | ------------------------------------------------------------------- |
| `src/`                | implementação principal do escalonador                              |
| `programas/`          | programas utilizados como entrada para as simulações                |
| `output/`             | resultados gerados durante as execuções                             |
| `run.sh`              | script para compilação e execução do escalonador                    |
| `run_all_quantums.sh` | script para execução automatizada com diferentes valores de quantum |
| `ep01.pdf`            | enunciado do exercício                                              |

## Instalação e Uso

### Requisitos

* Java
* Bash
* Linux

### Execução

O projeto pode ser executado utilizando o script `run.sh`:

```bash
./run.sh <quantum>
```

Exemplo:

```bash
./run.sh 5
```

Nesse caso, o escalonador será executado utilizando **5 unidades de tempo como quantum**.

Também é possível executar o programa sem informar o quantum:

```bash
./run.sh
```

Quando nenhum valor é informado pela linha de comando, será utilizado o **quantum definido no arquivo de configuração do projeto**.

## Testes com diferentes valores de Quantum

O repositório possui um script auxiliar para executar automaticamente o programa utilizando diferentes valores de quantum:

```bash
./run_all_quantums.sh
```

O script executa o programa **10 vezes**, passando como parâmetro os valores de quantum de `1` a `10` via linha de comando:

```text
Quantum 1 → Execução → Quantum 2 → Execução → Quantum 3 → ... → Quantum 10 → Execução
```

Essa execução permite comparar os resultados obtidos para diferentes valores de quantum e analisar seus impactos no comportamento do escalonador.

## Resultados

Os resultados das execuções são armazenados no diretório:

```text
output/
```

Os arquivos gerados podem ser utilizados para analisar o comportamento dos processos e comparar os resultados obtidos com diferentes valores de quantum.

## Conceitos abordados

O projeto envolve conceitos fundamentais de **Sistemas Operacionais**, incluindo:

* Escalonamento de processos
* Processos e execução
* Escalonamento de CPU
* Quantum de tempo
* Alternância de processos
* Fila de processos
* Simulação de execução
* Análise de diferentes configurações de escalonamento

## Licença

Projeto Acadêmico desenvolvido para a **Universidade de São Paulo — Escola de Artes, Ciências e Humanidades (USP — EACH)**.

© 2026 Ygor Araujo

[![GitHub](https://img.shields.io/badge/GitHub-contygor-181717?logo=github\&logoColor=white)](https://github.com/contygor)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ygor%20A)](https://www.linkedin.com/in/contygor/)
