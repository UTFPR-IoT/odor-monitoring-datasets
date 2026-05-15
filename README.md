# Odor-Monitoring-Datasets-2025/26

### Estrutura padrão dos experimentos
```text
.
└── nome-do-experimento/
    ├── README.md
    ├── data/
    │   └── dados-raw.csv
    ├── notebook/
    │   └── caderno-de-analise.ipynb
    └── output/
        ├── plot/
        │   └── grafico-plotado.png
        └── processed/
            └── dataset-processado.csv
```

## Estrutura do Repositório
```text
.
├── README.md                
├── .gitignore 
│
├── teste-campo-compostec/
│   ├── README.md
│   ├── data/
│   │   ├── media-alfredo-teste-campo-h2s.csv
│   │   ├── media-alfredo-teste-campo-nh3.csv
│   │   └── teste-zugam-compostec.xlsx
│   ├── notebook/
│   │   ├── media-teste-campo-compostec-h2s.ipynb
│   │   └── media-teste-campo-compostec-nh3.ipynb
│   └── output/
│       ├── plot/
│       └── processed/
│
├── teste-campo-estrebaria/
│   ├── README.md
│   ├── data/
│   │   └── teste-estrebaria-1-fluxo-passivo-equalizado-media.xlsx
│   ├── notebook/
│   └── output/
│       ├── plot/
│       └── processed/
│
├── teste-campo-utfpr/
│   ├── README.md
│   ├── data/
│   │   ├── teste-campo-utfpr.xlsx
│   │   ├── teste-fluxo-forcado.csv
│   │   └── teste-fluxo-nao-forcado.csv
│   ├── notebook/
│   └── output/
│       ├── plot/
│       └── processed/
│
├── teste-lab-lorawan/
│   ├── readme-teste-lab-lorawan.md
│   ├── data/
│   │   ├── data_raw.csv     # Dados brutos obtidos
│   │   ├── analysis.ipynb   # Notebook de análise em Python
│   │   └── README.md        # Notas específicas do experimento
│   ├── notebook/
│   └── output/
│       ├── plot/
│       └── processed/
│
├── teste-lab-ufmg/  
├── README.md
│   ├── datas/
│   │   ├── teste-h2s-2.7ppm.xlsx
│   │   ├── teste-h2s-500ppb-cx-7.5L.xlsx
│   │   ├── teste-h2s-diluido-bag3L-10ppm.xlsx
│   │   └── teste-nitrogenio-nivel-zero.xlsx
│   ├── notebook/
│   └── output/
│       ├── plot/
│       └── processed/     
│ 
└── teste-temperatura-umidade/
    ├── README.md
    ├── datas/
    │   └── semeatech-temperatura-umidade.xlsx
    ├── notebook/
    └── output/
        ├── plot/
        └── processed/