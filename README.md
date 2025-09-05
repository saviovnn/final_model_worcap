# 🔥 Detecção de Queimadas - Worcap Hackathon 2025

Sistema de detecção de áreas de queimadas em imagens de satélite utilizando **Machine Learning** e **índices espectrais**.

## 📋 Sobre o Projeto

Este projeto foi desenvolvido para o **Worcap Hackathon 2025** e implementa um pipeline completo para análise de imagens multitemporais de satélite, visando a detecção automática de áreas afetadas por queimadas.

### 🎯 Objetivo
Desenvolver um modelo de **Random Forest** que identifique pixels de queimadas comparando imagens de satélite antes (T1) e depois (T2) de eventos de fogo.

## 🛠️ Tecnologias Utilizadas

- **Python** - Linguagem principal
- **scikit-learn** - Machine Learning (Random Forest)
- **rasterio** - Processamento de imagens de satélite
- **numpy** - Manipulação de arrays
- **pandas** - Análise de dados
- **matplotlib** - Visualização

## 📊 Metodologia

### Índices Espectrais Calculados:
- **NDVI** (Normalized Difference Vegetation Index)
- **NBR** (Normalized Burn Ratio) 
- **dNBR** (diferencial NBR entre T1 e T2)

### Features do Modelo:
- NDVI T1 e T2
- NBR T1 e T2
- dNBR (diferença temporal)
- Diferenças entre bandas NIR e SWIR

## 📈 Resultados

- **603 imagens** processadas com sucesso
- **AUC médio**: 0.8475
- **F1-Score médio**: 0.8700
- **Recall médio**: 0.7991
- **Precision média**: 0.9668

## 📁 Estrutura do Projeto

```
worcap/
├── final_model_worcap.ipynb          # Notebook principal com pipeline completo
├── melhor_modelo_area_fogo.joblib    # Modelo treinado salvo
├── melhor_mascara_area_fogo.tif      # Máscara predita do melhor resultado
├── melhor_modelo_area_fogo.csv       # Predições em formato CSV
└── README.md                         # Este arquivo
```

## 🚀 Como Executar

1. **Instalar dependências:**
```bash
pip install numpy rasterio matplotlib scikit-learn pandas tqdm joblib
```

2. **Executar o notebook:**
```bash
jupyter notebook final_model_worcap.ipynb
```

## 👨‍💻 Autor

**Sávio Jenner Vianna Silva Rennó**  
Estudante de Sistemas de Informação - UNITAU  
📧 [savioviannasilva131@gmail.com](mailto:savioviannasilva131@gmail.com)

## 📝 Licença

Projeto desenvolvido para o Worcap Hackathon 2025.
