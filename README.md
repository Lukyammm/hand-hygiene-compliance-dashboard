# 🧼 HigieneM-os — Monitoramento de Higiene das Mãos (SCIH/HUC)

Sistema web para monitoramento operacional da adesão à higiene das mãos em ambiente hospitalar, com dados vindos de formulário e armazenados em Google Sheets.

---

## 📌 Descrição objetiva

O **HigieneM-os** é um WebApp em **Google Apps Script** que transforma respostas coletadas em formulário em um painel de gestão com:

- indicadores-chave (KPIs) em tempo real;
- filtros avançados por período, unidade, categoria profissional, momento e método;
- gráficos analíticos para acompanhamento de adesão;
- tabela detalhada para auditoria operacional.

É uma solução voltada para SCIH e lideranças assistenciais que precisam sair do acompanhamento manual e ganhar visão rápida, confiável e orientada à decisão.

---

## 🚨 Problema que o sistema resolve

Em rotinas hospitalares, o controle de higiene das mãos costuma sofrer com:

- planilhas extensas e de difícil leitura;
- consolidação manual e suscetível a erro;
- baixa velocidade para identificar quedas de adesão;
- dificuldade para comparar unidades, categorias e momentos críticos.

O sistema resolve esse cenário ao centralizar os dados em um **painel único**, com **classificação automática das ações**, cálculo de indicadores e visão histórica para apoiar decisões rápidas de educação, reforço de protocolo e gestão de risco assistencial.

---

## ✅ Principais funcionalidades

- **Leitura automática de dados** da planilha de respostas.
- **Normalização de registros** (padronização de texto e estrutura).
- **Classificação automática da ação** em:
  - Realizado;
  - Não realizado;
  - Incompleto.
- **Identificação do método** utilizado:
  - Água e sabonete;
  - Fricção com álcool;
  - Não informado.
- **KPIs operacionais**, incluindo:
  - total de observações;
  - adesão geral;
  - taxa de não realização;
  - completude do preenchimento.
- **Filtros combináveis** para análises direcionadas.
- **Gráficos de tendência e distribuição** para leitura gerencial.
- **Tabela analítica** para conferência e rastreabilidade.

---

## 🧰 Tecnologias utilizadas

- **Google Apps Script** (back-end e publicação do WebApp)
- **Google Sheets** (base de dados operacional)
- **HTML5 + JavaScript** (interface e lógica cliente)
- **Tailwind CSS** (layout e componentes visuais)
- **Chart.js** + `chartjs-plugin-datalabels` (visualização de dados)

---

## 🗂️ Estrutura do projeto

```text
HigieneM-os/
├── Code.gs         # Back-end (Apps Script): leitura, tratamento, filtros e métricas
├── index.html      # Front-end: dashboard, filtros, gráficos e tabela
├── README.md       # Documentação técnica/produto
└── PORTFOLIO.md    # Versão estratégica para apresentação
```

---

## 🔄 Fluxo de funcionamento

1. Observações são coletadas via formulário institucional.
2. As respostas chegam na aba de dados do Google Sheets.
3. O `Code.gs` lê os registros e aplica:
   - limpeza/padronização;
   - classificação da ação;
   - cálculo de KPIs;
   - montagem dos dados dos gráficos e tabela.
4. O `index.html` renderiza o dashboard com filtros e visões analíticas.
5. O usuário aplica filtros e recebe resultados atualizados em tempo real.

---

## 🖼️ Capturas de tela

> Substitua os caminhos abaixo pelos prints reais do projeto.

### Dashboard principal
![Dashboard principal](./docs/images/dashboard-principal.png)

### Filtros avançados
![Filtros avançados](./docs/images/filtros-avancados.png)

### Análises e gráficos
![Gráficos de adesão](./docs/images/graficos-adesao.png)

---

## ▶️ Como executar

### Pré-requisitos

- Conta Google com acesso ao Apps Script e Google Sheets.
- Planilha com estrutura compatível (timestamp, unidade, categoria, momento e ação).

### Passo a passo

1. Crie um projeto no **Google Apps Script**.
2. Copie o conteúdo de `Code.gs` para o arquivo `.gs` do projeto.
3. Copie o conteúdo de `index.html` para um arquivo HTML no projeto.
4. Ajuste as constantes no `Code.gs`:
   - `SPREADSHEET_ID`;
   - `SHEET_NAME`.
5. Clique em **Implantar > Nova implantação > Aplicativo da Web**.
6. Defina permissões de acesso conforme sua política institucional.
7. Abra a URL gerada e valide os dados no dashboard.

---

## 🚀 Melhorias futuras

- Controle de acesso por perfil (gestão, coordenação, auditoria).
- Exportação de relatórios em PDF/Excel por filtro aplicado.
- Alertas automáticos para queda de adesão por unidade.
- Série histórica com metas mensais e comparação com benchmark.
- Módulo de plano de ação com acompanhamento de status.

---

## 👤 Autor

Desenvolvido por **Mauricio** para suporte à gestão de higiene das mãos em ambiente hospitalar.

Se quiser, posso também preparar uma versão com arquitetura em camadas (config, serviços, métricas e UI) para facilitar evolução do produto.
