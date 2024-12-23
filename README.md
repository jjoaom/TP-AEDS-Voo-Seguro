# Sistema de Gerenciamento de Voos - Companhia Aérea Voo Seguro

## Descrição do Projeto

Este projeto é um sistema de gerenciamento para a companhia aérea fictícia **Voo Seguro**, desenvolvido em C++ como parte de um trabalho interdisciplinar do curso de Engenharia de Software. Ele visa resolver problemas relacionados à gestão de voos, reservas, tripulação e passageiros, utilizando arquivos binários para persistência de dados e bibliotecas para modularização do software.

---
![Build Status](https://img.shields.io/github/actions/workflow/status/jjoaom/Companhia-Voo-Seguro/cmake-multi-platform.yml?branch=main)
![Coverage](https://codecov.io/gh/jjoaom/Companhia-Voo-Seguro/branch/main/graph/badge.svg)
![License](https://img.shields.io/github/license/jjoaom/Companhia-Voo-Seguro)

## Sumário
- [Descrição do Projeto](#descrição-do-projeto)
- [Como Executar o Projeto](#como-executar-o-projeto)
  - [Pré-requisitos](#pré-requisitos)
  - [Instruções para Windows](#instruções-para-windows)
  - [Instruções para Linux](#instruções-para-linux)
- [Funcionalidades Implementadas](#funcionalidades-implementadas)
- [Documentação das Classes](#documentação-das-classes)
  - [Classe Passageiro](#classe-passageiro)
  - [Classe Tripulação](#classe-tripulação)
  - [Classe Voo](#classe-voo)
  - [Classe Assento](#classe-assento)
  - [Classe Reserva](#classe-reserva)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
---
## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/jjoaom/Companhia-Voo-Seguro
   ```
## Como Executar o Projeto

### Pré-requisitos

- **Compilador C++**: É necessário ter um compilador instalado, como GCC (Linux) ou MSVC/MinGW (Windows).

### Instruções para Windows

1. Baixe e instale o MinGW pelo site oficial [MinGW-w64](https://www.mingw-w64.org/).

2. Abra o terminal ou o Prompt de Comando no diretório do projeto.

4. Compile o programa principal:
    ```bash
   cd src
   ```
   ```bash
   g++ -o main main.cpp 
   ```

6. Execute o programa:
   ```bash
   main.exe
   ```


### Instruções para Linux

1. Instale o GCC (se ainda não estiver instalado):
   ```bash
   sudo apt update
   sudo apt install g++
   ```

2. Navegue até a pasta do projeto pelo terminal.

3. Compile o programa principal:
   ```bash
   cd src
   ```
   ```bash
   g++ -o sistema main.cpp -std=c++17
   ```

5. Execute o programa:
   ```bash
   ./sistema
   ```

---

## Funcionalidades Implementadas

1. **Cadastro de Passageiros**:
   - Registro de passageiros com informações como código, nome, endereço, telefone, fidelidade e pontos acumulados.

2. **Cadastro de Tripulação**:
   - Cadastro de membros da tripulação (piloto, copiloto e comissário), garantindo que não haja códigos duplicados.

3. **Cadastro de Voos**:
   - Cadastro completo de voos, incluindo informações sobre data, hora, origem, destino, tarifa, tripulação e avião. Um voo só é marcado como ativo se tiver ao menos um piloto e um copiloto.

4. **Cadastro de Assentos**:
   - Cadastro de assentos disponíveis para cada voo, com controle de disponibilidade.

5. **Reserva de Assentos**:
   - Permite a reserva de assentos, desde que o voo esteja ativo e o assento disponível. Previne reservas duplicadas.

6. **Baixa em Reserva**:
   - Liberação de assentos de voos cancelados ou alterados e cálculo da tarifa total a ser paga, quando aplicável.

7. **Pesquisa de Passageiros e Tripulação**:
   - Pesquisa por código ou nome de passageiros e membros da tripulação.

8. **Consulta ao Programa de Fidelidade**:
   - Acúmulo de pontos de fidelidade para passageiros, com 10 pontos por voo realizado.

---

## Documentação das Classes

### Classe Passageiro

#### Descrição
Representa um passageiro com os seguintes atributos:

| Atributo          | Tipo     | Descrição                                      |
| ------------------ | -------- | ---------------------------------------------- |
| `id`              | `string` | Identificador único do passageiro.             |
| `nome`            | `string` | Nome do passageiro.                            |
| `endereco`        | `string` | Endereço do passageiro.                        |
| `telefone`        | `string` | Telefone do passageiro.                        |
| `fidelidade`      | `bool`   | Indica se participa do programa de fidelidade. |
| `pontosFidelidade`| `int`    | Pontos acumulados no programa de fidelidade.   |

---

### Classe Tripulação

#### Descrição
Representa um membro da tripulação com os seguintes atributos:

| Atributo  | Tipo     | Descrição                          |
| --------- | -------- | ---------------------------------- |
| `id`      | `string` | Identificador único do tripulante. |
| `nome`    | `string` | Nome do membro da tripulação.      |
| `telefone`| `string` | Telefone do tripulante.            |
| `cargo`   | `string` | Cargo do tripulante (Piloto, etc). |

---

### Classe Voo

#### Descrição
Representa um voo com os seguintes atributos:

| Atributo  | Tipo     | Descrição                           |
| --------- | -------- | ----------------------------------- |
| `id`      | `string` | Identificador único do voo.         |
| `data`    | `string` | Data do voo.                        |
| `hora`    | `string` | Hora do voo.                        |
| `origem`  | `string` | Origem do voo.                      |
| `destino` | `string` | Destino do voo.                     |
| `idAviao` | `string` | Identificador do avião.             |
| `idPiloto`| `string` | Identificador do piloto.            |
| `status`  | `bool`   | Status do voo (ativo/inativo).      |
| `tarifa`  | `float`  | Tarifa do voo.                      |

---

### Classe Assento

#### Descrição
Representa um assento com os seguintes atributos:

| Atributo   | Tipo     | Descrição                      |
| ---------- | -------- | ------------------------------ |
| `numAssento`| `int`   | Número do assento.             |
| `idVoo`    | `string` | Identificador do voo.          |
| `ocupado`  | `bool`   | Status do assento (ocupado).   |

---

### Classe Reserva

#### Descrição
Representa uma reserva com os seguintes atributos:

| Atributo     | Tipo     | Descrição                      |
| ------------ | -------- | ------------------------------ |
| `idVoo`      | `string` | Identificador do voo.          |
| `numAssento` | `int`    | Número do assento.             |
| `idPassageiro`| `string`| Identificador do passageiro.   |

---

## Tecnologias Utilizadas

- Linguagem: **C++**
- Ferramentas de Desenvolvimento: **GCC**, **MSVC**, **MinGW**
- Ferramentas de Construção: **CMake**
- Ferramentas de Teste: **GoogleTest**
- Persistência: Arquivos binários
- Persistência: Arquivos binários

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
