# Sidebar (Barra Lateral)

A sidebar é um componente fundamental de navegação do AdminKit Pro, fornecendo acesso rápido às principais seções da aplicação.

## Visão Geral

A sidebar do AdminKit Pro é:
- **Responsiva**: Adapta-se a diferentes tamanhos de tela
- **Colapsável**: Pode ser expandida/recolhida pelo usuário
- **Suporte a submenus**: Permite organização hierárquica
- **Personalizável**: Suporta diferentes temas e posições

## Estrutura HTML

```html
<nav id="sidebar" class="sidebar js-sidebar">
    <div class="sidebar-content js-simplebar">
        <!-- Brand -->
        <a class="sidebar-brand" href="index.html">
            <span class="sidebar-brand-text align-middle">
                AdminKit
                <sup><small class="badge bg-primary text-uppercase">Pro</small></sup>
            </span>
            <svg class="sidebar-brand-icon align-middle" width="32px" height="32px">
                <!-- Ícone SVG -->
            </svg>
        </a>

        <!-- Usuário -->
        <div class="sidebar-user">
            <div class="d-flex justify-content-center">
                <div class="flex-shrink-0">
                    <img src="img/avatars/avatar.jpg" class="avatar img-fluid rounded me-1" />
                </div>
                <div class="flex-grow-1 ps-2">
                    <a class="sidebar-user-title dropdown-toggle" href="#" data-bs-toggle="dropdown">
                        Charles Hall
                    </a>
                    <div class="dropdown-menu dropdown-menu-start">
                        <a class="dropdown-item" href="pages-profile.html">
                            <i class="align-middle me-1" data-feather="user"></i> Perfil
                        </a>
                        <a class="dropdown-item" href="#">
                            <i class="align-middle me-1" data-feather="pie-chart"></i> Analytics
                        </a>
                        <div class="dropdown-divider"></div>
                        <a class="dropdown-item" href="pages-settings.html">
                            <i class="align-middle me-1" data-feather="settings"></i> Configurações
                        </a>
                        <a class="dropdown-item" href="#">Sair</a>
                    </div>
                    <div class="sidebar-user-subtitle">Designer</div>
                </div>
            </div>
        </div>

        <!-- Navegação -->
        <ul class="sidebar-nav">
            <!-- Itens do menu -->
        </ul>

        <!-- CTA (Call to Action) -->
        <div class="sidebar-cta">
            <div class="sidebar-cta-content">
                <strong class="d-inline-block mb-2">Relatório Semanal</strong>
                <div class="mb-3 text-sm">
                    Seu relatório semanal está pronto para download!
                </div>
                <div class="d-grid">
                    <a href="#" class="btn btn-outline-primary">Download</a>
                </div>
            </div>
        </div>
    </div>
</nav>
```

## Classes CSS

### Estrutura
| Classe | Descrição |
|--------|-----------|
| `.sidebar` | Container principal da sidebar |
| `.js-sidebar` | Habilita funcionalidades JavaScript |
| `.sidebar-content` | Wrapper do conteúdo com scrollbar |
| `.js-simplebar` | Plugin de scrollbar personalizada |
| `.sidebar-brand` | Logo/marca da aplicação |
| `.sidebar-brand-text` | Texto da marca |
| `.sidebar-brand-icon` | Ícone da marca |
| `.sidebar-user` | Seção de informações do usuário |
| `.sidebar-user-title` | Nome do usuário |
| `.sidebar-user-subtitle` | Cargo/função do usuário |
| `.sidebar-nav` | Lista principal de navegação |
| `.sidebar-header` | Cabeçalho de seção |
| `.sidebar-item` | Item do menu |
| `.sidebar-link` | Link do item do menu |
| `.sidebar-dropdown` | Lista de submenu |
| `.sidebar-badge` | Badge/etiqueta do item |
| `.sidebar-cta` | Seção de chamada para ação |
| `.sidebar-cta-content` | Conteúdo do CTA |

### Estados
| Classe | Descrição |
|--------|-----------|
| `.active` | Marca o item como ativo |
| `.collapsed` | Colapsa o submenu |
| `.show` | Exibe o submenu expandido |

## Menu Simples

Item individual sem submenu:

```html
<li class="sidebar-item">
    <a class="sidebar-link" href="pages-profile.html">
        <i class="align-middle" data-feather="user"></i>
        <span class="align-middle">Perfil</span>
    </a>
</li>
```

## Menu com Dropdown

Item com submenu expansível:

```html
<li class="sidebar-item">
    <a data-bs-target="#dashboards" data-bs-toggle="collapse" class="sidebar-link collapsed">
        <i class="align-middle" data-feather="sliders"></i>
        <span class="align-middle">Dashboards</span>
    </a>
    <ul id="dashboards" class="sidebar-dropdown list-unstyled collapse" data-bs-parent="#sidebar">
        <li class="sidebar-item">
            <a class="sidebar-link" href="index.html">Analytics</a>
        </li>
        <li class="sidebar-item">
            <a class="sidebar-link" href="dashboard-ecommerce.html">E-Commerce</a>
        </li>
        <li class="sidebar-item">
            <a class="sidebar-link" href="dashboard-crypto.html">Crypto</a>
        </li>
    </ul>
</li>
```

## Menu com Badge

Item com indicador visual:

```html
<li class="sidebar-item">
    <a class="sidebar-link" href="pages-tasks.html">
        <i class="align-middle" data-feather="list"></i>
        <span class="align-middle">Tarefas</span>
        <span class="sidebar-badge badge bg-primary">Pro</span>
    </a>
</li>
```

## Cabeçalhos de Seção

Separadores visuais no menu:

```html
<ul class="sidebar-nav">
    <li class="sidebar-header">Páginas</li>
    <!-- Itens -->
    <li class="sidebar-header">Componentes</li>
    <!-- Mais itens -->
</ul>
```

## Multi-nível

Submenus aninhados (até 3 níveis):

```html
<li class="sidebar-item">
    <a data-bs-target="#multi" data-bs-toggle="collapse" class="sidebar-link collapsed">
        <i class="align-middle" data-feather="corner-right-down"></i>
        <span class="align-middle">Multi Nível</span>
    </a>
    <ul id="multi" class="sidebar-dropdown list-unstyled collapse">
        <li class="sidebar-item">
            <a data-bs-target="#multi-2" data-bs-toggle="collapse" class="sidebar-link collapsed">
                Dois Níveis
            </a>
            <ul id="multi-2" class="sidebar-dropdown list-unstyled collapse">
                <li class="sidebar-item">
                    <a class="sidebar-link" href="#">Item 1</a>
                </li>
                <li class="sidebar-item">
                    <a class="sidebar-link" href="#">Item 2</a>
                </li>
            </ul>
        </li>
        <li class="sidebar-item">
            <a data-bs-target="#multi-3" data-bs-toggle="collapse" class="sidebar-link collapsed">
                Três Níveis
            </a>
            <ul id="multi-3" class="sidebar-dropdown list-unstyled collapse">
                <li class="sidebar-item">
                    <a data-bs-target="#multi-3-1" data-bs-toggle="collapse" class="sidebar-link collapsed">
                        Item 1
                    </a>
                    <ul id="multi-3-1" class="sidebar-dropdown list-unstyled collapse">
                        <li class="sidebar-item">
                            <a class="sidebar-link" href="#">Subitem 1</a>
                        </li>
                        <li class="sidebar-item">
                            <a class="sidebar-link" href="#">Subitem 2</a>
                        </li>
                    </ul>
                </li>
                <li class="sidebar-item">
                    <a class="sidebar-link" href="#">Item 2</a>
                </li>
            </ul>
        </li>
    </ul>
</li>
```

## Ícones

O AdminKit Pro usa **Feather Icons** por padrão. Para adicionar ícones:

```html
<li class="sidebar-item">
    <a class="sidebar-link" href="#">
        <i class="align-middle" data-feather="home"></i>
        <span class="align-middle">Início</span>
    </a>
</li>
```

Ícones comuns disponíveis:
- `home` - Início
- `user` - Usuário
- `settings` - Configurações
- `sliders` - Dashboard
- `layout` - Páginas
- `briefcase` - Componentes
- `check-circle` - Formulários
- `list` - Tabelas/Tarefas
- `bar-chart-2` - Gráficos
- `bell` - Notificações
- `calendar` - Calendário
- `map` - Mapas

## Configuração

A sidebar pode ser configurada através de atributos `data` no elemento `<body>`:

```html
<body data-theme="default"
      data-layout="fluid"
      data-sidebar-position="left"
      data-sidebar-layout="default">
```

| Atributo | Valores | Descrição |
|----------|---------|-----------|
| `data-sidebar-position` | `left`, `right` | Posição da sidebar |
| `data-sidebar-layout` | `default`, `compact` | Layout da sidebar |

## JavaScript

### Toggle Sidebar

Botão para expandir/recolher a sidebar (na navbar):

```html
<a class="sidebar-toggle js-sidebar-toggle">
    <i class="hamburger align-self-center"></i>
</a>
```

### Inicialização

A sidebar é inicializada automaticamente pelo arquivo `js/app.js`. Certifique-se de incluir:

```html
<script src="js/app.js"></script>
```

## Acessibilidade

### ARIA Attributes

```html
<li class="sidebar-item">
    <a class="sidebar-link" href="pagina.html" aria-current="page">
        <i class="align-middle" data-feather="home"></i>
        <span class="align-middle">Início</span>
    </a>
</li>
```

Use `aria-current="page"` no item ativo para melhor acessibilidade.

## Personalização

### Cores

A sidebar herda as cores do tema. Para personalizar, sobrescreva as variáveis CSS:

```css
:root {
    --sidebar-bg: #2c3e50;
    --sidebar-color: #ecf0f1;
    --sidebar-active-bg: #34495e;
}
```

### Largura

```css
.sidebar {
    width: 250px;
}
```

### Animação

```css
.sidebar {
    transition: all 0.3s ease;
}
```

## Exemplo Completo

```html
<nav id="sidebar" class="sidebar js-sidebar">
    <div class="sidebar-content js-simplebar">
        <a class="sidebar-brand" href="index.html">
            <span class="sidebar-brand-text align-middle">MinhaApp</span>
        </a>

        <div class="sidebar-user">
            <div class="d-flex justify-content-center">
                <div class="flex-shrink-0">
                    <img src="img/avatars/avatar.jpg" class="avatar img-fluid rounded me-1" alt="Avatar" />
                </div>
                <div class="flex-grow-1 ps-2">
                    <a class="sidebar-user-title dropdown-toggle" href="#" data-bs-toggle="dropdown">
                        João Silva
                    </a>
                    <div class="dropdown-menu dropdown-menu-start">
                        <a class="dropdown-item" href="pages-profile.html">
                            <i class="align-middle me-1" data-feather="user"></i> Perfil
                        </a>
                        <a class="dropdown-item" href="#">
                            <i class="align-middle me-1" data-feather="pie-chart"></i> Analytics
                        </a>
                        <div class="dropdown-divider"></div>
                        <a class="dropdown-item" href="pages-settings.html">
                            <i class="align-middle me-1" data-feather="settings"></i> Configurações
                        </a>
                        <a class="dropdown-item" href="#">Sair</a>
                    </div>
                    <div class="sidebar-user-subtitle">Administrador</div>
                </div>
            </div>
        </div>

        <ul class="sidebar-nav">
            <li class="sidebar-header">Menu Principal</li>

            <li class="sidebar-item active">
                <a class="sidebar-link" href="index.html">
                    <i class="align-middle" data-feather="home"></i>
                    <span class="align-middle">Início</span>
                </a>
            </li>

            <li class="sidebar-item">
                <a data-bs-target="#admin" data-bs-toggle="collapse" class="sidebar-link collapsed">
                    <i class="align-middle" data-feather="settings"></i>
                    <span class="align-middle">Administração</span>
                </a>
                <ul id="admin" class="sidebar-dropdown list-unstyled collapse" data-bs-parent="#sidebar">
                    <li class="sidebar-item">
                        <a class="sidebar-link" href="admin-users.html">Usuários</a>
                    </li>
                    <li class="sidebar-item">
                        <a class="sidebar-link" href="admin-roles.html">Permissões</a>
                    </li>
                    <li class="sidebar-item">
                        <a class="sidebar-link" href="admin-logs.html">Logs</a>
                    </li>
                </ul>
            </li>

            <li class="sidebar-header">Sistema</li>

            <li class="sidebar-item">
                <a class="sidebar-link" href="pages-settings.html">
                    <i class="align-middle" data-feather="settings"></i>
                    <span class="align-middle">Configurações</span>
                </a>
            </li>

            <li class="sidebar-item">
                <a class="sidebar-link" href="pages-profile.html">
                    <i class="align-middle" data-feather="user"></i>
                    <span class="align-middle">Meu Perfil</span>
                </a>
            </li>
        </ul>

        <div class="sidebar-cta">
            <div class="sidebar-cta-content">
                <strong class="d-inline-block mb-2">Nova Versão</strong>
                <div class="mb-3 text-sm">
                    A versão 2.0 está disponível!
                </div>
                <div class="d-grid">
                    <a href="#" class="btn btn-outline-primary">Atualizar</a>
                </div>
            </div>
        </div>
    </div>
</nav>
```

## Troubleshooting

### Sidebar não aparece
- Verifique se `js/app.js` está incluído
- Confira se a classe `js-sidebar` está presente
- Verifique se não há conflitos de CSS

### Submenu não abre
- Confira se `data-bs-toggle="collapse"` e `data-bs-target` estão corretos
- Verifique se Bootstrap JS está carregado
- Confira se o ID do submenu é único

### Scroll não funciona
- Certifique-se de que a classe `js-simplebar` está presente
- Verifique se o plugin SimpleBar está carregado

## Recursos Adicionais

- [Feather Icons](https://feathericons.com/) - Ícones usados na sidebar
- [Bootstrap Collapse](https://getbootstrap.com/docs/5.3/components/collapse/) - Documentação do collapse
