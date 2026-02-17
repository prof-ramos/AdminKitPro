# Layout e Estrutura

Guia completo de configuração de layout e estrutura no AdminKit Pro.

## 🏗️ Estrutura Base

O AdminKit Pro usa uma estrutura HTML bem definida:

```html
<body data-theme="default" data-layout="fluid" data-sidebar-position="left" data-sidebar-layout="default">
  <div class="wrapper">
    <!-- Sidebar -->
    <nav id="sidebar" class="sidebar js-sidebar">
      <!-- Conteúdo da sidebar -->
    </nav>

    <!-- Conteúdo Principal -->
    <div class="main">
      <!-- Navbar -->
      <nav class="navbar navbar-expand navbar-light navbar-bg">
        <!-- Conteúdo da navbar -->
      </nav>

      <!-- Conteúdo da Página -->
      <main class="content">
        <div class="container-fluid p-0">
          <!-- Seu conteúdo -->
        </div>
      </main>

      <!-- Footer -->
      <footer class="footer">
        <!-- Conteúdo do footer -->
      </footer>
    </div>
  </div>
</body>
```

## 📐 Tipos de Layout

### Layout Fluid (Padrão)

O layout fluid ocupa toda a largura disponível:

```html
<body data-layout="fluid">
```

**Características:**
- Largura total da viewport
- Ideal para dashboards e aplicações internas
- Melhor aproveitamento de espaço

### Layout Boxed

O layout boxed limita o conteúdo a uma largura máxima:

```html
<body data-layout="boxed">
```

**Características:**
- Conteúdo centralizado
- Largura máxima definida
- Ideal para apresentações e páginas públicas

### Customizar Largura Boxed

```css
/* No seu CSS customizado */
body[data-layout="boxed"] .wrapper {
  max-width: 1440px;
  margin: 0 auto;
}
```

## 📱 Posição da Sidebar

### Sidebar à Esquerda (Padrão)

```html
<body data-sidebar-position="left">
```

### Sidebar à Direita

```html
<body data-sidebar-position="right">
```

**Características:**
- Sidebar fixa na direita
- Conteúdo principal à esquerda
- Ideal para idiomas RTL

## 🗂️ Layouts de Sidebar

### Sidebar Default (Padrão)

```html
<body data-sidebar-layout="default">
```

**Características:**
- Largura total (~250px)
- Ícones grandes + texto
- Ideal para desktop

### Sidebar Compacta

```html
<body data-sidebar-layout="compact">
```

**Características:**
- Largura reduzida (~70px)
- Apenas ícones
- Expande ao passar o mouse
- Ideal para tablets

### Alternar Dinamicamente

```javascript
// Toggle entre layouts
document.body.setAttribute('data-sidebar-layout', 'compact');

// Voltar ao padrão
document.body.setAttribute('data-sidebar-layout', 'default');
```

## 🎛️ Sistema de Grid

O AdminKit Pro usa o sistema de grid do Bootstrap 5:

### Grid Responsivo

```html
<div class="container-fluid">
  <div class="row">
    <div class="col-sm-6 col-md-4 col-lg-3">
      <!-- Coluna que ocupa:
           - 6 colunas em sm (≥576px)
           - 4 colunas em md (≥768px)
           - 3 colunas em lg (≥992px)
      -->
    </div>
  </div>
</div>
```

### Breakpoints

| Breakpoint | Largura | Dispositivo |
|------------|---------|-------------|
| xs | <576px | Extra pequeno |
| sm | ≥576px | Pequeno |
| md | ≥768px | Médio |
| lg | ≥992px | Grande |
| xl | ≥1200px | Extra grande |
| xxl | ≥1400px | Extra extra grande |

### Utilitários de Flexbox

```html
<!-- Centralizar conteúdo -->
<div class="d-flex align-items-center justify-content-center">

<!-- Direção da coluna -->
<div class="d-flex flex-column">

<!-- Espaçamento automático -->
<div class="d-flex justify-content-between">

<!-- Grow e shrink -->
<div class="flex-grow-1">  <!-- Ocupa espaço disponível -->
<div class="flex-shrink-0"> <!-- Nunca encolhe -->
```

## 📏 Margens e Padding

### Sistema de Spacing

O Bootstrap usa um sistema de spacing com 6 níveis:

| Classe | Tamanho |
|--------|---------|
| 0 | 0 |
| 1 | 0.25rem (4px) |
| 2 | 0.5rem (8px) |
| 3 | 1rem (16px) |
| 4 | 1.5rem (24px) |
| 5 | 3rem (48px) |
| auto | Automático |

### Sintaxe

```
{property}{sides}-{size}
```

**Propriedades:**
- `m` - margin
- `p` - padding

**Lados:**
- `t` - top
- `b` - bottom
- `s` - start (left em LTR)
- `e` - end (right em LTR)
- `x` - eixos x (left + right)
- `y` - eixos y (top + bottom)
-空白 - todos os lados

### Exemplos

```html
<!-- Margens -->
<div class="m-3">          <!-- Todas as margens: 16px -->
<div class="mt-2">         <!-- Top: 8px -->
<div class="mb-4">         <!-- Bottom: 24px -->
<div class="mx-auto">      <!-- Horizontal centralizado -->
<div class="my-3">         <!-- Top e bottom: 16px -->

<!-- Padding -->
<div class="p-4">          <!-- Todo padding: 24px -->
<div class="pt-3">         <!-- Top: 16px -->
<div class="px-4">         <!-- Horizontal: 24px -->
```

## 🎴 Cards

Os cards são componentes fundamentais do layout:

```html
<div class="card">
  <div class="card-header">
    <h5 class="card-title">Título do Card</h5>
  </div>
  <div class="card-body">
    <!-- Conteúdo -->
  </div>
  <div class="card-footer">
    <!-- Rodapé -->
  </div>
</div>
```

### Cards com Flex

```html
<!-- Card que cresce para preencher espaço -->
<div class="card flex-fill w-100">

<!-- Cards em linha -->
<div class="row">
  <div class="col-md-6 d-flex">
    <div class="card flex-fill w-100">
      <!-- Ocupa altura disponível -->
    </div>
  </div>
</div>
```

## 🌊 Overflow e Scroll

### Scrollbars Customizadas

```css
/* Sidebar com scrollbar customizada */
.sidebar {
  overflow-y: auto;
}

/* Área de conteúdo scrollável */
.content {
  overflow-x: hidden;
  overflow-y: auto;
}
```

### Hide/Show Scrollbars

```css
/* Ocultar scrollbar mas manter funcionalidade */
.hide-scrollbar {
  scrollbar-width: none;  /* Firefox */
  -ms-overflow-style: none;  /* IE/Edge */
}

.hide-scrollbar::-webkit-scrollbar {
  display: none;  /* Chrome/Safari */
}
```

## 📊 Exemplos de Layout

### Dashboard Típico

```html
<main class="content">
  <div class="container-fluid p-0">
    <!-- Header da página -->
    <div class="row mb-2 mb-xl-3">
      <div class="col-auto">
        <h3><strong>Título</strong> da Página</h3>
      </div>
    </div>

    <!-- Cards de estatísticas -->
    <div class="row">
      <div class="col-sm-6 col-xl-3">
        <div class="card">
          <div class="card-body">
            <!-- Conteúdo -->
          </div>
        </div>
      </div>
    </div>

    <!-- Gráfico grande -->
    <div class="row">
      <div class="col-12">
        <div class="card flex-fill">
          <!-- Conteúdo do gráfico -->
        </div>
      </div>
    </div>
  </div>
</main>
```

### Layout de Formulário

```html
<div class="card">
  <div class="card-body">
    <form>
      <div class="row mb-3">
        <div class="col-md-6">
          <label class="form-label">Campo 1</label>
          <input type="text" class="form-control">
        </div>
        <div class="col-md-6">
          <label class="form-label">Campo 2</label>
          <input type="text" class="form-control">
        </div>
      </div>
      <div class="row">
        <div class="col-12">
          <button type="submit" class="btn btn-primary">
            Enviar
          </button>
        </div>
      </div>
    </form>
  </div>
</div>
```

## 🔧 Customizações Avançadas

### Sidebar Colapsada

```javascript
// Toggle sidebar
const sidebar = document.getElementById('sidebar');
sidebar.classList.toggle('collapsed');
```

### Altura da Viewport

```html
<!-- Ocupar toda a altura -->
<div class="vh-100">      <!-- 100% da viewport height -->
<div class="vh-75">       <!-- 75% da viewport height -->

<!-- Ocupar toda a largura -->
<div class="vw-100">      <!-- 100% da viewport width -->
```

### Z-Index Controlado

```css
/* Overlay sobre tudo */
.z-index-overlay {
  z-index: 9999;
}

/* Sidebar por cima do conteúdo */
.sidebar {
  z-index: 1000;
}
```

---

**Próximo:** [Branding e Identidade Visual](branding.md)

**Versão:** 1.0.0
**Última atualização:** 2026-02-17
