# Análise Descritiva de Acidentes em Minas Gerais (2020)

> Dashboard interativo desenvolvido em R e Quarto para análise de ocorrências, tipos de acidentes e condições de rodovias no estado de Minas Gerais durante o ano de 2020.

**[Acesse o Dashboard Interativo Online](https://avelarheitor.github.io/Projeto-Processo-Seletivo-EstatMG/)**
---

## Sobre o Projeto

Essa foi uma das etapas do processo seletivo da empresa júnior que trabalhei, foi pedido uma análise descritiva do banco em questão e o resultado foi extremamente satisfatório para mim, tendo em vista que foi meu primeiro contato mais forte com o R.

Este projeto analisa a base de dados de acidentes de trânsito ocorridos no estado de Minas Gerais no ano de 2020. A base conta com **6.536 ocorrências** e **14.052 pessoas envolvidas** (incluindo feridos leves, graves e óbitos).

### Objetivos:
- Mapear os tipos de acidentes mais frequentes.
- Identificar as rodovias (BRs) com maior número de acidentes.
- Avaliar a relação entre ocorrências, fatores climáticos, tipos de pista e distribuição por horário e dia da semana.

---

## Tecnologias Utilizadas

- **Linguagem**: [R](https://www.r-project.org/)
- **Relatório & Dashboard**: [Quarto](https://quarto.org/)
- **Estilização**: HTML5 e CSS3 customizado ([style.css](style.css))
- **Principais Pacotes R**:
  - `tidyverse` (`ggplot2`, `dplyr`, `forcats`, `lubridate`) — Manipulação e visualização de dados
  - `bslib` / `bsicons` — Componentes visuais e ícones do Dashboard
  - `leaflet` / `sf` / `geobr` — Mapeamento e dados geoespaciais
  - `reactable` / `kableExtra` — Tabelas interativas

---

## Estrutura do Repositório

```text
├── data/
│   ├── Acidentes_2020.xlsx      # Base de dados bruta
│   └── acidentes_2020_clean.rds # Base de dados tratada
├── index_files/                 # Arquivos de suporte do Dashboard HTML
├── .gitignore                   # Arquivos ignorados pelo versionamento Git
├── index.html                   # Dashboard compilado em HTML (GitHub Pages)
├── index.qmd                    # Código-fonte principal em Quarto
├── relatorio_final.Rproj        # Projeto do RStudio
└── style.css                    # Folha de estilo CSS do relatório
```

---

## Como Executar o Projeto Localmente

### Pré-requisitos
- **R** (versão 4.0 ou superior)
- **RStudio** (ou VS Code com extensão R/Quarto)
- **Quarto CLI**

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   cd SEU-REPOSITORIO
   ```

2. **Abra o projeto no RStudio:**
   Abra o arquivo `relatorio_final.Rproj`.

3. **Instale os pacotes necessários:**
   No console do R, execute:
   ```R
   if(!require(pacman)) install.packages("pacman")
   pacman::p_load(readxl, janitor, lubridate, tidyverse, reactable, 
                  bslib, bsicons, shiny, knitr, kableExtra, sf, 
                  geobr, leaflet, leaflet.extras, RColorBrewer, scales)
   ```

4. **Renderize o Dashboard:**
   Para compilar o relatório novamente, execute no terminal ou use o botão **Render** no RStudio:
   ```bash
   quarto render index.qmd
   ```

---

## Contato & Autoria

Projeto desenvolvido para o **Projeto EstatMG**.

- **Autor**: Heitor Pereira Avelar
- **GitHub**: [@avelarheitor](https://github.com/avelarheitor/)
- **LinkedIn**: [Heitor Avelar](https://linkedin.com/in/heitorpavelar)
- **Email**: heitorpereiraavelar@gmail.com
