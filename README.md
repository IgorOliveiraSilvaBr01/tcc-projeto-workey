# WorKey - Documentação Técnica

## Protótipo

**Figma:**

https://www.figma.com/design/prWMh7uwTX5kOfw5q1GWFK/Landpage----WorKey?node-id=8-439&t=B4e4tEtRcSMVBSRM-1

---

# Visão Geral

O projeto **WorKey** consiste em uma landing page desenvolvida para apresentar a plataforma WorKey, seus benefícios e funcionalidades.

O desenvolvimento foi realizado utilizando tecnologias front-end modernas, priorizando organização de código, componentização visual e manutenção simplificada.

## Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript
- Figma
- Git
- GitHub
- Visual Studio Code

---

# Estrutura do Projeto

```text
tcc-projeto-workey/

│
├── index.html
│
├── README.md
│
└── src/
    │
    ├── assets/
    │   └── images/
    │
    ├── css/
    │   ├── style.css
    │   ├── global.css
    │   ├── header.css
    │   ├── hero.css
    │   ├── main.css
    │   ├── statiscs.css
    │   ├── contact.css
    │   ├── faq.css
    │   └── footer.css
    │
    └── javascript/
        └── accordion.js
```

---

# Arquivo Principal

## index.html

O arquivo `index.html` é responsável por toda a estrutura da página e pela organização das seções apresentadas ao usuário.

As principais seções são:

### Header

Responsável pela navegação principal da aplicação.

**Elementos:**

- Logotipo da WorKey
- Nome da plataforma
- Menu de navegação
- Botões de autenticação

---

### Hero Section

Primeira área visual exibida ao usuário.

**Objetivos:**

- Apresentar a proposta da plataforma.
- Captar a atenção do visitante.
- Direcionar para o cadastro.

**Componentes:**

- Título principal
- Texto descritivo
- Botões de ação
- Imagem ilustrativa

---

### About Section

Seção responsável por apresentar o funcionamento da plataforma.

**Estrutura:**

- Título da seção
- Descrição
- Cards explicativos

**Cards:**

1. Adicione seus links.
2. Crie seu portfólio.
3. Conecte-se com oportunidades.

---

### Statistics Section

Apresenta indicadores da plataforma por meio de cards informativos.

**Componentes:**

- Ícone
- Valor numérico
- Descrição

---

### FAQ Section

Seção destinada às perguntas frequentes.

Possui comportamento interativo implementado através de JavaScript utilizando o padrão Accordion.

---

### Contact Section

Área destinada ao contato entre usuários e plataforma.

**Elementos:**

- Formulário
- Campos de entrada
- Informações visuais

---

### Footer

Rodapé da aplicação.

**Conteúdo:**

- Redes sociais
- Informações institucionais
- Direitos autorais

---

# Arquivos CSS

O projeto utiliza uma arquitetura modular de estilos.

Cada arquivo possui uma responsabilidade específica.

---

## style.css

Arquivo responsável por centralizar a importação de todos os demais estilos.

```css
@import url(./global.css);
@import url(./header.css);
@import url(./hero.css);
@import url(./main.css);
@import url(./statiscs.css);
@import url(./contact.css);
@import url(./faq.css);
@import url(./footer.css);
```

---

## global.css

Responsável pelas configurações globais da aplicação.

### Funções

- Reset CSS
- Variáveis globais
- Fontes
- Configurações padrão

### Principais recursos

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

Também concentra:

- Paleta de cores
- Fontes
- Espaçamentos
- Variáveis reutilizáveis

---

## header.css

Responsável pela estilização do cabeçalho.

### Controla

- Navegação
- Logo
- Botões
- Espaçamentos
- Responsividade

### Classes principais

```css
.home
.header-group
.btn-group
```

---

## hero.css

Responsável pela seção principal da página.

### Controla

- Layout em colunas
- Tipografia principal
- Botões CTA
- Imagens

### Classes principais

```css
.hero
.content-hero
.hero-title
.hero-ad
```

---

## main.css

Responsável pela seção de apresentação da plataforma.

### Controla

- Cards informativos
- Textos
- Estrutura da seção

### Classes principais

```css
.about
.about-content
.cards
.text
```

---

## statiscs.css

Responsável pela exibição dos indicadores da plataforma.

### Controla

- Cards estatísticos
- Ícones
- Alinhamento
- Espaçamento

### Classes principais

```css
.statistics-section
.statistics-card
```

---

## faq.css

Responsável pela aparência e comportamento visual do FAQ.

### Controla

- Accordion
- Perguntas
- Respostas
- Estados de exibição

### Classes principais

```css
.faq-section
.faq-content
.active
```

---

## contact.css

Responsável pela seção de contato.

### Controla

- Formulário
- Inputs
- Layout
- Espaçamentos

### Classes principais

```css
.contact-section
.contact-content
.contact-form
```

---

## footer.css

Responsável pelo rodapé da página.

### Controla

- Links
- Redes sociais
- Informações institucionais

### Classes principais

```css
.footer
.footer-content
.footer-social
```

---

# JavaScript

## accordion.js

Arquivo responsável pelo comportamento interativo da seção FAQ.

### Objetivo

Permitir que perguntas sejam abertas e fechadas dinamicamente.

### Funcionamento

1. Seleciona todos os elementos do FAQ.
2. Adiciona eventos de clique.
3. Alterna a classe responsável pela exibição da resposta.

### Exemplo

```javascript
const accordions = document.querySelectorAll('.accordion');

accordions.forEach(accordion => {
    accordion.addEventListener('click', () => {
        accordion.classList.toggle('active');
    });
});
```

---

# Recursos Visuais

## SVG

O projeto utiliza imagens vetoriais SVG para:

- Ícones
- Ilustrações
- Logotipos

### Benefícios

- Alta qualidade
- Baixo peso
- Escalabilidade

---

## Google Fonts

Fontes utilizadas no projeto:

- Montserrat
- Roboto

Aplicadas em:

- Títulos
- Textos
- Botões

---

# Fluxo de Carregamento

```text
index.html
    ↓
style.css
    ↓
Arquivos CSS específicos
    ↓
Imagens SVG
    ↓
accordion.js
    ↓
Página pronta para uso
```

---

# Considerações Técnicas

O projeto foi estruturado utilizando separação de responsabilidades, onde cada seção possui seus próprios estilos e componentes visuais.

Essa organização proporciona:

- Maior legibilidade do código;
- Facilidade de manutenção;
- Melhor escalabilidade;
- Reutilização de componentes;
- Organização adequada para projetos front-end.

A utilização de HTML semântico, CSS modular e JavaScript puro garante um sistema leve, performático e de fácil entendimento para futuras manutenções.
