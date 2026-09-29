# 🌐 Dashboard de Controle de Portas PON & CTOs - FTTH 2026

Dashboard interativo, moderno e responsivo desenvolvido para monitoramento de portas GPON/OLT e consulta de viabilidade de CTOs com base na planilha **"Controle CTO e PON - 2026"**.

---

## 🚀 Como Executar o Dashboard

Basta abrir o arquivo **`index.html`** em qualquer navegador moderno (Google Chrome, Microsoft Edge, Firefox, etc.):

1. Dê um duplo clique no arquivo: `c:\controlePON\index.html`
2. Ou via terminal:
   ```bash
   start c:\controlePON\index.html
   ```

---

## 📊 Principais Recursos do Dashboard

### 1. 📌 Indicadores Chave de Desempenho (KPIs)
- **Clientes Ativos**: Total de ONUs provisionadas e conectadas.
- **Capacidade Total**: Soma de todas as portas PON da OLT (68 portas × 128 = 8.704 portas).
- **Vagas Disponíveis**: Capacidade ociosa pronta para novas instalações e vendas.
- **Taxa de Ocupação Global**: Percentual de saturação da rede com barra visual.
- **Alertas de Atenção**: Contador de portas **🔴 Lotadas (0 vagas)** e **🟡 Quase Cheias (≤ 5 vagas)**.

### 2. 🔍 Buscador de Viabilidade de CTOs (Ideal para Vendas e Suporte)
- Digite parte do nome de qualquer caixa (ex: `AMARELA`, `ANDRADE`, `BELAVISTA`, `RESIDENCIAL`, `SCM`, `BENTO`, etc.).
- O sistema mostra em tempo real:
  - Qual a **Porta PON** e **Slot** correspondente;
  - Se a rota possui **vagas livres disponíveis**;
  - Capacidade atual da porta.

### 3. 🖥️ Visão Física da OLT (Chassi & Slots)
- Representação gráfica dos módulos/placas da OLT (**Slots 1, 2, 3, 4, 6, 8, 11 e 12**).
- Cada porta óptica possui um **LED luminoso** com status em tempo real:
  - 🟢 **Verde:** Livre com boa margem
  - 🟡 **Amarelo pulsante:** Quase cheia (≤ 5 vagas)
  - 🔴 **Vermelho pulsante:** 100% Lotada (0 vagas)
- Clique em qualquer porta para abrir a ficha completa com todas as CTOs interligadas.

### 4. 📈 Gráficos Analíticos (Chart.js)
- **Distribuição de Status**: Gráfico em rosca (Donut) com percentuais da rede.
- **Comparativo por Placa**: Gráfico em barras empilhadas mostrando Clientes Ativos vs Vagas por módulo da OLT.

### 5. 📋 Tabela Gerencial Dinâmica
- Filtros por **Placa** (Slot) e por **Status** (Livres, Quase Cheias, Lotadas).
- Botões de **filtros rápidos**: Apenas Lotadas, Quase Cheias, Livres ou Mais Vagas (> 50 vagas).
- **Ordenação clicável** por qualquer coluna (Placa, Clientes, Vagas, % Ocupação, Status).
- Chips visuais com nomes das CTOs em cada linha.

### 6. 🔄 Sincronização em Tempo Real com Google Sheets
- Botão **"Sincronizar Planilha"** no cabeçalho.
- Conecta diretamente à planilha oficial:
  [Planilha Google Sheets](https://docs.google.com/spreadsheets/d/1rWwViGvELZf6ZM5rnKngxbs0am7JFF-YJTj-9J2UvXg/edit?usp=sharing)
- **Fallback Automático:** Caso esteja offline ou sem conexão, utiliza a base de dados interna em `pon_data.js` sem interrupções.

### 7. 📥 Exportação de Relatórios
- **Exportar CSV/Excel**: Gera download de relatório com os dados e filtros atualmente aplicados.

---

## 📁 Estrutura de Arquivos

```
c:\controlePON\
├── index.html       # Aplicação web completa do dashboard
├── pon_data.js      # Base de dados estruturada em JavaScript (com fallback offline)
├── pon_data.json    # Dados em formato JSON puro para integrações externas
└── README.md        # Documentação e instruções de operação
```
