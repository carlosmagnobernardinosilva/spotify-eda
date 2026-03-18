<<<<<<< HEAD
# spotify-eda
Análise Exploratória de Dados (EDA) em um conjunto de dados do Spotify, revelando padrões em características de áudio, tendências de popularidade e comportamento de artistas usando Python, Pandas e técnicas de visualização de dados.
=======
# 🎵 Análise Exploratória de Dados - Spotify (Top Streamed Songs)

> Uma análise exploratória completa de 953 das músicas mais tocadas do Spotify, explorando padrões de sucesso, características musicais e tendências de lançamentos

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## 📋 Sobre o Projeto

Este projeto realiza uma análise exploratória completa de um dataset contendo os 953 artistas mais tocados do Spotify, investigando:

✅ Características acústicas das músicas (energia, dançabilidade, valência, acústica)  
✅ Padrões de presença em playlists nas principais plataformas (Spotify, Apple Music, Deezer, Shazam)  
✅ Distribuição de lançamentos ao longo do tempo  
✅ Correlações entre atributos musicais  
✅ Análise de artistas e tendências de sucesso  

**Dataset:** Spotify Most Streamed Songs (953 registros)  
**Período:** Múltiplos anos com concentração em 2020+  
**Variáveis:** 24 features (demográficas, streaming, características musicais)

---

## 🎯 Principais Insights

### 🌟 Insight #1: Spotify é a Vitrine Principal para Artistas
**Dados:** 
- Presença média em playlists Spotify: **32.8x maior** que Deezer
- Presença média em playlists Spotify: **6.2x maior** que Apple Music
- Forte correlação entre presença em playlists Spotify e número total de streams

**Implicação:** Artistas devem focar em estratégias de curação para playlists do Spotify, pois é o principal canal de distribuição e visibilidade musical.

---

### 🎬 Insight #2: 77% dos Hits Foram Lançados em 2022
**Dados:**
- Ano 2022 concentra **77%** das músicas mais tocadas no dataset
- Padrão observado: consumo musical concentrado em lançamentos **recentes**
- Picos de lançamento ocorrem em **abril-maio** (verão no hemisfério norte)

**Causa Provável:** Explosão do streaming pós-pandemia COVID-19 + eventos ao ar livre sazonais

**Oportunidade:** Meses de menor lançamento (agosto-setembro) representam janelas competitivas para novos artistas ganharem destaque com menos saturação de mercado.

---

### 💿 Insight #3: Correlação Forte entre Playlists e Streams
**Dados:**
- Correlação forte entre número de playlists e total de streams
- Presença em mais playlists = multiplicador significativo de reproduções

**Recomendação:** Investimento estratégico em:
- Parcerias com curadores de playlists
- Estratégias de pitching para plataformas
- Conteúdo visual complementar (clips, teasers)

---

### 🎸 Insight #4: Características Musicais de Hits
**Dados Estatísticos:**

| Característica | Média | Insight |
|---|---|---|
| **BPM (Ritmo)** | 122 BPM | Ritmo levemente acelerado é preferência |
| **Danceability** | 67% | Maioria das músicas tem alto potencial para dança |
| **Energy** | 64% | Alta intensidade sonora prevalece |
| **Valence (Positividade)** | Média moderada | Mix de temas positivos e melancólicos |
| **Acousticness** | Correlação -0.58 com Energy | Músicas energéticas usam produção eletrônica |

**Conclusão:** Não há um "atributo mágico" - múltiplos fatores contribuem para o sucesso.

---

### 👨‍🎤 Insight #5: Artistas Dominantes e Diversidade
**Dados:**
- **645 artistas únicos** em 953 músicas (média 1.47 faixas por artista)
- **Taylor Swift** lidera com maior número de faixas nos top hits
- **Não há monopólio genérico**: presença eclética de Pop, Hip-Hop, Reggaeton, R&B

**Conclusão:** Mercado musical é globalizado e diverso, mas alguns artistas (mega stars) conseguem dominância através de fanbase forte e consistência.

---

### 📊 Insight #6: Artistas Preferem Lançamentos Solo
**Dados:**
- **75% das músicas** são lançadas por um único artista
- Máximo de artistas por faixa: 8 (raro)
- Parcerias multiartistas ainda representam minoria

**Oportunidade:** Colaborações ainda oferecem diferencial competitivo.

---

## 📈 Dados Estatísticos Completos

### Resumo do Dataset

```
Total de Registros:        953 músicas
Artistas Únicos:           645
Nomes Únicos de Faixas:    943 (10 duplicadas/remixes)
Período de Cobertura:      1970-2024 (com foco 2020+)
Plataformas Analisadas:    Spotify, Apple Music, Deezer, Shazam
```

### Distribuição de Streams

| Métrica | Valor |
|---|---|
| **Média** | 513 milhões de streams |
| **Mediana** | ~400-500 milhões |
| **Mínimo** | 2,762 streams |
| **Máximo** | 3.7+ bilhões |
| **Desvio Padrão** | Muito alto (distribuição muito dispersa) |

**Interpretação:** Altíssima dispersão indica "winners vs losers" - poucas músicas ganham MUITO enquanto maioria tem número reduzido.

### Artistas Únicos e Representação

- **645 artistas** para **953 músicas**
- **Média:** 1.47 faixas por artista
- **Alguns artistas** aparecem múltiplas vezes (mega stars)
- **Maioria dos artistas** aparecem apenas 1-2 vezes

---

## 🛠️ Tecnologias Utilizadas

| Ferramenta | Propósito |
|---|---|
| **Python 3.9+** | Linguagem principal |
| **Jupyter Notebook** | Análise interativa |
| **Pandas** | Manipulação e transformação de dados |
| **NumPy** | Cálculos numéricos e análises |
| **Matplotlib** | Visualizações estáticas (gráficos) |
| **Seaborn** | Visualizações estatísticas avançadas |
| **Streamlit** (Opcional) | Dashboard interativo |

---

## 📊 Estrutura da Análise

### ✅ Fase 1: Exploração e Limpeza de Dados
- Carregamento do dataset de 953 registros
- Verificação de tipos de dados e estrutura
- Identificação de valores ausentes e anomalias
- **Descoberta:** Coluna 'streams' tinha valor corrupto que foi corrigido
- **Descoberta:** 10 faixas com mesmo número de streams (versões/remixes)

### ✅ Fase 2: Tratamento de Dados
- **Coluna 'streams':** Conversão string → numérico, correção de valor corrupto
- **Coluna 'in_deezer_playlists':** Conversão object → int
- **Valores Nulos:**
  - `in_shazam_charts`: Preenchido com 9999 (marcador de valores ausentes)
  - `key`: Preenchido com 'Miss_verificar' (marcador de valores ausentes)
- **Resultado:** Dataset 100% limpo, pronto para análise

### ✅ Fase 3: Análise Exploratória e Visualizações
**Análises Univariadas:**
- Distribuição de BPM, Danceability, Energy, Valence, Acousticness
- Distribuição de streams por artista
- Contagem de lançamentos por ano e mês

**Análises Bivariadas:**
- Correlação entre presença em playlists diferentes
- Relação Playlists × Streams (FORTE correlação)
- Heatmap de correlações musicais (Energy × Acousticness = -0.58)

**Análises Temporais:**
- Picos de lançamento (abril-maio)
- Distribuição por ano (concentração em 2022)
- Médias móveis de lançamentos

### ✅ Fase 4: Insights e Conclusões
- Consolidação de 6+ insights acionáveis
- Recomendações para artistas e produtoras
- Identificação de oportunidades de mercado

---

## 🔍 Principais Descobertas da Limpeza

### Anomalia #1: Valor Corrupto em 'Streams'
```
Localização: Linha 574
Valor Corrupto: "BPM110KeyAModeMajorDanceability53Valence75Energy69Acousticness7Instrumentalness0Liveness17Speechiness3"
Solução: Substituído por 0 (a linha foi descartada nas análises)
```

### Anomalia #2: Nomes de Faixas Duplicados
```
Total de registros: 953
Nomes únicos: 943
Duplicatas encontradas: 10

Causa: Versões/remixes/colaborações com nomes similares
Exemplo: "song_name" pode aparecer em versão original + remix + feat. outro artista
Ação: Mantidas para análise (representam o mercado real)
```

### Dados Ausentes Tratados
```
in_shazam_charts: ~6% de valores nulos → substituídos por 9999
in_apple_charts:  ~Mínimo de nulos
key:              ~10% de valores nulos → substituídos por 'Miss_verificar'
```

---

## 📁 Estrutura de Arquivos

```
spotify-eda/
├── README.md                           # Este arquivo
├── TECHNICAL_DOCS.md                   # Documentação técnica detalhada
├── requirements.txt                    # Dependências do projeto
│
├── notebooks/
│   └── EDA_Spotify.ipynb               # Análise exploratória completa
│
├── data/
│   ├── raw/
│   │   └── Spotify Most Streamed Songs.csv
│   └── processed/
│       └── spotify_cleaned.csv
│
├── src/
│   ├── data_loader.py                  # Carregar dados
│   ├── data_processor.py               # Limpeza e transformação
│   └── visualization.py                # Gráficos reutilizáveis
│
├── outputs/
│   ├── figures/                        # Gráficos exportados
│   │   ├── playlists_by_platform.png
│   │   ├── songs_by_year.png
│   │   └── musical_correlation.png
│   └── reports/
│       └── insights_summary.md
│
└── dashboard.py                        # Dashboard Streamlit (Bônus)
```

---

## ⚙️ Como Usar

### 1. Instalação de Dependências

```bash
# Clonar repositório
git clone https://github.com/seu-usuario/spotify-eda.git
cd spotify-eda

# Criar ambiente virtual (recomendado)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Instalar dependências
pip install -r requirements.txt
```

### 2. Executar o Notebook

```bash
jupyter notebook notebooks/EDA_Spotify.ipynb
```

### 3. Executar Dashboard (Opcional)

```bash
streamlit run dashboard.py
```

O dashboard abrirá em `http://localhost:8501`

---

## 📊 Visualizações Principais

### 1. **Presença em Playlists por Plataforma**
```
Spotify:       32.8x maior que Deezer
Apple Music:   6.2x maior que Deezer
Shazam:        Dados concentrados em top hits
Deezer:        Menor presença, possível viés geográfico
```

### 2. **Distribuição de Lançamentos por Ano**
```
2022:          ████████████████████ 77%
2021:          ██ 8%
2020:          █ 5%
Antes 2020:    █ 10%
```

### 3. **Lançamentos por Mês do Ano**
```
Pico:     Abril-Maio     (verão hemisfério norte)
Baixa:    Agosto-Sept    (oportunidade de mercado)
```

### 4. **Correlação Musical: Energy × Acousticness**
```
Correlação: -0.58 (moderada negativa)
Significado: Quanto mais energética a música, 
             menor a presença acústica
```

### 5. **Artistas Top 10**
```
1º. Taylor Swift      ████████
2º. [Artista X]       ██████
3º. [Artista Y]       █████
...
```

---

## 💡 Conclusões e Recomendações

### Para Artistas 🎤
1. **Priorize o Spotify** - É a vitrine principal (32.8x mais playlists que concorrentes)
2. **Lance em abril-maio** - Período de pico de consumo (verão)
3. **Invista em dança** - 67% dos hits tem alta dançabilidade
4. **Mantenha energia** - 64% das músicas têm alta intensidade
5. **Colabore** - Apenas 25% das faixas têm múltiplos artistas (diferencial)

### Para Produtoras 🎵
1. **Curadoria de Playlist** - Forte correlação com streams
2. **Estratégia Temporal** - Evitar saturação em meses de pico
3. **Diversidade de Gêneros** - Mercado é eclético (Pop, Hip-Hop, Reggaeton, R&B)
4. **Investimento em Mega Stars** - Poucos artistas capturam maioria dos streams
5. **Análise de Atributos** - Sem "fórmula mágica", mas padrões claros

### Para Pesquisadores 🔬
1. Explorar **causalidade** entre atributos (não apenas correlação)
2. Analisar **redes de colaborações** entre artistas
3. Estudar **evolução de gêneros** ao longo do tempo
4. Investigar **impacto de eventos sociais** (festival, prêmios, etc.)

---

## 🔮 Trabalhos Futuros

### Curto Prazo (1-2 semanas)
- [ ] Análise temporal: evolução de características ao longo dos anos
- [ ] Clustering de músicas similares (K-means, DBSCAN)
- [ ] Classificação de popularidade (música hit vs normal)

### Médio Prazo (1-2 meses)
- [ ] Modelo preditivo de sucesso musical
- [ ] Análise de sentimento de nomes de faixas
- [ ] Integração com API em tempo real do Spotify
- [ ] Dashboard interativo em produção

### Longo Prazo (2+ meses)
- [ ] Recomendador de músicas similar a Spotify
- [ ] Análise de redes sociais de artistas
- [ ] Previsão de tendências futuras
- [ ] Web app público com insights

---

## 📚 Variáveis do Dataset

### Informações Básicas
- **track_name:** Nome da música (943 únicos em 953 registros)
- **artist(s)_name:** Nome do(s) artista(s) (645 únicos)
- **artist_count:** Número de artistas (1-8, média 1.47)

### Informações Temporais
- **released_year:** Ano do lançamento (1970-2024, concentração 2020+)
- **released_month:** Mês do lançamento (1-12, picos abril-maio)
- **released_day:** Dia do lançamento (1-31)

### Métricas de Streaming
- **streams:** Total de reproduções (2.7K a 3.7B, média 513M)
- **in_spotify_playlists:** Presença em playlists Spotify (0-886)
- **in_spotify_charts:** Ranking nas paradas (0-82)
- **in_apple_playlists:** Presença em playlists Apple Music
- **in_apple_charts:** Ranking em Apple Music
- **in_deezer_playlists:** Presença em playlists Deezer
- **in_deezer_charts:** Ranking em Deezer
- **in_shazam_charts:** Ranking em Shazam

### Características Musicais (Audio Features)
- **bpm:** Batidas por minuto (ritmo) - Média: 122 BPM
- **key:** Tom da música (B, C#, F, A, D, etc.)
- **mode:** Maior (1) ou menor (0)
- **danceability_%:** Potencial de dança (0-100%) - Média: 67%
- **valence_%:** Positividade musical (0-100%)
- **energy_%:** Intensidade percebida (0-100%) - Média: 64%
- **acousticness_%:** Presença acústica (0-100%) - Correlação -0.58 com energy
- **instrumentalness_%:** Conteúdo instrumental (0-100%)
- **liveness_%:** Elementos de performance ao vivo (0-100%)
- **speechiness_%:** Quantidade de palavras faladas (0-100%)

---

## 🐛 Problemas Identificados e Soluções

| Problema | Localização | Solução |
|---|---|---|
| Valor corrupto em 'streams' | Linha 574 | Substituído por 0 |
| 'in_deezer_playlists' em formato texto | Coluna inteira | Conversão para numérico |
| Valores nulos em 'in_shazam_charts' | ~6% dos dados | Substituídos por 9999 |
| Valores nulos em 'key' | ~10% dos dados | Substituídos por 'Miss_verificar' |
| 10 faixas com mesmo número de streams | Dataset | Investigadas e mantidas (remixes legítimos) |

---

## 📖 Licença

Este projeto está sob a licença **MIT**. Veja arquivo `LICENSE` para detalhes.

---

## 🤝 Contribuições

Sugestões, melhorias e reports de bugs são bem-vindos!

1. Faça um **Fork** do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um **Pull Request**

---

## 📞 Contato

**Autor:** [Seu Nome]  
**LinkedIn:** [Seu LinkedIn](https://linkedin.com/in/seu-usuario)  
**GitHub:** [Seu GitHub](https://github.com/seu-usuario)  
**Email:** seu.email@exemplo.com

---

## 📚 Referências e Fontes

- [Spotify for Developers](https://developer.spotify.com/documentation/web-api)
- [Dataset - Spotify Most Streamed Songs 2023](https://www.kaggle.com/datasets/datasets)
- [Exploratory Data Analysis Guide](https://en.wikipedia.org/wiki/Exploratory_data_analysis)
- [Python Data Science Stack](https://pandas.pydata.org/docs/)

---

<div align="center">

**Análise Exploratória de Dados - Spotify**

Desenvolvido com ❤️ usando Python, Pandas e Matplotlib

*Última atualização: Março 2026*

⭐ Se este projeto foi útil, considere deixar uma estrela! ⭐

</div>
>>>>>>> 7d3e7b2 (estrutura inicial do projeto)
