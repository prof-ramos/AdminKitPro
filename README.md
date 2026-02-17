<div align="center">

# AdminKit Pro

### Template de Dashboard Admin Responsivo Baseado em Bootstrap 5

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-purple.svg)](https://getbootstrap.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26.svg)](https://www.w3.org/html/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6.svg)](https://www.w3.org/css/)

[Documentação](docs/README.md) • [Demo Online](#) • [Contribuindo](#contribuindo) • [Licença](LICENSE)

</div>

---

## Sobre o AdminKit Pro

O **AdminKit Pro** é um template premium de dashboard admin construído com Bootstrap 5, projetado para ajudar desenvolvedores a criar interfaces de administração modernas, responsivas e elegantes em menos tempo.

Com uma arquitetura limpa e componentes bem estruturados, o AdminKit Pro serve como o ponto de partida perfeito para qualquer aplicação web que需要一个 painel administrativo robusto.

### Destaques

- **Bootstrap 5.3** - Construído com a versão mais recente do framework Bootstrap
- **Design Responsivo** - Funciona perfeitamente em desktop, tablet e mobile
- **Dark Mode** - Suporte nativo para tema escuro
- **Componentes Prontos** - Mais de 30 componentes de interface pré-construídos
- **Gráficos Integrados** - Suporte para ApexCharts e Chart.js
- **Tabelas Avançadas** - DataTables com múltiplas funcionalidades
- **Editores WYSIWYG** - Quill e TinyMCE integrados
- **Mapas** - Google Maps e mapas vetoriais
- **Ícones** - Feather Icons e Font Awesome
- **Formulários** - Validação, máscaras, uploads e muito mais
- **Páginas Completas** - Autenticação, perfil, tarefas, projetos, etc.

---

## Demonstração

### Dashboard Principal

O dashboard principal inclui:

- Estatísticas em tempo real
- Gráficos de vendas e receitas
- Lista de transações recentes
- Atividades do usuário
- Projetos em andamento
- Notificações e alertas

### Componentes

[Ver todos os componentes](docs/componentes/)

- **UI Components** - Botões, cards, modais, tabs, alertas, etc.
- **Formulários** - Inputs básicos, grupos de input, validação, editores
- **Tabelas** - DataTables com paginação, busca e filtros
- **Gráficos** - ApexCharts e Chart.js
- **Ícones** - Bibliotecas de ícones populares
- **Mapas** - Google Maps e mapas vetoriais

---

## Instalação

### Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Servidor web local (opcional, para desenvolvimento)

### Passos

1. **Clone o repositório**

```bash
git clone https://github.com/seu-usuario/adminkit-pro.git
cd adminkit-pro
```

2. **Abra o projeto**

Você pode abrir o arquivo `index.html` diretamente no navegador ou usar um servidor local:

```bash
# Usando Python 3
python -m http.server 8000

# Usando Node.js (http-server)
npx http-server

# Usando PHP
php -S localhost:8000
```

3. **Acesse no navegador**

```
http://localhost:8000
```

### Configuração

O AdminKit Pro usa arquivos CSS para temas. Escolha seu tema preferido em `<head>`:

```html
<!-- Tema Claro (Padrão) -->
<link href="css/light.css" rel="stylesheet">

<!-- Tema Escuro -->
<link href="css/dark.css" rel="stylesheet">
```

Para mais detalhes, consulte o [Guia de Início](docs/guia-de-inicio/).

---

## Uso

### Estrutura de Arquivos

```
adminkit-pro/
├── css/                 # Estilos e temas
├── js/                  # Scripts JavaScript
├── fonts/               # Fontes utilizadas
├── img/                 # Imagens e ícones
├── docs/                # Documentação em pt-BR
│   ├── componentes/     # Documentação de componentes
│   ├── exemplos/        # Exemplos de uso
│   ├── guia-de-inicio/  # Guias de introdução
│   └── personalizacao/  # Guias de personalização
├── index.html           # Página principal (dashboard)
├── *.html               # Outras páginas do template
└── README.md            # Este arquivo
```

### Personalização

#### Temas

O AdminKit Pro suporta múltiplos temas:

```html
<body data-theme="default">  <!-- Tema padrão -->
<body data-theme="dark">     <!-- Tema escuro -->
<body data-theme="light">    <!-- Tema claro -->
<body data-theme="colored">  <!-- Tema colorido -->
```

#### Layout

```html
<body data-layout="fluid">   <!-- Layout fluido (padrão) -->
<body data-layout="boxed">   <!-- Layout em caixa -->
```

#### Sidebar

```html
<body data-sidebar-position="left">  <!-- Sidebar esquerda (padrão) -->
<body data-sidebar-position="right"> <!-- Sidebar direita -->

<body data-sidebar-layout="default">  <!-- Sidebar padrão -->
<body data-sidebar-layout="compact">  <!-- Sidebar compacta -->
```

Para mais informações sobre personalização, consulte a [documentação de personalização](docs/personalizacao/).

---

## Documentação

A documentação completa em português brasileiro está disponível no diretório [`docs/`](docs/README.md):

- [Guia de Início](docs/guia-de-inicio/) - Comece aqui
- [Componentes](docs/componentes/) - Referência completa
- [Personalização](docs/personalizacao/) - Adapte ao seu projeto
- [Exemplos](docs/exemplos/) - Casos de uso práticos

---

## Tecnologias Utilizadas

- **HTML5** - Estrutura semântica
- **CSS3** - Estilos modernos com variáveis CSS
- **JavaScript (ES6+)** - Funcionalidades interativas
- **Bootstrap 5.3** - Framework CSS
- **ApexCharts** - Gráficos interativos
- **Chart.js** - Biblioteca de gráficos
- **DataTables** - Tabelas avançadas
- **Feather Icons** - Ícones minimalistas
- **Font Awesome** - Ícones vetoriais
- **Quill** - Editor WYSIWYG
- **TinyMCE** - Editor de texto rico
- **Google Maps** - Mapas interativos
- **jsVectorMap** - Mapas vetoriais

---

## Navegadores Suportados

| Chrome | Firefox | Safari | Edge |
|--------|---------|--------|------|
| Última versão | Última versão | Última versão | Última versão |

---

## Contribuindo

Contribuições são bem-vindas! Por favor, leia nosso guia:

1. Leia o [CONTRIBUTING.md](CONTRIBUTING.md)
2. Verifique as [issues abertas](../../issues)
3. Faça um fork do projeto
4. Crie uma branch para sua feature (`git checkout -b feature/NovaFuncionalidade`)
5. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
6. Push para a branch (`git push origin feature/NovaFuncionalidade`)
7. Abra um Pull Request

### Diretrizes de Contribuição

- Mantenha o código limpo e bem documentado
- Siga os padrões de código existentes
- Teste em múltiplos navegadores
- Atualize a documentação conforme necessário
- Respeite o [Código de Conduta](CODE_OF_CONDUCT.md)

---

## Créditos

### Desenvolvimento Original

- **AdminKit** - Template original

### Dependências de Terceiros

- Bootstrap ([https://getbootstrap.com](https://getbootstrap.com))
- ApexCharts ([https://apexcharts.com](https://apexcharts.com))
- Chart.js ([https://www.chartjs.org](https://www.chartjs.org))
- DataTables ([https://datatables.net](https://datatables.net))
- Feather Icons ([https://feathericons.com](https://feathericons.com))
- Font Awesome ([https://fontawesome.com](https://fontawesome.com))
- Quill ([https://quilljs.com](https://quilljs.com))
- TinyMCE ([https://www.tiny.cloud](https://www.tiny.cloud))

### Tradução e Documentação em Português

- **Comunidade Brasileira** - Tradução e documentação em pt-BR

---

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

```
Copyright (c) 2026 AdminKit Pro

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## Suporte

- Documentação: [docs/README.md](docs/README.md)
- Issues: [GitHub Issues](../../issues)
- Discussões: [GitHub Discussions](../../discussions)

---

## Status do Projeto

Este projeto está ativamente mantido. Versões e atualizações serão lançadas regularmente.

---

<div align="center">

**Feito com ❤️ pela comunidade de desenvolvedores brasileiros**

[⬆ Voltar ao topo](#adminkit-pro)

</div>
