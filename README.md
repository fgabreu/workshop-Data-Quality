# workshop-Data-Quality
Qualidade em Projeto de Dados

Workshop 02 do https://jornadadedados.alpaclass.com/ Para desenvolver o desafio de negocio, vamos montar a seguinte ETL

Fluxo:

graph TD;
    A[Configura Variáveis] --> B[Ler o Banco SQL];
    B --> V[Validação do Schema de Entrada];
    V -->|Falha| X[Alerta de Erro];
    V -->|Sucesso| C[Transformar os KPIs];
    C --> Y[Validação do Schema de Saída];
    Y -->|Falha| Z[Alerta de Erro];
    Y -->|Sucesso| D[Salvar no DuckDB];
