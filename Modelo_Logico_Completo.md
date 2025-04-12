# Modelo Lógico Relacional – Projeto Obesidade

Este documento descreve o modelo lógico relacional derivado do modelo conceitual fornecido. Inclui tabelas, atributos, chaves primárias, estrangeiras e os relacionamentos com suas respectivas cardinalidades.

## Pessoa
- id_pessoa (INT) – PK
- age (FLOAT)
- gender (STRING)
- height (FLOAT)
- weight (FLOAT)
- id_diagnostico (INT) – FK → Diagnostico(id_diagnostico)
- id_hist_fam (INT) – FK → HistoricoFamiliar(id_hist_fam)

## HabitoAlimentar
- id_habito (INT) – PK
- favc (STRING)
- fcvc (FLOAT)
- ncp (FLOAT)
- caec (STRING)
- calc (STRING)
- ch2o (FLOAT)

## EstiloVida
- id_estilo (INT) – PK
- scc (STRING)
- smoke (STRING)
- faf (FLOAT)
- tue (FLOAT)
- mtrans (STRING)

## HistoricoFamiliar
- id_hist_fam (INT) – PK
- valor (STRING)

## Diagnostico
- id_diagnostico (INT) – PK
- nome (STRING)

## Possui (Relacionamento)
- id_pessoa (INT) – PK, FK → Pessoa
- id_habito (INT) – PK, FK → HabitoAlimentar
- Cardinalidade: (1,N) Pessoa – (1,N) HabitoAlimentar

## Recebe (Relacionamento)
- id_pessoa (INT) – PK, FK → Pessoa
- id_estilo (INT) – PK, FK → EstiloVida
- Cardinalidade: (1,N) Pessoa – (1,N) EstiloVida
