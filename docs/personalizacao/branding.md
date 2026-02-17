# Branding e Identidade Visual

Guia completo para adicionar sua marca e identidade visual ao AdminKit Pro.

## 🏷️ Logo e Marca

### Adicionar Logo Texto

Modifique o nome do projeto na sidebar:

```html
<a class="sidebar-brand" href="index.html">
  <span class="sidebar-brand-text align-middle">
    Seu Projeto
    <sup><small class="badge bg-primary text-uppercase">Tag</small></sup>
  </span>
</a>
```

### Adicionar Logo Imagem

#### 1. Adicionar Arquivo do Logo

Coloque seu logo em `img/logo.svg` ou `img/logo.png`:

```bash
# Estrutura recomendada
img/
├── logo.svg          # Logo principal (vetor)
├── logo-white.svg    # Logo para fundo escuro
├── favicon.png       # Favicon
└── logo-icon.svg     # Ícone da marca
```

#### 2. Integrar no HTML

```html
<a class="sidebar-brand" href="index.html">
  <img src="img/logo.svg" alt="Seu Projeto" height="32">
</a>
```

### Logo Responsivo

```html
<a class="sidebar-brand" href="index.html">
  <!-- Logo completo em sidebar expandida -->
  <img src="img/logo.svg" alt="Logo" class="logo-expanded">
  <!-- Ícone em sidebar colapsada -->
  <img src="img/logo-icon.svg" alt="Logo" class="logo-collapsed">
</a>
```

### Logo com Badge

```html
<a class="sidebar-brand" href="index.html">
  <span class="sidebar-brand-text align-middle">
    Seu Projeto
    <sup>
      <small class="badge bg-primary text-uppercase">Pro</small>
    </sup>
  </span>
  <svg class="sidebar-brand-icon align-middle" width="32px" height="32px">
    <!-- Seu ícone SVG -->
  </svg>
</a>
```

## 🎨 Favicon

### Criar Favicon

1. Use uma ferramenta como [favicon.io](https://favicon.io/)
2. Gere os tamanhos: 16x16, 32x32, 48x48
3. Salve em `img/icons/`

### Integrar Favicon

```html
<link rel="shortcut icon" href="img/icons/icon-48x48.png" />
<link rel="icon" type="image/png" sizes="16x16" href="img/icons/icon-16x16.png">
<link rel="icon" type="image/png" sizes="32x32" href="img/icons/icon-32x32.png">
```

### Favicon Moderno (SVG)

```html
<link rel="icon" type="image/svg+xml" href="img/icons/favicon.svg">
```

## 📝 Títulos e Metadados

### Título da Página

```html
<head>
  <title>Seu Projeto - Dashboard</title>
</head>
```

### Meta Descrição

```html
<meta name="description" content="Descrição do seu projeto em português">
```

### Palavras-chave

```html
<meta name="keywords" content="seu-projeto, dashboard, admin, bootstrap">
```

### Open Graph (Compartilhamento)

```html
<meta property="og:title" content="Seu Projeto">
<meta property="og:description" content="Descrição para redes sociais">
<meta property="og:image" content="https://seusite.com/img/og-image.png">
<meta property="og:url" content="https://seusite.com/">
<meta property="og:type" content="website">
```

## 🌐 Cores da Marca

### Definir Paleta de Cores

```css
:root {
  /* Cores Primárias */
  --primary: #2563eb;
  --primary-hover: #1d4ed8;
  --primary-light: #dbeafe;
  --primary-dark: #1e40af;

  /* Cores Secundárias */
  --secondary: #7c3aed;
  --secondary-hover: #6d28d9;
  --secondary-light: #ede9fe;

  /* Cores de Acento */
  --accent: #f59e0b;
  --accent-hover: #d97706;
  --accent-light: #fef3c7;

  /* Cores Neutras */
  --gray-50: #f9fafb;
  --gray-100: #f3f4f6;
  --gray-200: #e5e7eb;
  --gray-300: #d1d5db;
  --gray-400: #9ca3af;
  --gray-500: #6b7280;
  --gray-600: #4b5563;
  --gray-700: #374151;
  --gray-800: #1f2937;
  --gray-900: #111827;
}
```

### Aplicar Cores da Marca

```css
/* Botões */
.btn-primary {
  background-color: var(--primary);
  border-color: var(--primary);
}

.btn-primary:hover {
  background-color: var(--primary-hover);
  border-color: var(--primary-hover);
}

/* Links */
a {
  color: var(--primary);
}

a:hover {
  color: var(--primary-hover);
}

/* Badges */
.badge-primary {
  background-color: var(--primary);
}
```

## 🔤 Tipografia da Marca

### Escolher Fonte

```html
<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

### Aplicar Fonte

```css
:root {
  --font-family-base: 'Inter', system-ui, -apple-system, sans-serif;
  --font-family-heading: 'Inter', system-ui, -apple-system, sans-serif;
  --font-family-monospace: 'SF Mono', 'Roboto Mono', monospace;
}

body {
  font-family: var(--font-family-base);
}

h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-family-heading);
}
```

### Hierarquia Tipográfica

```css
/* Títulos */
h1 { font-size: 2.5rem; font-weight: 700; }
h2 { font-size: 2rem; font-weight: 600; }
h3 { font-size: 1.75rem; font-weight: 600; }
h4 { font-size: 1.5rem; font-weight: 600; }
h5 { font-size: 1.25rem; font-weight: 500; }
h6 { font-size: 1rem; font-weight: 500; }

/* Texto */
.display-1 { font-size: 6rem; font-weight: 700; }
.display-2 { font-size: 5.5rem; font-weight: 700; }
.display-3 { font-size: 4.5rem; font-weight: 700; }
.display-4 { font-size: 3.5rem; font-weight: 700; }
```

## 🎯 Identidade Visual Consistente

### Componentes Customizados

```css
/* Cards com borda colorida */
.card-branded {
  border-left: 4px solid var(--primary);
}

/* Botões com gradiente */
.btn-gradient {
  background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
  border: none;
  color: white;
}

/* Headers de seção */
.section-header {
  border-bottom: 2px solid var(--primary);
  padding-bottom: 0.5rem;
  margin-bottom: 1.5rem;
}
```

### Ícones da Marca

Use ícones consistentes com sua marca:

```html
<!-- Ícone SVG inline -->
<svg class="brand-icon" width="24" height="24" viewBox="0 0 24 24" fill="var(--primary)">
  <!-- Seu ícone -->
</svg>
```

## 📱 Manifesto de Aplicação (PWA)

### Criar manifest.json

```json
{
  "name": "Seu Projeto",
  "short_name": "Projeto",
  "description": "Descrição do projeto",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#2563eb",
  "icons": [
    {
      "src": "img/icons/icon-192x192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "img/icons/icon-512x512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

### Linkar no HTML

```html
<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#2563eb">
```

## 🎨 Exemplos de Branding

### Exemplo 1: Tecnologia

```css
:root {
  --primary: #3b82f6;      /* Azul tech */
  --secondary: #8b5cf6;    /* Roxo inovação */
  --accent: #06b6d4;       /* Ciano futurista */
}
```

### Exemplo 2: Finanças

```css
:root {
  --primary: #059669;      /* Verde confiança */
  --secondary: #0d9488;    /* Teal estabilidade */
  --accent: #f59e0b;       /* Laranja destaque */
}
```

### Exemplo 3: Saúde

```css
:root {
  --primary: #0ea5e9;      /* Azul saúde */
  --secondary: #10b981;    /* Verde bem-estar */
  --accent: #f43f5e;       /* Rosa urgência */
}
```

### Exemplo 4: E-commerce

```css
:root {
  --primary: #f43f5e;      /* Rosa destaque */
  --secondary: #8b5cf6;    /* Roxo premium */
  --accent: #f59e0b;       /* Laranja oferta */
}
```

## 🔧 Ferramentas de Branding

### Geradores de Logo

- [Canva](https://www.canva.com/) - Criar logos facilmente
- [LogoMaker](https://logomaker.com/) - Gerador automático
- [Hatchful](https://hatchful.shopify.com/) - Logos gratuitos

### Geradores de Paleta

- [Coolors](https://coolors.co/) - Gerar paletas harmoniosas
- [Adobe Color](https://color.adobe.com/pt/) - Criar temas
- [Paletton](https://paletton.com/) - Combinações de cores

### Ferramentas de Favicon

- [favicon.io](https://favicon.io/) - Gerador completo
- [RealFaviconGenerator](https://realfavicongenerator.net/) - Favicon avançado

## ✅ Checklist de Branding

- [ ] Logo criado e adicionado
- [ ] Favicon configurado
- [ ] Cores da marca definidas
- [ ] Tipografia escolhida
- [ ] Títulos e metadados atualizados
- [ ] Open Graph configurado
- [ ] Manifesto PWA criado
- [ ] Consistência visual verificada

## 📚 Recursos Relacionados

- [Temas e Cores](temas-cores.md)
- [Layout e Estrutura](layout-estrutura.md)
- [Internacionalização](traducao-i18n.md)

---

**Próximo:** [Tradução e Internacionalização](traducao-i18n.md)

**Versão:** 1.0.0
**Última atualização:** 2026-02-17
