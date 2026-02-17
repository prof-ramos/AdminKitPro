# Guia de Personalização do AdminKit Pro

Aprenda a personalizar o AdminKit Pro para atender às necessidades específicas do seu projeto.

## 📋 Índice

- [Cores e Temas](#cores-e-temas)
- [Tipografia](#tipografia)
- [Layout](#layout)
- [Componentes](#componentes)
- [Logo e Branding](#logo-e-branding)
- [Personalização Avançada](#personalização-avançada)

---

## 🎨 Cores e Temas

### Temas Predefinidos

O AdminKit Pro vem com 4 temas pré-configurados:

- **Default** - Tema principal com azul e cinza
- **Light** - Variação clara minimalista
- **Dark** - Tema escuro para redução de fadiga visual
- **Colored** - Tema colorido com acentos vibrantes

### Alterar Variáveis de Cor

As cores são definidas através de variáveis CSS. Você pode sobrescrevê-las:

```css
:root {
  /* Cores Principais */
  --primary: #435ebe;
  --secondary: #6c757d;
  --success: #38c27a;
  --danger: #de0430;
  --warning: #ffc107;
  --info: #0dcaf0;
  --light: #f9fafb;
  --dark: #212529;

  /* Cores do Template */
  --bs-body-bg: #f5f7fb;
  --bs-body-color: #3d4655;

  /* Sidebar */
  --sidebar-bg: #2c3e50;
  --sidebar-color: #ffffff;
}
```

### Criar um Tema Customizado

1. Copie `css/light.css` ou `css/dark.css`
2. Renomeie para `css/custom.css`
3. Altere as variáveis CSS
4. Importe no HTML:

```html
<link href="css/custom.css" rel="stylesheet">
```

---

## 🔤 Tipografia

### Fontes Utilizadas

O AdminKit usa **Inter** como fonte principal:

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
```

### Alterar a Fonte

Para usar uma fonte diferente:

1. **Importe a fonte** no `<head>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
```

2. **Altere a variável CSS**:

```css
:root {
  --font-family-base: 'Roboto', sans-serif;
  --font-family-sans-serif: 'Roboto', sans-serif;
}
```

3. **Ou sobrescreva com CSS customizado**:

```css
body {
  font-family: 'Roboto', sans-serif !important;
}
```

### Tamanhos de Fonte

```css
:root {
  --font-size-base: 0.9375rem;
  --font-size-lg: 1rem;
  --font-size-sm: 0.875rem;
}
```

---

## 📐 Layout

### Layout Fluid (Padrão)

O conteúdo ocupa toda a largura disponível:

```html
<body data-layout="fluid">
```

### Layout Boxed

O conteúdo é limitado a uma largura máxima:

```html
<body data-layout="boxed">
```

### Alterar Largura Máxima (Boxed)

```css
@media (min-width: 1400px) {
  body[data-layout="boxed"] .wrapper {
    max-width: 1320px;
    margin: 0 auto;
  }
}
```

---

## 🧩 Componentes

### Sidebar

#### Posição

```html
<!-- Sidebar à esquerda (padrão) -->
<body data-sidebar-position="left">

<!-- Sidebar à direita -->
<body data-sidebar-position="right">
```

#### Tamanho

```html
<!-- Sidebar completa (padrão) -->
<body data-sidebar-layout="default">

<!-- Sidebar compacta -->
<body data-sidebar-layout="compact">
```

#### Largura Customizada

```css
.sidebar {
  --sidebar-width: 280px; /* Padrão: 250px */
}
```

### Navbar

#### Altura

```css
.navbar {
  --navbar-height: 60px; /* Padrão */
}
```

#### Cor de Fundo

```css
.navbar {
  background-color: #sua-cor !important;
}
```

### Cards

#### Border Radius

```css
.card {
  --card-border-radius: 0.5rem;
}
```

#### Sombras

```css
.card {
  box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}
```

---

## 🏷️ Logo e Branding

### Alterar o Logo

#### Logo Baseado em Texto

```html
<a class="sidebar-brand" href="index.html">
  <span class="sidebar-brand-text align-middle">
    Seu Projeto
  </span>
</a>
```

#### Logo com Imagem

```html
<a class="sidebar-brand" href="index.html">
  <img src="img/logo.svg" alt="Logo" height="32">
</a>
```

### Favicon

Substitua o arquivo `img/icons/icon-48x48.png` pelo seu favicon.

### Título da Página

Altere a tag `<title>` em cada arquivo HTML:

```html
<title>Seu Projeto - Dashboard</title>
```

---

## ⚡ Personalização Avançada

### CSS Customizado

Crie um arquivo `css/custom.css` e importe após o tema:

```html
<link href="css/light.css" rel="stylesheet">
<link href="css/custom.css" rel="stylesheet">
```

### Sobrescrever Estilos

```css
/* Para sobrescrever estilos específicos */
.card-custom {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.btn-primary {
  background-color: #sua-cor;
  border-color: #sua-cor;
}
```

### JavaScript Customizado

Adicione seu código em `js/custom.js`:

```javascript
// Seu código customizado
document.addEventListener('DOMContentLoaded', function() {
  // Sua lógica aqui
});
```

Importe no HTML antes de fechar `</body>`:

```html
<script src="js/app.js"></script>
<script src="js/custom.js"></script>
```

---

## 🎯 Exemplos de Personalização

### Dashboard Minimalista

```css
/* Remover sombras */
.card {
  box-shadow: none !important;
  border: 1px solid #e3e6f0;
}

/* Background mais claro */
body {
  background-color: #f8f9fa !important;
}
```

### Tema Escuro Customizado

```css
/* Sobrescrever cores do tema dark */
[data-theme="dark"] {
  --primary: #5a8dee;
  --bs-body-bg: #1a1d2d;
  --bs-body-color: #e2e8f0;
}
```

### Cores de Marca

```css
/* Substituir azul padrão por sua cor */
:root {
  --primary: #FF5722; /* Laranja */
  --primary-hover: #E64A19;
  --primary-light: #FFCCBC;
}
```

---

## 🔧 Ferramentas Úteis

### Inspetor de Navegador

Use o inspetor para experimentar mudanças antes de aplicá-las:

1. Clique com o botão direito → "Inspecionar"
2. Encontre o elemento que deseja modificar
3. Edite os estilos no painel "Styles"
4. Copie o CSS final para seu arquivo customizado

### Geradores de Cores

- [Coolors](https://coolors.co/) - Gerar paletas de cores
- [Adobe Color](https://color.adobe.com/) - Criar temas de cores
- [Gradient Hunt](https://gradienthunt.com/) - Gradientes CSS

### Editores de Sombra

- [Box Shadow Generator](https://cssgenerator.org/box-shadow-css-generator.html)
- [Smooth Shadow](https://smoothshadow.com/)

---

## 📚 Recursos Relacionados

- [Configuração de Temas](../guia-de-inicio/configuracao.md)
- [Variáveis de Customização](../guia-de-inicio/variaveis.md)
- [Documentação de Componentes](../componentes/)
- [Exemplos de Uso](../exemplos/)

---

## 🤝 Contribuindo

Tem uma dica de personalização para compartilhar?

1. Documente o exemplo
2. Inclua código funcional
3. Envie um Pull Request

Consulte o [CONTRIBUTING.md](../../CONTRIBUTING.md) para mais detalhes.

---

<div align="center">

**Próximo**: [Configuração de Temas](../guia-de-inicio/configuracao.md) • **Anterior**: [Exemplos](../exemplos/)

[⬆ Voltar ao topo](#guia-de-personalização-do-adminkit-pro)

</div>
