# Desafio Técnico - Estágio em Meteorologia (Ampere)

Este repositório contém a solução do desafio técnico para a vaga de estágio em Meteorologia na empresa Ampere, desenvolvido por **Edivan Silva**.

## Sobre o Projeto

O desafio consiste em três exercícios principais:

1. **Download de Arquivos GRIB**
2. **Acumulado de Chuva e Plotagem de Mapa**
3. **Extração de Valores de Precipitação da Bacia do Rio Grande**

## Bibliotecas Utilizadas

Para a execução dos códigos, foram utilizadas as seguintes bibliotecas:

- `os` e `requests`: Para manipulação de diretórios e download de arquivos.
- `pygrib`: Para leitura de arquivos GRIB.
- `numpy`: Para manipulação de dados matriciais.
- `matplotlib` e `cartopy`: Para visualização e plotagem de mapas.
- `pandas` e `geopandas`: Para manipulação e análise de dados espaciais.
- `shapely`: Para manipulação de geometrias.

## Estrutura do Código

### Exercício 1 - Download de Arquivos GRIB

O script baixa arquivos GRIB de precipitação do modelo MERGE do CPTEC/INPE, referentes ao período de **15/03/2025 a 21/03/2025**. O processo é feito da seguinte forma:

1. Define-se o diretório para armazenar os arquivos.
2. Gera-se a lista de datas para download.
3. Baixa-se os arquivos correspondentes e os salva localmente.

### Exercício 2 - Acumulado de Chuva e Plotagem de Mapa

Este trecho do código:

1. Lê os arquivos GRIB baixados no exercicio 1 e soma a precipitação para obter o acumulado.
2. Define uma paleta de cores e intervalos para visualização dos dados.
3. Plota um mapa usando `cartopy`, adicionando contornos e uma legenda para os valores de precipitação.
4. Salva a figura resultante como `Precip_Acumulada.png`.

### Exercício 3 - Extração de Valores de Precipitação da Bacia do Grande

O script faz a análise espacial da precipitação na Bacia do Rio Grande:

1. Clona o repositório do desafio contendo os dados.
2. Lê o shapefile da bacia e o arquivo de precipitação.
3. Filtra os pontos de chuva que estão dentro da bacia.
4. Calcula a precipitação média da região.
5. Plota um mapa com os pontos e valores de precipitação.
6. Salva os dados extraídos em `Média_prec_bacia.csv`.

## Como Executar

1. **No Google Colab:**
   - Suba o script `Desafio_Técnico_Edivan_Silva.ipynb`.
   - Execute as células conforme a ordem do código.
   
2. **Localmente:**
   - Certifique-se de ter instalado as bibliotecas necessárias:
     ```sh
     pip install pygrib cartopy geopandas shapely matplotlib numpy pandas requests
     ```
   - Execute o script Python:
     ```sh
     python desafio_técnico_edivan_silva.py
     ```

## Resultados

- Arquivos GRIB baixados na pasta `MERGE_GRIBS`.
- Mapa de precipitação acumulada salvo como `Precip_Acumulada.png`.
- Dados extraídos da Bacia do Grande salvos em `Média_prec_bacia.csv`.

---

Este repositório representa uma solução para o desafio técnico proposto, que visa demostrar habilidades em análise e processamento de dados meteorológicos. Para sugestões e melhorias, entre em contato!

**Desenvolvido por:** *Edivan Silva*

