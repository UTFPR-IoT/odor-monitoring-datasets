# Experimento: integração LoRaWAN

## Visão geral
- __Data:__ 2026-03-25 18:11:10 (GMT-3) à 2026-04-09 09:11:29
    - Ineterrupto: 2026-03-31 11:17:00 à 2026-04-09 09:11:29
- __Local:__ E304 UTFPR-TD.
- __Objetivo:__ avaliar a integração LoRaWAN da estação.

## Metodologia
- Tempo de amostragem da estação em 1 minuto:
    - a cada 1 minuto a estação coleta uma amostra de todas as suas variáveis e armezana no SD.
- Envio LoRaWAN a cada 30 minutos:
    - entre os envios são calculadas métricas sobre cada variável da estação entre o período de envio; essas métricas são enviadas à Nuvem.

#### Observações
- O sensor anemômetro não foi experimentado:
    - valores arbitrários.
- Sensor SO2 apresentou leituras negativas.
- RTC da estação estava com a data desconfigurada em 2 meses.
    - Início: 2026-03-25 16:00:10

## Resultados
Nesse experimento foram avaliados o escopo de registro local (raw-estacao.csv) e de registro na Nuvem (net-) para o período de operação ineterrupta.

#### raw-estação
O índice do registro local segue:

| Índice | Grandeza                       | Unidade |
| :---:  | :---                           | :---:   |
| D0     | VOC - Concentração             | ppb     |
| D1     | VOC - Massa                    | ug      |
| D2     | VOC - Temperatura              | °C      |
| D3     | VOC - Umidade                  | %       |
| D4     | $H_2S$ - Concentração          | ppb     |
| D5     | $H_2S$ - Massa                 | ug      |
| D6     | $H_2S$ - Temperatura           | °C      |
| D7     | $H_2S$ - Umidade               | %       |
| D8     | $SO_2$ - Concentração          | ppb     |
| D9     | $SO_2$ - Massa                 | ug      |
| D10    | $SO_2$ - Temperatura           | °C      |
| D11    | $SO_2$ - Umidade               | %       |
| D12    | $NH_3$ - Concentração          | ppb     |
| D13    | $NH_3$ - Massa                 | ug      |
| D14    | $NH_3$ - Temperatura           | °C      |
| D15    | $NH_3$ - Umidade               | %       |
| D16    | $CH_3SH$ - Concentração        | ppb     |
| D17    | $CH_3SH$ - Massa               | ug      |
| D18    | $CH_3SH$ - Temperatura         | °C      |
| D19    | $CH_3SH$ - Umidade             | %       |
| D20    | CO (Monóxido de Carbono)       | -       |
| D21    | $NH_3$ (Amônia)                | -       |
| D22    | $NO_2$ (Dióxido de Nitrogênio) | -       |
| D23    | Reservado                      | 0       |
| D24    | Reservado                      | 0       |
| D25    | Reservado                      | 0       |
| D26    | Temperatura Ambiente           | °C      |
| D27    | Pressão Atmosférica            | hPa     |
| D28    | Umidade Relativa               | %       |
| D29    | Direção do Vento               | °       |
| D30    | Velocidade do Vento            | m/s     |

#### net-raw
- Há um .csv para cada variável;
- O .csv contém valores métricos de média, máxima e mínima para o período.

## Estrutura dos arquivos
```text
.
├── README.md
├── data/
│   ├── net-anemodir-raw.csv     # direção do vento
│   ├── net-anemovel-raw.csv     # velocidade do vento
│   ├── net-ch3sh-raw.csv        # ch3sh
│   ├── net-h2s-raw.csv          # h2s
│   ├── net-hum-raw.csv          # umidade
│   ├── net-nh3-raw.csv          # nh3
│   ├── net-press-raw.csv        # pressão
│   ├── net-so2-raw.csv          # so2
│   ├── net-temp-raw.csv         # temperatura
│   ├── net-voc-raw.csv          # voc
│   └── raw-estacao.csv          # csv colhido no SD da estação
├── notebook/
└── output/
    ├── plot/
    └── processed/
```