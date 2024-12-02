# Projeto de Classificação de Gatos vs Cachorros

Este projeto implementa um modelo de classificação binária para diferenciar imagens de gatos e cachorros utilizando aprendizado profundo. O processo inclui pré-processamento de dados, treinamento de um modelo usando a arquitetura **VGG16** e avaliação do desempenho do modelo em dados nunca vistos. Abaixo está uma descrição detalhada do projeto.

---

## Índice

1. [Visão Geral](#visão-geral)
2. [Conjunto de Dados](#conjunto-de-dados)
3. [Estrutura do Projeto](#estrutura-do-projeto)
4. [Dependências](#dependências)
5. [Passos para Executar o Projeto](#passos-para-executar-o-projeto)
6. [Arquitetura do Modelo](#arquitetura-do-modelo)
7. [Resultados](#resultados)
8. [Contribuições](#contribuições)
9. [Licença](#licença)

---

## Visão Geral

O objetivo deste projeto é classificar imagens de gatos e cachorros. Para isso, utilizamos **transfer learning** (aprendizado por transferência) com o modelo pré-treinado **VGG16** para extração de características. O conjunto de dados é dividido em conjuntos de treinamento, validação e teste, e uma camada personalizada de classificação é adicionada ao modelo base VGG16 para realizar a classificação binária.

---

## Conjunto de Dados

O conjunto de dados utilizado neste projeto é o [Conjunto de Dados de Gatos e Cachorros da Microsoft](https://www.microsoft.com/en-us/download/details.aspx?id=54765). Ele contém imagens de gatos e cachorros com as seguintes características:

- **Número total de imagens**: ~25.000
- **Categorias**: Gatos e Cachorros
- **Formato**: JPEG

O conjunto de dados é separado em três subconjuntos:

- **Conjunto de treinamento**: 90% do conjunto de dados original
- **Conjunto de teste**: 10% do conjunto de dados original
- **Conjunto de validação**: Derivado do conjunto de teste (50% dos dados de teste)

---

## Estrutura do Projeto

Os seguintes diretórios são criados e utilizados durante a execução do projeto:



PetImages/
│
├── training/
│ ├── cats/
│ ├── dogs/
│
├── validation/
│ ├── cats/
│ ├── dogs/
│
├── testing/
├── cats/
├── dogs/



Além disso, o script Python faz o download, descompacta e organiza o conjunto de dados automaticamente.

---

## Dependências

O projeto utiliza as seguintes bibliotecas Python:

- `tensorflow` (para construção e treinamento do modelo)
- `matplotlib` (para visualização dos resultados)
- `numpy` (para operações numéricas)
- `pandas` (para manipulação de dados)
- `requests` (para download do conjunto de dados)
- `shutil` (para operações com arquivos)
- `os` (para gerenciamento de diretórios)
- `random` (para embaralhar os dados)

Instale todas as dependências utilizando:

```bash
pip install tensorflow matplotlib numpy pandas requests