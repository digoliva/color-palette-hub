# Color Palette Hub Pro 🎨

Uma aplicação web leve, moderna e responsiva para gerenciamento, criação e organização de paletas de cores orientadas ao design de dashboards e relatórios (como Power BI, Tableau, etc.).

---

## 📋 Conteúdo

- [Visão Geral](#-visão-geral)
- [Principais Funcionalidades](#-principais-funcionalidades)
- [Estrutura dos Arquivos](#-estrutura-dos-arquivos)
- [Como Usar](#-como-usar)
- [Estrutura de Dados e Importação/Exportação](#-estrutura-de-dados-e-importaçãoexportação)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)

---

## 🔍 Visão Geral

O **Color Palette Hub Pro** ajuda designers, analistas de dados e desenvolvedores a organizarem paletas de cores por contexto de aplicação (como títulos, fundos, cartões KPI e gráficos destaque). Além do gerenciamento de múltiplas paletas, a ferramenta conta com um gerador interativo de harmonias cromáticas.

---

## ✨ Principais Funcionalidades

- **Gerenciamento de Dashboards/Paletas:**
  - Criação de novos dashboards de cores.
  - Edição de nomes das paletas existentes.
  - Exclusão de paletas.
  - Alternância rápida entre diferentes conjuntos de cores.

- **Cadastro e Exibição de Cores:**
  - Inserção via código HEX.
  - Definição do local ou elemento de aplicação (ex: *Fundo do Dashboard*, *Título Principal*, *Cartão KPI*, etc.).
  - Sugestões automáticas de aplicação via campo preditivo.
  - Cópia instantânea da cor (HEX) para a área de transferência ao clicar sobre o cartão.

- **🎡 Gerador de Harmonia de Cores:**
  - Seleção por círculo cromático (*Color Wheel*).
  - Cálculo automático de harmonias cromáticas:
    - **Análogas**
    - **Monocromático**
    - **Tríade**
    - **Complementar**
  - Aplicação com um único clique direto na área de cadastro.

- **Persistência de Dados e Portabilidade:**
  - Salvamento automático das paletas no `localStorage` do navegador.
  - Exportação de dados da paleta em formato **JSON**.
  - Importação de arquivos JSON para rápida sincronização e compartilhamento de temas.

---

## 📁 Estrutura dos Arquivos

```text
.
├── index.html         # Código-fonte principal (HTML, CSS e JavaScript)
├── PaletaOF.json      # Exemplo de arquivo JSON contendo a paleta "Ourofino"
└── README.md          # Documentação do projeto
```

---

## 🚀 Como Usar

### 1. Executando a Aplicação
A aplicação é construída em um único arquivo HTML standalone. Para executá-la:
1. Faça o download ou clone o repositório.
2. Abra o arquivo `index.html` em qualquer navegador web moderno.

### 2. Adicionando Cores Manualmente
1. Informe um código hexadecimal válido (ex: `#072047`).
2. Digite ou selecione a aplicação da cor no relatório (ex: *Título Principal*).
3. Clique em **Adicionar**.

### 3. Usando a Roda de Cores (Gerador de Harmonia)
1. Clique no botão **🎡 Gerador de Cores** no menu lateral.
2. Clique no círculo central para selecionar a cor base.
3. Escolha uma das regras de harmonia (*Análogas*, *Monocromático*, *Tríade*, *Complementar*).
4. Clique na cor desejada para transferi-la automaticamente para o formulário.

### 4. Exportar / Importar
- **Exportar:** Abra a paleta desejada e clique em **📤 Exportar** no canto superior direito para baixar o arquivo `.json`.
- **Importar:** Clique em **📥 Importar** e selecione um arquivo de paleta `.json` válido (como o exemplo `PaletaOF.json`).

---

## 📊 Estrutura de Dados e Importação/Exportação

O arquivo JSON exportado/importado segue a seguinte estrutura:

```json
{
  "name": "Nome da Paleta",
  "colors": [
    {
      "id": 1780001196193,
      "hex": "#072047",
      "usage": "Azul escuro primário"
    },
    {
      "id": 1780001212738,
      "hex": "#10AD31",
      "usage": "Verde primário"
    }
  ]
}
```

---

## 🛠️ Tecnologias Utilizadas

- **HTML5:** Estruturação semântica.
- **CSS3:** Variáveis de estilo, CSS Grid, Flexbox e visual no estilo Dark Mode.
- **JavaScript (Vanilla):** Lógica da aplicação, cálculos de harmonias HSL/HEX, manipulação do DOM e persistência local via `localStorage`.