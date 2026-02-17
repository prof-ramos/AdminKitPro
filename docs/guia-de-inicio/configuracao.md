# Configuração de Temas do AdminKit

O AdminKit Pro oferece um sistema flexível de temas que permite personalizar completamente a aparência da sua aplicação. Este guia mostra como configurar e alternar entre os diferentes temas disponíveis.

## Temas Disponíveis

O AdminKit possui quatro temas pré-configurados:

| Tema | Descrição | Arquivo CSS |
|------|-----------|-------------|
| **Default** | Tema principal com azul e cinza | `css/light.css` |
| **Light** | Variação clara minimalista | `css/light.css` |
| **Dark** | Tema escuro para redução de fadiga visual | `css/dark.css` |
| **Colored** | Tema colorido com acentos vibrantes | `css/light.css` |

## Configuração via HTML

### Método 1: Alteração Manual no HTML

Edite o arquivo HTML e altere a linha do CSS:

```html
<head>
    <!-- Para tema claro -->
    <link href="css/light.css" rel="stylesheet">

    <!-- Para tema escuro -->
    <link href="css/dark.css" rel="stylesheet">
</head>
```

### Método 2: Configuração via Atributos data-*

O AdminKit usa atributos data para configurar o tema e layout:

```html
<body data-theme="default"
      data-layout="fluid"
      data-sidebar-position="left"
      data-sidebar-layout="default">
```

#### Atributos Disponíveis

| Atributo | Valores | Padrão | Descrição |
|----------|---------|--------|-----------|
| `data-theme` | `default`, `dark`, `light`, `colored` | `default` | Esquema de cores |
| `data-layout` | `fluid`, `boxed` | `fluid` | Tipo de layout |
| `data-sidebar-position` | `left`, `right` | `left` | Posição da sidebar |
| `data-sidebar-layout` | `default`, `compact` | `default` | Tamanho da sidebar |

## Painel de Configurações

O AdminKit inclui um painel interativo de configurações que permite alternar temas visualmente.

### Ativando o Painel

O painel já está incluído no template. Para usá-lo:

1. Abra qualquer página do AdminKit
2. Clique no ícone de sliders no canto superior direito
3. O painel de configurações será exibido

### Recursos do Painel

- **Color Scheme**: Selecione entre Default, Colored, Dark e Light
- **Sidebar Layout**: Alterne entre Default e Compact
- **Sidebar Position**: Mova a sidebar para esquerda ou direita
- **Layout**: Alterne entre Fluid e Boxed

As configurações são salvas automaticamente no localStorage do navegador.

## Configuração via JavaScript

### Alterar Tema Programaticamente

```javascript
// Alterar para tema escuro
document.body.setAttribute('data-theme', 'dark');

// Alterar para tema claro
document.body.setAttribute('data-theme', 'light');

// Alterar para tema colorido
document.body.setAttribute('data-theme', 'colored');

// Alterar layout para boxed
document.body.setAttribute('data-layout', 'boxed');

// Mover sidebar para direita
document.body.setAttribute('data-sidebar-position', 'right');

// Sidebar compacta
document.body.setAttribute('data-sidebar-layout', 'compact');
```

### Ler Configuração Atual

```javascript
// Obter tema atual
const currentTheme = document.body.getAttribute('data-theme');
console.log('Tema atual:', currentTheme);

// Verificar se está em modo dark
const isDark = document.body.getAttribute('data-theme') === 'dark';
```

## Alternância Dinâmica de Temas

### Criar um Toggle Light/Dark

```html
<button id="theme-toggle" class="btn btn-light">
    <i class="align-middle" data-feather="moon"></i>
</button>

<script>
    const toggleBtn = document.getElementById('theme-toggle');

    toggleBtn.addEventListener('click', function() {
        const currentTheme = document.body.getAttribute('data-theme');
        const newTheme = currentTheme === 'dark' ? 'light' : 'dark';

        document.body.setAttribute('data-theme', newTheme);

        // Salvar preferência
        localStorage.setItem('theme', newTheme);

        // Atualizar CSS
        const stylesheet = document.querySelector('.js-stylesheet');
        stylesheet.setAttribute('href', `css/${newTheme}.css`);
    });
</script>
```

## Persistência de Configurações

### Usando localStorage

O AdminKit usa localStorage para salvar as preferências do usuário:

```javascript
// Salvar configuração
localStorage.setItem('adminkit_config_theme', 'dark');
localStorage.setItem('adminkit_config_layout', 'boxed');
localStorage.setItem('adminkit_config_sidebarPosition', 'right');

// Ler configuração
const theme = localStorage.getItem('adminkit_config_theme');
const layout = localStorage.getItem('adminkit_config_layout');
```

### Carregar Configurações ao Iniciar

```javascript
document.addEventListener('DOMContentLoaded', function() {
    // Carregar tema salvo
    const savedTheme = localStorage.getItem('adminkit_config_theme') || 'default';
    document.body.setAttribute('data-theme', savedTheme);

    // Carregar layout salvo
    const savedLayout = localStorage.getItem('adminkit_config_layout') || 'fluid';
    document.body.setAttribute('data-layout', savedLayout);

    // Carregar posição da sidebar
    const savedSidebarPos = localStorage.getItem('adminkit_config_sidebarPosition') || 'left';
    document.body.setAttribute('data-sidebar-position', savedSidebarPos);
});
```

## Detalhes dos Temas

### Tema Default

Cores principais:
- **Primary**: Azul (#435ebe)
- **Background**: Branco (#ffffff)
- **Text**: Cinza escuro (#3d4655)
- **Sidebar**: Azul escuro (#2c3e50)

### Tema Light

Cores principais:
- **Primary**: Azul claro (#435ebe)
- **Background**: Branco puro (#ffffff)
- **Text**: Cinza médio (#6c757d)
- **Sidebar**: Branco com borda

### Tema Dark

Cores principais:
- **Primary**: Azul vibrante (#435ebe)
- **Background**: Cinza escuro (#1e2128)
- **Text**: Branco/cinza claro (#e2e8f0)
- **Sidebar**: Preto/cinza muito escuro (#17191f)

### Tema Colored

Cores principais:
- **Primary**: Gradiente colorido
- **Background**: Branco
- **Text**: Cinza escuro
- **Sidebar**: Colorida com gradiente

## Layouts

### Layout Fluid (Padrão)

O conteúdo ocupa toda a largura disponível:

```html
<body data-layout="fluid">
```

### Layout Boxed

O conteúdo é limitado a uma largura máxima e centralizado:

```html
<body data-layout="boxed">
```

## Sidebar

### Sidebar Default

Sidebar completa com texto completo nos itens.

```html
<body data-sidebar-layout="default">
```

### Sidebar Compact

Sidebar reduzida, mostrando apenas ícones.

```html
<body data-sidebar-layout="compact">
```

### Posição da Sidebar

#### Sidebar à Esquerda (Padrão)

```html
<body data-sidebar-position="left">
```

#### Sidebar à Direita

```html
<body data-sidebar-position="right">
```

## Personalização Avançada

### Criar um Tema Customizado

1. Copie `css/light.css` ou `css/dark.css`
2. Renomeie para `css/custom.css`
3. Altere as variáveis CSS:
```css
:root {
    --primary: #sua-cor;
    --secondary: #sua-cor;
    --success: #sua-cor;
    --danger: #sua-cor;
    --warning: #sua-cor;
    --info: #sua-cor;
    --light: #sua-cor;
    --dark: #sua-cor;
}
```

4. No HTML:
```html
<link href="css/custom.css" rel="stylesheet">
```

## Boas Práticas

1. **Respeite a Preferência do Usuário**: Sempre que possível, use a preferência do sistema operacional
2. **Teste Todos os Temas**: Certifique-se de que seu conteúdo fica bom em todos os temas
3. **Mantenha Contraste**: Garanta que o texto seja legível em todos os temas
4. **Use Variáveis CSS**: Use variáveis para facilitar a manutenção
5. **Salve Preferências**: Persista as escolhas do usuário para melhor experiência

## Solução de Problemas

### O tema não muda dinamicamente

Verifique se:
- O arquivo CSS correto está sendo carregado
- Os atributos `data-*` estão sendo aplicados ao `<body>`
- Não há CSS inline sobrescrevendo os estilos

### As cores não ficam consistentes

- Limpe o cache do navegador
- Verifique se há conflitos com outros arquivos CSS
- Use específicos CSS mais altos para sobrescrever estilos

### O localStorage não funciona

- Verifique se o navegador permite cookies e dados de site
- Teste em modo privado (pode não funcionar)
- Verifique o console do navegador por erros de segurança

## Próximos Passos

- Personalize as cores em [Variáveis de Customização](variaveis.md)
- Explore os [Componentes Disponíveis](../componentes/)
- Veja [Exemplos de Uso](../exemplos/)
