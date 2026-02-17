# Componentes AdminKit Pro

Documentação completa dos componentes do AdminKit Pro em português brasileiro.

## Índice

- [Sidebar (Barra Lateral)](#sidebar-barra-lateral)
- [Navbar (Barra de Navegação)](#navbar-barra-de-navegação)
- [Cards (Cartões)](#cards-cartões)
- [Tabelas](#tabelas)
- [Formulários](#formulários)
- [Modais](#modais)

## Sidebar (Barra Lateral)

A sidebar é um dos principais componentes de navegação do AdminKit Pro, localizada à esquerda da tela.

### Estrutura Básica

```html
<nav id="sidebar" class="sidebar js-sidebar">
    <div class="sidebar-content js-simplebar">
        <!-- Brand/Logo -->
        <a class="sidebar-brand" href="index.html">
            <span class="sidebar-brand-text align-middle">AdminKit</span>
        </a>

        <!-- Usuário -->
        <div class="sidebar-user">
            <img src="img/avatars/avatar.jpg" class="avatar" alt="Avatar" />
            <a class="sidebar-user-title" href="#">Nome do Usuário</a>
            <div class="sidebar-user-subtitle">Cargo</div>
        </div>

        <!-- Navegação -->
        <ul class="sidebar-nav">
            <li class="sidebar-header">Páginas</li>
            <li class="sidebar-item active">
                <a class="sidebar-link" href="pagina.html">
                    <i class="align-middle" data-feather="home"></i>
                    <span class="align-middle">Início</span>
                </a>
            </li>
        </ul>
    </div>
</nav>
```

### Classes Modificadoras

- `sidebar` - Classe base da sidebar
- `js-sidebar` - Habilita funcionalidades JavaScript
- `sidebar-brand` - Logo/marca da aplicação
- `sidebar-user` - Informações do usuário
- `sidebar-nav` - Lista de navegação
- `sidebar-header` - Cabeçalho de seção
- `sidebar-item` - Item do menu
- `sidebar-link` - Link do menu
- `active` - Marca o item como ativo
- `collapsed` - Colapsa o submenu

### Submenus (Dropdowns)

```html
<li class="sidebar-item">
    <a data-bs-target="#submenu" data-bs-toggle="collapse" class="sidebar-link collapsed">
        <i class="align-middle" data-feather="grid"></i>
        <span class="align-middle">Menu</span>
    </a>
    <ul id="submenu" class="sidebar-dropdown list-unstyled collapse" data-bs-parent="#sidebar">
        <li class="sidebar-item">
            <a class="sidebar-link" href="subpagina.html">Subitem 1</a>
        </li>
        <li class="sidebar-item">
            <a class="sidebar-link" href="subpagina2.html">Subitem 2</a>
        </li>
    </ul>
</li>
```

### Badges

```html
<li class="sidebar-item">
    <a class="sidebar-link" href="pagina.html">
        <span>Página</span>
        <span class="sidebar-badge badge bg-primary">Pro</span>
    </a>
</li>
```

## Navbar (Barra de Navegação)

A navbar está localizada no topo da página e contém elementos de busca, notificações e perfil do usuário.

### Estrutura Básica

```html
<nav class="navbar navbar-expand navbar-light navbar-bg">
    <!-- Toggle Sidebar -->
    <a class="sidebar-toggle js-sidebar-toggle">
        <i class="hamburger align-self-center"></i>
    </a>

    <!-- Busca -->
    <form class="d-none d-sm-inline-block">
        <div class="input-group input-group-navbar">
            <input type="text" class="form-control" placeholder="Buscar..." aria-label="Buscar">
            <button class="btn" type="button">
                <i class="align-middle" data-feather="search"></i>
            </button>
        </div>
    </form>

    <!-- Menu Direito -->
    <div class="navbar-collapse collapse">
        <ul class="navbar-nav navbar-align">
            <!-- Notificações -->
            <li class="nav-item dropdown">
                <a class="nav-icon dropdown-toggle" href="#" data-bs-toggle="dropdown">
                    <div class="position-relative">
                        <i class="align-middle" data-feather="bell"></i>
                        <span class="indicator">4</span>
                    </div>
                </a>
                <!-- Dropdown de notificações -->
            </li>

            <!-- Perfil -->
            <li class="nav-item dropdown">
                <a class="nav-icon dropdown-toggle" href="#" data-bs-toggle="dropdown">
                    <img src="img/avatars/avatar.jpg" class="avatar" alt="Avatar" />
                </a>
            </li>
        </ul>
    </div>
</nav>
```

### Componentes da Navbar

#### Toggle Sidebar
Botão para expandir/recolher a sidebar:
```html
<a class="sidebar-toggle js-sidebar-toggle">
    <i class="hamburger align-self-center"></i>
</a>
```

#### Campo de Busca
```html
<div class="input-group input-group-navbar">
    <input type="text" class="form-control" placeholder="Buscar..." />
    <button class="btn" type="button">
        <i class="align-middle" data-feather="search"></i>
    </button>
</div>
```

#### Notificações
```html
<li class="nav-item dropdown">
    <a class="nav-icon dropdown-toggle" href="#" data-bs-toggle="dropdown">
        <div class="position-relative">
            <i class="align-middle" data-feather="bell"></i>
            <span class="indicator">4</span>
        </div>
    </a>
    <div class="dropdown-menu dropdown-menu-lg dropdown-menu-end py-0">
        <div class="dropdown-menu-header">
            4 Novas Notificações
        </div>
        <div class="list-group">
            <!-- Itens de notificação -->
        </div>
    </div>
</li>
```

#### Seleção de Idioma
```html
<li class="nav-item dropdown">
    <a class="nav-flag dropdown-toggle" href="#" data-bs-toggle="dropdown">
        <img src="img/flags/br.png" alt="Português" />
    </a>
    <div class="dropdown-menu dropdown-menu-end">
        <a class="dropdown-item" href="#">
            <img src="img/flags/br.png" alt="Português" width="20" />
            <span>Português</span>
        </a>
        <a class="dropdown-item" href="#">
            <img src="img/flags/us.png" alt="English" width="20" />
            <span>English</span>
        </a>
    </div>
</li>
```

## Cards (Cartões)

Os cards são componentes versáteis para organizar conteúdo de forma estruturada.

### Card Básico

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Título do Card</h5>
    </div>
    <div class="card-body">
        <p class="card-text">Conteúdo do card...</p>
    </div>
</div>
```

### Card com Imagem

```html
<div class="card">
    <img class="card-img-top" src="img/foto.jpg" alt="Imagem">
    <div class="card-header">
        <h5 class="card-title mb-0">Título</h5>
    </div>
    <div class="card-body">
        <p class="card-text">Conteúdo...</p>
    </div>
</div>
```

### Card com Ações

```html
<div class="card">
    <div class="card-header">
        <div class="card-actions float-end">
            <div class="dropdown position-relative">
                <a href="#" data-bs-toggle="dropdown">
                    <i class="align-middle" data-feather="more-horizontal"></i>
                </a>
                <div class="dropdown-menu dropdown-menu-end">
                    <a class="dropdown-item" href="#">Ação 1</a>
                    <a class="dropdown-item" href="#">Ação 2</a>
                </div>
            </div>
        </div>
        <h5 class="card-title mb-0">Título</h5>
    </div>
    <div class="card-body">
        <!-- Conteúdo -->
    </div>
</div>
```

### Card com Tabs

```html
<div class="card">
    <div class="card-header">
        <ul class="nav nav-tabs card-header-tabs" role="tablist">
            <li class="nav-item">
                <a class="nav-link active" data-bs-toggle="tab" href="#tab1">Tab 1</a>
            </li>
            <li class="nav-item">
                <a class="nav-link" data-bs-toggle="tab" href="#tab2">Tab 2</a>
            </li>
        </ul>
    </div>
    <div class="card-body">
        <div class="tab-content">
            <div class="tab-pane fade show active" id="tab1">
                Conteúdo da Tab 1
            </div>
            <div class="tab-pane fade" id="tab2">
                Conteúdo da Tab 2
            </div>
        </div>
    </div>
</div>
```

### Card com List Group

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Título</h5>
    </div>
    <ul class="list-group list-group-flush">
        <li class="list-group-item">Item 1</li>
        <li class="list-group-item">Item 2</li>
        <li class="list-group-item">Item 3</li>
    </ul>
</div>
```

### Cards de Estatísticas

```html
<div class="card">
    <div class="card-body">
        <div class="row">
            <div class="col mt-0">
                <h5 class="card-title">Vendas</h5>
            </div>
            <div class="col-auto">
                <div class="stat text-primary">
                    <i class="align-middle" data-feather="shopping-cart"></i>
                </div>
            </div>
        </div>
        <h1 class="mt-1 mb-3">2.382</h1>
        <div class="mb-0">
            <span class="badge badge-success-light">
                <i class="mdi mdi-arrow-bottom-right"></i> 5.25%
            </span>
            <span class="text-muted">Desde a semana passada</span>
        </div>
    </div>
</div>
```

## Tabelas

O AdminKit Pro suporta tabelas Bootstrap padrão e DataTables avançados.

### Tabela Básica

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Tabela</h5>
    </div>
    <div class="card-body">
        <table class="table">
            <thead>
                <tr>
                    <th>Nome</th>
                    <th>Email</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>João Silva</td>
                    <td>joao@email.com</td>
                    <td><span class="badge bg-success">Ativo</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
```

### Tabela sem Bordas

```html
<table class="table table-borderless">
    <!-- Conteúdo -->
</table>
```

### Tabela Responsiva

```html
<div class="table-responsive">
    <table class="table">
        <!-- Conteúdo -->
    </table>
</div>
```

### Tabela com Hover

```html
<table class="table table-hover">
    <!-- Conteúdo -->
</table>
```

### Tabela Compacta

```html
<table class="table table-sm">
    <!-- Conteúdo -->
</table>
```

## Formulários

Componentes de formulário estilizados e funcionais.

### Input Básico

```html
<div class="mb-3">
    <label class="form-label" for="inputEmail">Email</label>
    <input type="email" class="form-control" id="inputEmail" placeholder="nome@exemplo.com">
</div>
```

### Input com Descrição

```html
<div class="mb-3">
    <label class="form-label" for="inputPassword">Senha</label>
    <input type="password" class="form-control" id="inputPassword">
    <div class="form-text">Mínimo de 8 caracteres</div>
</div>
```

### Select

```html
<div class="mb-3">
    <label class="form-label" for="selectOption">Opção</label>
    <select class="form-select" id="selectOption">
        <option>Selecione...</option>
        <option value="1">Opção 1</option>
        <option value="2">Opção 2</option>
    </select>
</div>
```

### Textarea

```html
<div class="mb-3">
    <label class="form-label" for="textarea">Mensagem</label>
    <textarea class="form-control" id="textarea" rows="3"></textarea>
</div>
```

### Checkbox e Radio

```html
<!-- Checkbox -->
<div class="form-check">
    <input class="form-check-input" type="checkbox" id="check1">
    <label class="form-check-label" for="check1">Aceitar termos</label>
</div>

<!-- Radio -->
<div class="form-check">
    <input class="form-check-input" type="radio" name="radioGroup" id="radio1">
    <label class="form-check-label" for="radio1">Opção 1</label>
</div>
```

### Input Group

```html
<div class="input-group">
    <span class="input-group-text">@</span>
    <input type="text" class="form-control" placeholder="Usuário">
</div>
```

### Formulário Horizontal

```html
<form>
    <div class="row mb-3">
        <label class="col-sm-2 col-form-label" for="inputEmail3">Email</label>
        <div class="col-sm-10">
            <input type="email" class="form-control" id="inputEmail3">
        </div>
    </div>
    <div class="row mb-3">
        <label class="col-sm-2 col-form-label" for="inputPassword3">Senha</label>
        <div class="col-sm-10">
            <input type="password" class="form-control" id="inputPassword3">
        </div>
    </div>
</form>
```

## Modais

Componentes modais para diálogos e sobreposições.

### Modal Básico

```html
<!-- Botão de acionamento -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#modalExemplo">
    Abrir Modal
</button>

<!-- Modal -->
<div class="modal fade" id="modalExemplo" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Título do Modal</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Fechar"></button>
            </div>
            <div class="modal-body">
                <p>Conteúdo do modal...</p>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Fechar</button>
                <button type="button" class="btn btn-primary">Salvar</button>
            </div>
        </div>
    </div>
</div>
```

### Modal com Scroll

```html
<div class="modal fade" id="modalScroll" tabindex="-1">
    <div class="modal-dialog modal-dialog-scrollable">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

### Modal Centralizado

```html
<div class="modal fade" id="modalCentro" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

### Modal Grande

```html
<div class="modal fade" id="modalGrande" tabindex="-1">
    <div class="modal-dialog modal-lg">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

### Modal Extra Grande

```html
<div class="modal fade" id="modalXG" tabindex="-1">
    <div class="modal-dialog modal-xl">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

## Exemplos Adicionais

Para mais exemplos e demonstrações interativas, consulte os arquivos HTML na raiz do projeto:

- `ui-cards.html` - Exemplos de cards
- `ui-modals.html` - Exemplos de modais
- `forms-basic-inputs.html` - Exemplos de formulários
- `tables-bootstrap.html` - Exemplos de tabelas
- `index.html` - Exemplo completo de dashboard

## Personalização

Para personalizar os componentes, consulte a documentação de [Personalização](../personalizacao/README.md).
