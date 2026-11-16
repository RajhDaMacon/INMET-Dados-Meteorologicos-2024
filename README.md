# Dados Meteorológicos INMET 2024

Este repositório contém os **dados meteorológicos horários** de **565 estações automáticas** do [INMET](https://portal.inmet.gov.br/) (Instituto Nacional de Meteorologia) para todo o ano de **2024** no Brasil.

## Conteúdo

- Arquivo ZIP com **565 arquivos CSV**, um para cada estação.
- Cada CSV contém dados horários de:
  - Precipitação
  - Pressão atmosférica
  - Radiação global
  - Temperatura do ar e ponto de orvalho
  - Umidade relativa
  - Vento (direção, rajada e velocidade)
  - E outros parâmetros

## Como usar

1. Baixe o arquivo ZIP (veja seção de downloads abaixo).
2. Extraia os arquivos.
3. Abra os CSVs no Excel, LibreOffice, Python (pandas), R, etc.
   - **Atenção à codificação**: os arquivos usam encoding Latin-1 / Windows-1252 (acentos podem aparecer errados se abrir como UTF-8).

### Exemplo em Python

```python
import pandas as pd

df = pd.read_csv("INMET_CO_DF_A001_BRASILIA_01-01-2024_A_31-12-2024.CSV", 
                 sep=";", encoding="latin1", skiprows=8)
print(df.head())
```

## Lista de estações

Há 565 estações cobrindo todas as regiões do Brasil (N, NE, CO, SE, S).

Os nomes dos arquivos seguem o padrão:
`INMET_<REGIAO>_<UF>_<CODIGO>_<NOME-ESTACAO>_01-01-2024_A_31-12-2024.CSV`

## Fonte

Dados oficiais do INMET - Portal de Dados Meteorológicos.

## Download

O arquivo ZIP completo (~99 MB) será disponibilizado em breve nas Releases deste repositório.

**Compartilhe este link no WhatsApp** para que qualquer pessoa possa consultar as informações e baixar os dados:
https://github.com/RajhDaMacon/INMET-Dados-Meteorologicos-2024
