# Temas e Cores

Guia completo de personalização de temas e cores no AdminKit Pro.

## 🎨 Temas Disponíveis

O AdminKit Pro inclui 4 temas pré-configurados:

| Tema | Arquivo CSS | Características |
|------|-------------|-----------------|
| **Default** | light.css | Tema principal com cores equilibradas |
| **Dark** | dark.css | Tema escuro para redução de cansaço visual |
| **Light** | light.css | Variante clara minimalista |
| **Colored** | light.css | Tema com cores vibrantes |

### Como Alternar Temas

#### Método 1: Data Attribute (Recomendado)

```html
<!-- No elemento body -->
<body data-theme="dark">
```

#### Método 2: Trocar Arquivo CSS

```html
<!-- Tema Light -->
<link class="js-stylesheet" href="css/light.css" rel="stylesheet">

<!-- Tema Dark -->
<link class="js-stylesheet" href="css/dark.css" rel="stylesheet">
```

#### Método 3: JavaScript

```javascript
// Alternar para tema dark
document.body.setAttribute('data-theme', 'dark');

// Alternar para tema light
document.body.setAttribute('data-theme', 'light');
```

## 🎭 Variáveis de Cor

O AdminKit Pro usa variáveis CSS para facilitar a personalização:

### Variáveis Principais (Light Theme)

```css
:root {
  /* Cores Primárias */
  --primary: #435ebe;
  --primary-light: #eef1ff;
  --primary-dark: #2c3b82;

  /* Cores de Estado */
  --success: #31a367;
  --success-light: #dcfce7;
  --warning: #f7c942;
  --warning-light: #fef9c3;
  --danger: #e63757;
  --danger-light: #ffe2e6;
  --info: #3b82f6;
  --info-light: #dbeafe;

  /* Cores Neutras */
  --gray-100: #f3f4f6;
  --gray-200: #e5e7eb;
  --gray-300: #d1d5db;
  --gray-400: #9ca3af;
  --gray-500: #6b7280;
  --gray-600: #4b5563;
  --gray-700: #374151;
  --gray-800: #1f2937;
  --gray-900: #111827;

  /* Cores de Fundo */
  --white: #ffffff;
  --black: #000000;
  --body-bg: #f3f4f6;
  --card-bg: #ffffff;

  /* Cores de Texto */
  --text-primary: #1f2937;
  --text-secondary: #6b7280;
  --text-muted: #9ca3af;
}
```

### Variáveis do Dark Theme

```css
[data-theme="dark"] {
  --body-bg: #111827;
  --card-bg: #1f2937;
  --text-primary: #f9fafb;
  --text-secondary: #d1d5db;
  --text-muted: #9ca3af;
  --gray-100: #1f2937;
  --gray-200: #374151;
  --gray-300: #4b5563;
}
```

## 🖌️ Criar um Tema Customizado

### Passo 1: Copiar um Tema Existente

```bash
# Copiar o tema light como base
cp css/light.css css/custom.css
```

### Passo 2: Modificar as Variáveis

No arquivo `custom.css`, localize as variáveis CSS e modifique conforme necessário:

```css
:root {
  /* Sua marca principal */
  --primary: #2563eb;
  --primary-light: #dbeafe;
  --primary-dark: #1e40af;

  /* Outras cores da sua marca */
  --secondary: #7c3aed;
  --accent: #f59e0b;
}
```

### Passo 3: Usar o Tema Customizado

```html
<link href="css/custom.css" rel="stylesheet">
```

## 🌈 Esquemas de Cores Populares

### Azure (Nuvens/SaaS)

```css
:root {
  --primary: #0ea5e9;
  --primary-light: #e0f2fe;
  --primary-dark: #0284c7;
}
```

### Emerald (Finanças)

```css
:root {
  --primary: #10b981;
  --primary-light: #d1fae5;
  --primary-dark: #059669;
}
```

### Purple (SaaS Premium)

```css
:root {
  --primary: #8b5cf6;
  --primary-light: #ede9fe;
  --primary-dark: #7c3aed;
}
```

### Rose (E-commerce/Beleza)

```css
:root {
  --primary: #f43f5e;
  --primary-light: #ffe4e6;
  --primary-dark: #e11d48;
}
```

## 🔄 Animações e Transições

O AdminKit Pro inclui transições suaves para mudanças de tema:

```css
/* Transição suave entre temas */
body {
  transition: background-color 0.3s ease, color 0.3s ease;
}

/* Cards e containers */
.card, .navbar, .sidebar {
  transition: background-color 0.3s ease, border-color 0.3s ease;
}
```

## 🎯 Melhores Práticas

### 1. Mantenha Contraste Adequado

Certifique-se de que o texto permaneça legível em todos os temas:

```css
/* Bom contraste */
--text-primary: #1f2937; /* escuro sobre fundo claro */
--text-primary: #f9fafb; /* claro sobre fundo escuro */

/* Evite */
--text-primary: #9ca3af; /* pouco contraste */
```

### 2. Use Cores Consistentes

Mantenha a semântica das cores em todo o projeto:

- Primary: ação principal
- Success: confirmações
- Warning: alertas
- Danger: erros/destrutivas
- Info: informações neutras

### 3. Teste em Diferentes Contextos

Verifique suas cores em:
- Luz natural
- Luz artificial
- Telas de diferentes qualidades
- Modos de alto contraste

## 🔍 Ferramentas Úteis

### Geradores de Paleta

- **[Coolors](https://coolors.co/)** - Gerar paletas harmoniosas
- **[Adobe Color](https://color.adobe.com/pt/)** - Criar e explorar temas
- **[Material Design Colors](https://material.io/resources/color/)** - Paletas acessíveis

### Verificadores de Contraste

- **[WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)** - Verificar WCAG
- **[Contrast Ratio](https://contrast-ratio.com/)** - Calcular contraste

## 📝 Exemplo Completo

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Projeto - Tema Customizado</title>

  <link href="css/light.css" rel="stylesheet">
  <style>
    /* Personalização específica do projeto */
    :root {
      --primary: #2563eb;
      --primary-light: #dbeafe;
      --primary-dark: #1e40af;
    }
  </style>
</head>
<body data-theme="default">
  <!-- Seu conteúdo -->
</body>
</html>
```

---

**Próximo:** [Layout e Estrutura](layout-estrutura.md)

**Versão:** 1.0.0
**Última atualização:** 2026-02-17
