# Monitoramento da Fauna — Parque Nacional do Cerrado

Análise de dados de 30 dias de monitoramento por câmeras automáticas (01/05/2026 a 30/05/2026)
em um parque nacional do Cerrado.

> Os dados são sintéticos e foram criados para fins educacionais (checkpoint da trilha de dados).

## Contexto após análise dos dados

O parque possui 12 câmeras distribuídas em três ambientes:

| Área | Câmeras |
|---|---|
| Cerrado aberto | CAM01 a CAM04 |
| Mata de galeria | CAM05 a CAM08 |
| Veredas e áreas úmidas | CAM09 a CAM12 |

O dataset contém as colunas câmera, data/hora, duração, espécie, grupo
(mamífero, ave ou anfíbio), número de indivíduos, temperatura e umidade.

## Desafios do Checkpoint

| # | Desafio | Status |
|---|---|---|
| Bônus 1 | Preparação e tratamento dos dados | Não Iniciado |
| 1 | Capivaras: solitárias ou em grupo? | Não Iniciado |
| 2 | Em quais períodos do dia a fauna está mais ativa? | Não Iniciado |
| 3 | Anfíbios são mais registrados com umidade alta? | Não Iniciado |
| 4 | Quais câmeras têm mais registros e mais espécies? | Não Iniciado |
| 5 | Onde e quando procurar a onça-pintada? | Não Iniciado |
| Bônus 2 | Duração dos registros por espécie | Não Iniciado |
| Bônus 3 | Padrão de ocorrência do lobo-guará | Não Iniciado |
| Bônus 4 | Investigação própria | Não Iniciado |

## Arquitetura Planejada

```text
dataset.json → Volume (raw) → bronze_registros → silver_registros → notebooks de análise
```

Todas as tabelas ficam no Unity Catalog, no schema `workspace.fauna`.

## Tecnologias

- Databricks Free Edition (computação serverless)
- PySpark e Spark SQL
- Delta Lake e Unity Catalog
- Git e GitHub (Git folders do Databricks)

## Estrutura do repositório

_Em construção — será atualizada a cada etapa._

## Autor

Lucas Roberto — [@lucasrobc](https://github.com/lucasrobc)