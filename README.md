﻿# Sistema de Gerenciamento de Voos - Companhia Aérea Voo Seguro

 Descrição do Projeto

Este projeto tem como objetivo o desenvolvimento de um sistema de gerenciamento para a Voo Seguro, uma companhia aérea que visa melhorar o controle de voos, reservas, tripulação e passageiros. O sistema foi desenvolvido como parte de um trabalho interdisciplinar no curso de Engenharia de Software, utilizando a linguagem de programação C.

O sistema foi projetado para resolver problemas como reservas duplicadas, falta de controle sobre voos e assentos, e ausência de integração entre as informações dos passageiros, tripulação e voos. O programa foi implementado utilizando arquivos binários para persistência de dados, e bibliotecas em C para organizar os módulos do software.
Funcionalidades Implementadas

    Cadastro de Passageiros:
        Registro de passageiros com informações como código, nome, endereço, telefone, fidelidade e pontos acumulados.

    Cadastro de Tripulação:
        Cadastro de membros da tripulação (piloto, copiloto e comissário), garantindo que não haja códigos duplicados.

    Cadastro de Voos:
        Cadastro completo de voos, incluindo informações sobre data, hora, origem, destino, tarifa, tripulação e avião. Um voo só é marcado como ativo se tiver ao menos um piloto e um copiloto.

    Cadastro de Assentos:
        Cadastro de assentos disponíveis para cada voo, com controle de disponibilidade.

    Reserva de Assentos:
        Funcionalidade que permite a reserva de assentos, desde que o voo esteja ativo e o assento esteja disponível. Previne reservas duplicadas.

    Baixa em Reserva:
        Liberação de assentos de voos cancelados ou alterados e cálculo da tarifa total a ser paga, quando aplicável.

    Pesquisa de Passageiros e Tripulação:
        Pesquisa por código ou nome de passageiros e membros da tripulação.

    Consulta ao Programa de Fidelidade:
        Acúmulo de pontos de fidelidade para passageiros, com 10 pontos por voo realizado.
        
Como Rodar o Sistema
Pré-requisitos:

    Ter um compilador C instalado (ex: GCC).
    Sistema operacional compatível com C (Linux, Windows, macOS).
