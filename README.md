# 📊 Dashboard Câmara Municipal do Recife - Transparência

Dashboard interativo para análise de gastos com pessoal da Câmara Municipal do Recife, com dados carregados dinamicamente via Google Sheets.

## 🌐 Acesso

**[https://aristeuduarte.github.io/camara-recife-transparencia/](https://aristeuduarte.github.io/camara-recife-transparencia/)**

## ✨ Funcionalidades

- 📈 **Visão Geral**: Gráficos de evolução mensal, distribuição por categoria e gabinetes
- 🏛️ **Análise de Gabinetes**: Ranking de gastos por parlamentar
- 👥 **Lista de Servidores**: Busca, filtros e paginação
- 🏆 **Rankings**: Top salários e estatísticas por categoria
- 📥 **Exportação**: Download de dados em CSV
- 🔄 **Atualização em Tempo Real**: Dados carregados do Google Sheets

## 🔧 Configuração

### 1. Criar a Planilha no Google Sheets

1. Acesse [Google Sheets](https://sheets.google.com)
2. Crie uma nova planilha
3. Importe o arquivo `camara_recife_servidores_2025.csv`
4. A planilha deve ter as seguintes colunas:

| Coluna | Descrição |
|--------|-----------|
| Matricula | Número de matrícula do servidor |
| Nome | Nome completo |
| Categoria | Categoria funcional |
| Cargo | Cargo do servidor |
| Funcao | Função exercida |
| Bruto | Remuneração bruta |
| Liquido | Remuneração líquida |
| Lotacao | Local de lotação |
| Mes | Mês de referência |

### 2. Publicar a Planilha

1. No Google Sheets, vá em **Arquivo** → **Compartilhar** → **Publicar na Web**
2. Selecione a aba "Servidores" (ou a aba com os dados)
3. Formato: **Valores separados por vírgula (.csv)**
4. Clique em **Publicar**
5. Copie a URL gerada

### 3. Configurar o Dashboard

Edite o arquivo `index.html` e substitua a URL na linha:

```javascript
const GOOGLE_SHEETS_CSV_URL = 'COLE_SUA_URL_AQUI';
```

Exemplo de URL válida:
```javascript
const GOOGLE_SHEETS_CSV_URL = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vXXXXX/pub?output=csv';
```

### 4. Deploy no GitHub Pages

1. Faça commit das alterações
2. Vá em **Settings** → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** / **root**
5. Aguarde o deploy

## 📁 Estrutura

```
camara-recife-transparencia/
├── index.html          # Dashboard completo (single-file)
├── README.md           # Este arquivo
└── preview.png         # Imagem de preview para redes sociais
```

## 🔄 Atualizando os Dados

Para atualizar os dados:

1. Edite a planilha no Google Sheets
2. As alterações serão refletidas automaticamente no dashboard
3. Clique em "🔄 Atualizar Dados" no dashboard para recarregar

## 📊 Fonte dos Dados

Os dados são obtidos do [Portal da Transparência da Câmara Municipal do Recife](https://www.recife.pe.leg.br/transparencia).

## 🛠️ Tecnologias

- HTML5 / CSS3 / JavaScript
- [Chart.js](https://www.chartjs.org/) para gráficos
- Google Sheets como backend de dados
- GitHub Pages para hospedagem

## 📄 Licença

Este projeto é de código aberto para fins de transparência pública.

---

Desenvolvido por [Aristeu Duarte](https://github.com/aristeuduarte)
