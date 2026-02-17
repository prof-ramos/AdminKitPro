# Variáveis de Customização do AdminKit

O AdminKit usa variáveis CSS para facilitar a personalização do template. Este guia detalha todas as variáveis disponíveis e como utilizá-las.

## Variáveis de Cores

### Cores Principais

```css
:root {
    --primary: #435ebe;      /* Cor principal - azul */
    --secondary: #6c757d;    /* Cor secundária - cinza */
    --success: #00cc27;      /* Sucesso - verde */
    --danger: #e63757;       /* Perigo/danger - vermelho */
    --warning: #f5803e;      /* Aviso - laranja */
    --info: #00d1e2;         /* Informação - ciano */
    --light: #f9f9f9;        /* Claro - cinza muito claro */
    --dark: #212529;         /* Escuro - preto suave */
}
```

### Cores do Tema Light

```css
:root {
    --body-bg: #f5f7fb;           /* Fundo da página */
    --card-bg: #ffffff;           /* Fundo dos cards */
    --border-color: #dce3eb;      /* Cor das bordas */
    --text-color: #3d4655;        /* Cor do texto principal */
    --text-muted: #6c757d;        /* Cor do texto secundário */
    --heading-color: #1e2128;     /* Cor dos títulos */
}
```

### Cores do Tema Dark

```css
[data-theme="dark"] {
    --body-bg: #1e2128;           /* Fundo da página */
    --card-bg: #2c3038;           /* Fundo dos cards */
    --border-color: #3d4655;      /* Cor das bordas */
    --text-color: #e2e8f0;        /* Cor do texto principal */
    --text-muted: #a0aec0;        /* Cor do texto secundário */
    --heading-color: #ffffff;     /* Cor dos títulos */
}
```

### Cores da Sidebar

```css
:root {
    --sidebar-bg: #2c3e50;        /* Fundo da sidebar */
    --sidebar-color: #ffffff;     /* Cor do texto da sidebar */
    --sidebar-active: #3d5166;    /* Cor do item ativo */
    --sidebar-width: 260px;       /* Largura da sidebar */
    --sidebar-width-compact: 70px; /* Largura da sidebar compacta */
}
```

## Variáveis de Tipografia

### Fontes

```css
:root {
    --font-family-base: 'Inter', sans-serif;
    --font-size-base: 0.9375rem;  /* 15px */
    --font-weight-light: 300;
    --font-weight-normal: 400;
    --font-weight-semibold: 600;
    --font-weight-bold: 700;
}
```

### Tamanhos de Título

```css
:root {
    --h1-font-size: 2rem;         /* 32px */
    --h2-font-size: 1.75rem;      /* 28px */
    --h3-font-size: 1.5rem;       /* 24px */
    --h4-font-size: 1.25rem;      /* 20px */
    --h5-font-size: 1.125rem;     /* 18px */
    --h6-font-size: 1rem;         /* 16px */
}
```

## Variáveis de Espaçamento

```css
:root {
    --spacer: 1rem;               /* Espaçamento base - 16px */
    --spacers: (
        0: 0,
        1: 0.25rem,   /* 4px */
        2: 0.5rem,    /* 8px */
        3: 1rem,      /* 16px */
        4: 1.5rem,    /* 24px */
        5: 3rem       /* 48px */
    );
}
```

## Variáveis de Layout

```css
:root {
    --navbar-height: 56px;        /* Altura da navbar */
    --footer-height: 56px;        /* Altura do footer */
    --sidebar-width: 260px;       /* Largura da sidebar */
    --container-max-width: 1320px; /* Largura máxima do container */
}
```

## Variáveis de Border Radius

```css
:root {
    --border-radius: 0.375rem;    /* 6px */
    --border-radius-sm: 0.25rem;  /* 4px */
    --border-radius-lg: 0.5rem;   /* 8px */
    --border-radius-pill: 50rem;  /* Pílula */
}
```

## Variáveis de Sombras

```css
:root {
    --box-shadow-sm: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
    --box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15);
    --box-shadow-lg: 0 1rem 3rem rgba(0, 0, 0, 0.175);
}
```

## Variáveis de Transições

```css
:root {
    --transition-base: all 0.2s ease-in-out;
    --transition-fade: opacity 0.15s linear;
    --transition-collapse: height 0.35s ease;
}
```

## Como Sobrescrever Variáveis

### Método 1: No Próprio CSS

Crie um arquivo `custom.css` após o CSS principal:

```html
<link href="css/light.css" rel="stylesheet">
<link href="css/custom.css" rel="stylesheet">
```

No `custom.css`:

```css
:root {
    --primary: #ff6b6b;           /* Altera cor principal para vermelho */
    --secondary: #4ecdc4;         /* Altera cor secundária para turquesa */
    --sidebar-bg: #1a1a2e;        /* Sidebar mais escura */
    --body-bg: #f0f2f5;           /* Fundo da página mais claro */
}
```

### Método 2: Por Seletor Específico

Para sobrescrever apenas em certas áreas:

```css
/* Apenas na sidebar */
.sidebar {
    --sidebar-bg: #000000;
}

/* Apenas em cards */
.card {
    --card-bg: #f8f9fa;
}

/* Apenas no tema dark */
[data-theme="dark"] {
    --primary: #5d78ff;
}
```

### Método 3: Via JavaScript

```javascript
// Alterar variável dinamicamente
document.documentElement.style.setProperty('--primary', '#ff6b6b');

// Ler valor de uma variável
const primaryColor = getComputedStyle(document.documentElement)
    .getPropertyValue('--primary').trim();
```

## Exemplos de Customização

### Exemplo 1: Paleta de Cores Corporativa

```css
:root {
    /* Sua marca */
    --primary: #0056b3;
    --secondary: #6c757d;

    /* Variantes */
    --primary-light: #4dabf7;
    --primary-dark: #004494;

    /* Aplicações */
    --sidebar-bg: var(--primary);
    --navbar-bg: var(--primary);
}
```

### Exemplo 2: Tema com Alto Contraste

```css
:root {
    --primary: #0000ff;
    --text-color: #000000;
    --heading-color: #000000;
    --body-bg: #ffffff;
    --card-bg: #ffffff;
    --border-color: #000000;
}
```

### Exemplo 3: Tema Minimalista

```css
:root {
    --primary: #333333;
    --secondary: #666666;
    --body-bg: #fafafa;
    --card-bg: #ffffff;
    --text-color: #333333;
    --border-color: #e0e0e0;
}
```

## Variáveis para Componentes Específicos

### Botões

```css
:root {
    --btn-padding-y: 0.375rem;
    --btn-padding-x: 0.75rem;
    --btn-font-size: 0.9375rem;
    --btn-border-radius: 0.375rem;
}
```

### Cards

```css
:root {
    --card-border-width: 1px;
    --card-border-color: rgba(0, 0, 0, 0.125);
    --card-border-radius: 0.75rem;
    --card-box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.075);
}
```

### Inputs

```css
:root {
    --input-padding-y: 0.5rem;
    --input-padding-x: 0.75rem;
    --input-font-size: 0.9375rem;
    --input-border-radius: 0.375rem;
    --input-border-color: #ced4da;
    --input-focus-border-color: #435ebe;
}
```

### Modais

```css
:root {
    --modal-zindex: 1055;
    --modal-bg: #ffffff;
    --modal-border-radius: 0.5rem;
    --modal-box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.5);
}
```

## Variáveis de Z-Index

```css
:root {
    --zindex-dropdown: 1000;
    --zindex-sticky: 1020;
    --zindex-fixed: 1030;
    --zindex-modal-backdrop: 1040;
    --zindex-modal: 1055;
    --zindex-popover: 1060;
    --zindex-tooltip: 1070;
}
```

## Variáveis de Breakpoints

```css
:root {
    --breakpoint-xs: 0;
    --breakpoint-sm: 576px;
    --breakpoint-md: 768px;
    --breakpoint-lg: 992px;
    --breakpoint-xl: 1200px;
    --breakpoint-xxl: 1400px;
}
```

## Boas Práticas

### 1. Use Variáveis Sempre que Possível

```css
/* Ruim */
.button {
    background-color: #435ebe;
}

/* Bom */
.button {
    background-color: var(--primary);
}
```

### 2. Crie Hierarquias de Cores

```css
:root {
    --primary: #435ebe;
    --primary-light: #7c8ef0;
    --primary-dark: #2a3d8a;
    --primary-bg: #eef1ff;
}
```

### 3. Use Nomes Descritivos

```css
/* Ruim */
--cor1: #ff0000;

/* Bom */
--danger: #e63757;
```

### 4. Documente Suas Variáveis

```css
/**
 * Cores da Marca
 * Primary: Cor principal da marca
 * Secondary: Cor secundária para elementos de suporte
 */
:root {
    --primary: #435ebe;
    --secondary: #6c757d;
}
```

## Debug de Variáveis

### Ver Todas as Variáveis no Console

```javascript
// Abra o console do navegador e execute:
const root = getComputedStyle(document.documentElement);
const vars = Array.from(document.styleSheets)
    .flatMap(sheet => Array.from(sheet.cssRules))
    .filter(rule => rule.cssText.includes('--'))
    .map(rule => rule.cssText);
console.log(vars.join('\n'));
```

### Ver Valor de uma Variável Específica

```javascript
const primaryColor = getComputedStyle(document.documentElement)
    .getPropertyValue('--primary');
console.log('Primary:', primaryColor);
```

## Solução de Problemas

### Variáveis Não Funcionam

1. Verifique se o navegador suporta variáveis CSS (todos os modernos suportam)
2. Certifique-se de que as variáveis estão definidas no `:root`
3. Use `var()` corretamente: `var(--primary)`

### Sobrescrita Não Funciona

1. Verifique a especificidade do seletor
2. Use `!important` apenas quando necessário
3. Certifique-se de que seu CSS carrega após o CSS do AdminKit

### Temas não Mudam

1. Verifique se os atributos `data-*` estão corretos
2. Use seletores específicos como `[data-theme="dark"]`
3. Limpe o cache do navegador

## Próximos Passos

- Configure os temas em [Configuração](configuracao.md)
- Explore a [Estrutura de Arquivos](estrutura.md)
- Veja [Exemplos de Uso](../exemplos/)
