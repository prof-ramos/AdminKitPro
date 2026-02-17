# Navbar (Barra de Navegação)

A navbar é a barra de navegação superior do AdminKit Pro, contendo elementos essenciais como busca, notificações e perfil do usuário.

## Visão Geral

A navbar do AdminKit Pro inclui:
- **Toggle da sidebar**: Botão para expandir/recolher a sidebar
- **Campo de busca**: Busca global na aplicação
- **Mega menu**: Menu dropdown expansivo
- **Notificações**: Sistema de notificações com contador
- **Mensagens**: Sistema de mensagens
- **Seleção de idioma**: Multi-idioma suportado
- **Perfil do usuário**: Menu de perfil e configurações

## Estrutura HTML

```html
<nav class="navbar navbar-expand navbar-light navbar-bg">
    <!-- Toggle Sidebar -->
    <a class="sidebar-toggle js-sidebar-toggle">
        <i class="hamburger align-self-center"></i>
    </a>

    <!-- Campo de Busca -->
    <form class="d-none d-sm-inline-block">
        <div class="input-group input-group-navbar">
            <input type="text" class="form-control" placeholder="Buscar..." aria-label="Buscar">
            <button class="btn" type="button">
                <i class="align-middle" data-feather="search"></i>
            </button>
        </div>
    </form>

    <!-- Menu Principal -->
    <ul class="navbar-nav d-none d-lg-flex">
        <li class="nav-item px-2 dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="megaDropdown"
               data-bs-toggle="dropdown">
                Mega Menu
            </a>
            <div class="dropdown-menu dropdown-menu-start dropdown-mega">
                <!-- Conteúdo do mega menu -->
            </div>
        </li>
    </ul>

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
            </li>

            <!-- Perfil -->
            <li class="nav-item dropdown">
                <a class="nav-icon pe-md-0 dropdown-toggle" href="#" data-bs-toggle="dropdown">
                    <img src="img/avatars/avatar.jpg" class="avatar img-fluid rounded" />
                </a>
            </li>
        </ul>
    </div>
</nav>
```

## Classes CSS

### Estrutura
| Classe | Descrição |
|--------|-----------|
| `.navbar` | Container principal da navbar |
| `.navbar-expand` | Habilita expansão responsiva |
| `.navbar-light` | Tema claro |
| `.navbar-bg` | Fundo da navbar |
| `.sidebar-toggle` | Botão de toggle da sidebar |
| `.js-sidebar-toggle` | Habilita funcionalidade JavaScript |
| `.hamburger` | Ícone de menu hambúrguer |
| `.input-group-navbar` | Grupo de input da navbar |
| `.navbar-nav` | Lista de navegação |
| `.nav-item` | Item do menu |
| `.nav-link` | Link do menu |
| `.nav-icon` | Ícone de navegação |
| `.navbar-align` | Alinhamento dos itens |
| `.indicator` | Indicador de notificação |

## Toggle Sidebar

Botão para expandir/recolher a sidebar:

```html
<a class="sidebar-toggle js-sidebar-toggle">
    <i class="hamburger align-self-center"></i>
</a>
```

## Campo de Busca

### Busca Simples

```html
<form class="d-none d-sm-inline-block">
    <div class="input-group input-group-navbar">
        <input type="text" class="form-control"
               placeholder="Buscar..."
               aria-label="Buscar">
        <button class="btn" type="button">
            <i class="align-middle" data-feather="search"></i>
        </button>
    </div>
</form>
```

### Busca com Dropdown

```html
<form class="d-none d-sm-inline-block">
    <div class="input-group input-group-navbar">
        <input type="text" class="form-control"
               placeholder="Buscar..."
               aria-label="Buscar">
        <button class="btn" type="button" data-bs-toggle="dropdown">
            <i class="align-middle" data-feather="search"></i>
        </button>
        <div class="dropdown-menu dropdown-menu-end">
            <div class="dropdown-arrow"></div>
            <div class="dropdown-header">
                <h6 class="dropdown-header-title">Resultados da Busca</h6>
            </div>
            <div class="dropdown-scroll max-h-400">
                <!-- Resultados -->
            </div>
        </div>
    </div>
</form>
```

## Mega Menu

Menu dropdown expansivo com múltiplas colunas:

```html
<li class="nav-item px-2 dropdown">
    <a class="nav-link dropdown-toggle" href="#" id="megaDropdown"
       role="button" data-bs-toggle="dropdown">
        Mega Menu
    </a>
    <div class="dropdown-menu dropdown-menu-start dropdown-mega"
         aria-labelledby="megaDropdown">
        <div class="d-md-flex align-items-start justify-content-start">
            <div class="dropdown-mega-list">
                <div class="dropdown-header">UI Elements</div>
                <a class="dropdown-item" href="#">Alerts</a>
                <a class="dropdown-item" href="#">Buttons</a>
                <a class="dropdown-item" href="#">Cards</a>
                <a class="dropdown-item" href="#">Carousel</a>
                <a class="dropdown-item" href="#">General</a>
                <a class="dropdown-item" href="#">Grid</a>
                <a class="dropdown-item" href="#">Modals</a>
                <a class="dropdown-item" href="#">Tabs</a>
                <a class="dropdown-item" href="#">Typography</a>
            </div>
            <div class="dropdown-mega-list">
                <div class="dropdown-header">Forms</div>
                <a class="dropdown-item" href="#">Layouts</a>
                <a class="dropdown-item" href="#">Basic Inputs</a>
                <a class="dropdown-item" href="#">Input Groups</a>
                <a class="dropdown-item" href="#">Advanced Inputs</a>
                <a class="dropdown-item" href="#">Editors</a>
                <a class="dropdown-item" href="#">Validation</a>
                <a class="dropdown-item" href="#">Wizard</a>
            </div>
            <div class="dropdown-mega-list">
                <div class="dropdown-header">Tables</div>
                <a class="dropdown-item" href="#">Basic Tables</a>
                <a class="dropdown-item" href="#">Responsive Table</a>
                <a class="dropdown-item" href="#">Table with Buttons</a>
                <a class="dropdown-item" href="#">Column Search</a>
                <a class="dropdown-item" href="#">Multi Selection</a>
                <a class="dropdown-item" href="#">Ajax Sourced Data</a>
            </div>
        </div>
    </div>
</li>
```

## Notificações

### Notificações Simples

```html
<li class="nav-item dropdown">
    <a class="nav-icon dropdown-toggle" href="#"
       id="alertsDropdown" data-bs-toggle="dropdown">
        <div class="position-relative">
            <i class="align-middle" data-feather="bell"></i>
            <span class="indicator">4</span>
        </div>
    </a>
    <div class="dropdown-menu dropdown-menu-lg dropdown-menu-end py-0"
         aria-labelledby="alertsDropdown">
        <div class="dropdown-menu-header">
            4 Novas Notificações
        </div>
        <div class="list-group">
            <a href="#" class="list-group-item">
                <div class="row g-0 align-items-center">
                    <div class="col-2">
                        <i class="text-danger" data-feather="alert-circle"></i>
                    </div>
                    <div class="col-10">
                        <div class="text-dark">Atualização concluída</div>
                        <div class="text-muted small mt-1">
                            Reinicie o servidor 12 para completar a atualização.
                        </div>
                        <div class="text-muted small mt-1">30m atrás</div>
                    </div>
                </div>
            </a>
            <!-- Mais itens -->
        </div>
        <div class="dropdown-menu-footer">
            <a href="#" class="text-muted">Ver todas as notificações</a>
        </div>
    </div>
</li>
```

### Tipos de Notificação

```html
<!-- Sucesso -->
<div class="col-2">
    <i class="text-success" data-feather="check-circle"></i>
</div>

<!-- Aviso -->
<div class="col-2">
    <i class="text-warning" data-feather="bell"></i>
</div>

<!-- Informação -->
<div class="col-2">
    <i class="text-primary" data-feather="info"></i>
</div>

<!-- Perigo -->
<div class="col-2">
    <i class="text-danger" data-feather="alert-circle"></i>
</div>
```

## Mensagens

```html
<li class="nav-item dropdown">
    <a class="nav-icon dropdown-toggle" href="#"
       id="messagesDropdown" data-bs-toggle="dropdown">
        <div class="position-relative">
            <i class="align-middle" data-feather="message-square"></i>
        </div>
    </a>
    <div class="dropdown-menu dropdown-menu-lg dropdown-menu-end py-0"
         aria-labelledby="messagesDropdown">
        <div class="dropdown-menu-header">
            <div class="position-relative">
                4 Novas Mensagens
            </div>
        </div>
        <div class="list-group">
            <a href="#" class="list-group-item">
                <div class="row g-0 align-items-center">
                    <div class="col-2">
                        <img src="img/avatars/avatar-5.jpg"
                             class="avatar img-fluid rounded-circle"
                             alt="Vanessa Tucker">
                    </div>
                    <div class="col-10 ps-2">
                        <div class="text-dark">Vanessa Tucker</div>
                        <div class="text-muted small mt-1">
                            Nam pretium turpis et arcu. Duis arcu tortor.
                        </div>
                        <div class="text-muted small mt-1">15m atrás</div>
                    </div>
                </div>
            </a>
            <!-- Mais itens -->
        </div>
        <div class="dropdown-menu-footer">
            <a href="#" class="text-muted">Ver todas as mensagens</a>
        </div>
    </div>
</li>
```

## Seleção de Idioma

```html
<li class="nav-item dropdown">
    <a class="nav-flag dropdown-toggle" href="#"
       id="languageDropdown" data-bs-toggle="dropdown">
        <img src="img/flags/br.png" alt="Português" />
    </a>
    <div class="dropdown-menu dropdown-menu-end"
         aria-labelledby="languageDropdown">
        <a class="dropdown-item" href="#">
            <img src="img/flags/br.png" alt="Português" width="20"
                 class="align-middle me-1" />
            <span class="align-middle">Português</span>
        </a>
        <a class="dropdown-item" href="#">
            <img src="img/flags/us.png" alt="English" width="20"
                 class="align-middle me-1" />
            <span class="align-middle">English</span>
        </a>
        <a class="dropdown-item" href="#">
            <img src="img/flags/es.png" alt="Español" width="20"
                 class="align-middle me-1" />
            <span class="align-middle">Español</span>
        </a>
    </div>
</li>
```

## Fullscreen

Botão para ativar modo tela cheia:

```html
<li class="nav-item">
    <a class="nav-icon js-fullscreen d-none d-lg-block" href="#">
        <div class="position-relative">
            <i class="align-middle" data-feather="maximize"></i>
        </div>
    </a>
</li>
```

## Perfil do Usuário

```html
<li class="nav-item dropdown">
    <a class="nav-icon pe-md-0 dropdown-toggle" href="#"
       data-bs-toggle="dropdown">
        <img src="img/avatars/avatar.jpg"
             class="avatar img-fluid rounded"
             alt="Charles Hall" />
    </a>
    <div class="dropdown-menu dropdown-menu-end">
        <a class="dropdown-item" href="pages-profile.html">
            <i class="align-middle me-1" data-feather="user"></i> Perfil
        </a>
        <a class="dropdown-item" href="#">
            <i class="align-middle me-1" data-feather="pie-chart"></i> Analytics
        </a>
        <div class="dropdown-divider"></div>
        <a class="dropdown-item" href="pages-settings.html">
            <i class="align-middle me-1" data-feather="settings"></i>
            Configurações e Privacidade
        </a>
        <a class="dropdown-item" href="#">
            <i class="align-middle me-1" data-feather="help-circle"></i>
            Central de Ajuda
        </a>
        <div class="dropdown-divider"></div>
        <a class="dropdown-item" href="#">Sair</a>
    </div>
</li>
```

## Responsividade

### Menu Responsivo

Elementos ocultos em telas menores:

```html
<!-- Visível apenas em telas médias e grandes -->
<form class="d-none d-sm-inline-block">
    <!-- Campo de busca -->
</form>

<!-- Visível apenas em telas grandes -->
<ul class="navbar-nav d-none d-lg-flex">
    <!-- Mega menu -->
</ul>

<!-- Ícone fullscreen oculto em telas pequenas -->
<a class="nav-icon js-fullscreen d-none d-lg-block" href="#">
    <!-- Fullscreen -->
</a>
```

## Personalização

### Cor de Fundo

```html
<nav class="navbar navbar-expand navbar-light navbar-bg">
    <!-- Navbar com fundo claro -->
</nav>
```

```css
.navbar-bg {
    background-color: #ffffff;
}
```

### Cor Escura

```html
<nav class="navbar navbar-expand navbar-dark bg-dark">
    <!-- Navbar escura -->
</nav>
```

### Altura Personalizada

```css
.navbar {
    height: 60px;
}
```

### Sombra

```css
.navbar {
    box-shadow: 0 2px 4px rgba(0,0,0,.08);
}
```

## Exemplo Completo

```html
<nav class="navbar navbar-expand navbar-light navbar-bg">
    <!-- Toggle Sidebar -->
    <a class="sidebar-toggle js-sidebar-toggle">
        <i class="hamburger align-self-center"></i>
    </a>

    <!-- Busca -->
    <form class="d-none d-sm-inline-block">
        <div class="input-group input-group-navbar">
            <input type="text" class="form-control"
                   placeholder="Buscar..."
                   aria-label="Buscar">
            <button class="btn" type="button">
                <i class="align-middle" data-feather="search"></i>
            </button>
        </div>
    </form>

    <!-- Links Principais -->
    <ul class="navbar-nav d-none d-lg-flex">
        <li class="nav-item px-2">
            <a class="nav-link" href="index.html">Início</a>
        </li>
        <li class="nav-item px-2">
            <a class="nav-link" href="pages-profile.html">Perfil</a>
        </li>
    </ul>

    <!-- Menu Direito -->
    <div class="navbar-collapse collapse">
        <ul class="navbar-nav navbar-align">
            <!-- Notificações -->
            <li class="nav-item dropdown">
                <a class="nav-icon dropdown-toggle" href="#"
                   id="alertsDropdown" data-bs-toggle="dropdown">
                    <div class="position-relative">
                        <i class="align-middle" data-feather="bell"></i>
                        <span class="indicator">4</span>
                    </div>
                </a>
                <div class="dropdown-menu dropdown-menu-lg dropdown-menu-end py-0">
                    <div class="dropdown-menu-header">
                        4 Novas Notificações
                    </div>
                    <div class="list-group list-group-flush">
                        <a href="#" class="list-group-item">
                            <div class="row g-0 align-items-center">
                                <div class="col-2">
                                    <i class="text-success" data-feather="check-circle"></i>
                                </div>
                                <div class="col-10">
                                    <div class="text-dark">Atualização concluída</div>
                                    <div class="text-muted small mt-1">30m atrás</div>
                                </div>
                            </div>
                        </a>
                    </div>
                    <div class="dropdown-menu-footer">
                        <a href="#" class="text-muted">Ver todas</a>
                    </div>
                </div>
            </li>

            <!-- Idioma -->
            <li class="nav-item dropdown">
                <a class="nav-flag dropdown-toggle" href="#"
                   id="languageDropdown" data-bs-toggle="dropdown">
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

            <!-- Fullscreen -->
            <li class="nav-item">
                <a class="nav-icon js-fullscreen d-none d-lg-block" href="#">
                    <div class="position-relative">
                        <i class="align-middle" data-feather="maximize"></i>
                    </div>
                </a>
            </li>

            <!-- Perfil -->
            <li class="nav-item dropdown">
                <a class="nav-icon pe-md-0 dropdown-toggle" href="#"
                   data-bs-toggle="dropdown">
                    <img src="img/avatars/avatar.jpg"
                         class="avatar img-fluid rounded"
                         alt="Avatar" />
                </a>
                <div class="dropdown-menu dropdown-menu-end">
                    <a class="dropdown-item" href="pages-profile.html">
                        <i class="align-middle me-1" data-feather="user"></i> Perfil
                    </a>
                    <a class="dropdown-item" href="pages-settings.html">
                        <i class="align-middle me-1" data-feather="settings"></i> Configurações
                    </a>
                    <div class="dropdown-divider"></div>
                    <a class="dropdown-item" href="#">Sair</a>
                </div>
            </li>
        </ul>
    </div>
</nav>
```

## Acessibilidade

### ARIA Labels

```html
<a class="sidebar-toggle js-sidebar-toggle" aria-label="Alternar menu">
    <i class="hamburger align-self-center"></i>
</a>
```

### Roles

```html
<nav class="navbar" role="navigation" aria-label="Navegação principal">
    <!-- Conteúdo -->
</nav>
```

## Troubleshooting

### Dropdowns não abrem
- Verifique se Bootstrap JS está carregado
- Confira se `data-bs-toggle="dropdown"` está presente
- Certifique-se de que os IDs são únicos

### Indicador de notificação não aparece
- Verifique se a classe `indicator` está presente
- Confira se o CSS do indicador está carregado

### Toggle da sidebar não funciona
- Certifique-se de que `js-sidebar-toggle` está presente
- Verifique se `js/app.js` está carregado
- Confira se a sidebar tem a classe `js-sidebar`

## Recursos Adicionais

- [Bootstrap Navbar](https://getbootstrap.com/docs/5.3/components/navbar/) - Documentação oficial
- [Feather Icons](https://feathericons.com/) - Ícones usados
