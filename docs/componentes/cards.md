# Cards (Cartões)

Os cards são componentes versáteis e flexíveis para organizar e apresentar conteúdo de forma estruturada no AdminKit Pro.

## Visão Geral

Os cards do AdminKit Pro são perfeitos para:
- Apresentar estatísticas e métricas
- Exibir informações resumidas
- Agrupar conteúdo relacionado
- Criar widgets interativos
- Organizar formulários

## Estrutura Básica

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Título do Card</h5>
    </div>
    <div class="card-body">
        <p class="card-text">Conteúdo do card...</p>
    </div>
    <div class="card-footer">
        <!-- Rodapé do card -->
    </div>
</div>
```

## Card Simples

```html
<div class="card">
    <div class="card-body">
        <h5 class="card-title">Título do Card</h5>
        <p class="card-text">Este é um card simples com título e texto.</p>
        <a href="#" class="btn btn-primary">Ação</a>
    </div>
</div>
```

## Card com Imagem

```html
<div class="card">
    <img class="card-img-top" src="img/photos/unsplash-1.jpg" alt="Imagem">
    <div class="card-header">
        <h5 class="card-title mb-0">Card com Imagem</h5>
    </div>
    <div class="card-body">
        <p class="card-text">Card com imagem no topo e conteúdo abaixo.</p>
    </div>
</div>
```

## Card com Ações

Menu de ações no header:

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
                    <a class="dropdown-item" href="#">Ação 3</a>
                </div>
            </div>
        </div>
        <h5 class="card-title mb-0">Card com Ações</h5>
    </div>
    <div class="card-body">
        <p class="card-text">Conteúdo do card...</p>
    </div>
</div>
```

## Card com Tabs

Abas na parte superior do card:

```html
<div class="card">
    <div class="card-header">
        <ul class="nav nav-tabs card-header-tabs" role="tablist">
            <li class="nav-item">
                <a class="nav-link active" data-bs-toggle="tab" href="#tab1">
                    Aba 1
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" data-bs-toggle="tab" href="#tab2">
                    Aba 2
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link disabled" data-bs-toggle="tab" href="#tab3">
                    Aba 3
                </a>
            </li>
        </ul>
    </div>
    <div class="card-body">
        <div class="tab-content">
            <div class="tab-pane fade show active" id="tab1" role="tabpanel">
                <h5 class="card-title">Conteúdo da Aba 1</h5>
                <p class="card-text">Texto da primeira aba...</p>
            </div>
            <div class="tab-pane fade" id="tab2" role="tabpanel">
                <h5 class="card-title">Conteúdo da Aba 2</h5>
                <p class="card-text">Texto da segunda aba...</p>
            </div>
            <div class="tab-pane fade" id="tab3" role="tabpanel">
                <h5 class="card-title">Conteúdo da Aba 3</h5>
                <p class="card-text">Texto da terceira aba...</p>
            </div>
        </div>
    </div>
</div>
```

## Card com Pills

Abas estilo pílula:

```html
<div class="card">
    <div class="card-header">
        <ul class="nav nav-pills card-header-pills" role="tablist">
            <li class="nav-item">
                <a class="nav-link active" data-bs-toggle="tab" href="#pill1">
                    Ativo
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link" data-bs-toggle="tab" href="#pill2">
                    Link
                </a>
            </li>
        </ul>
    </div>
    <div class="card-body">
        <div class="tab-content">
            <div class="tab-pane fade show active" id="pill1" role="tabpanel">
                <h5 class="card-title">Card com Pills</h5>
                <p class="card-text">Conteúdo da primeira pílula...</p>
            </div>
            <div class="tab-pane fade" id="pill2" role="tabpanel">
                <h5 class="card-title">Card com Pills</h5>
                <p class="card-text">Conteúdo da segunda pílula...</p>
            </div>
        </div>
    </div>
</div>
```

## Card com List Group

Lista de itens no card:

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Card com Lista</h5>
    </div>
    <ul class="list-group list-group-flush">
        <li class="list-group-item">Item 1 da lista</li>
        <li class="list-group-item">Item 2 da lista</li>
        <li class="list-group-item">Item 3 da lista</li>
        <li class="list-group-item">Item 4 da lista</li>
    </ul>
    <div class="card-footer">
        <a href="#" class="btn btn-primary">Ver Todos</a>
    </div>
</div>
```

## Card de Estatísticas

Card para exibir métricas:

```html
<div class="card">
    <div class="card-body">
        <div class="row">
            <div class="col mt-0">
                <h5 class="card-title">Vendas</h5>
            </div>
            <div class="col-auto">
                <div class="stat text-primary">
                    <i class="align-middle" data-feather="truck"></i>
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

### Cores de Estatísticas

```html
<!-- Primária -->
<div class="stat text-primary">
    <i class="align-middle" data-feather="shopping-cart"></i>
</div>

<!-- Sucesso -->
<div class="stat text-success">
    <i class="align-middle" data-feather="check-circle"></i>
</div>

<!-- Aviso -->
<div class="stat text-warning">
    <i class="align-middle" data-feather="alert-triangle"></i>
</div>

<!-- Perigo -->
<div class="stat text-danger">
    <i class="align-middle" data-feather="alert-circle"></i>
</div>

<!-- Informação -->
<div class="stat text-info">
    <i class="align-middle" data-feather="info"></i>
</div>
```

## Card de Progresso

Exibe progresso de uma tarefa:

```html
<div class="card">
    <div class="card-body">
        <div class="d-flex justify-content-between mb-2">
            <h5 class="card-title">Progresso do Projeto</h5>
            <span class="text-muted">65%</span>
        </div>
        <div class="progress progress-sm">
            <div class="progress-bar bg-success" role="progressbar"
                 style="width: 65%;" aria-valuenow="65"
                 aria-valuemin="0" aria-valuemax="100"></div>
        </div>
        <div class="mt-3">
            <small class="text-muted">Atualizado há 2 horas</small>
        </div>
    </div>
</div>
```

## Card com Gráfico

Contém um gráfico Chart.js:

```html
<div class="card">
    <div class="card-header">
        <div class="card-actions float-end">
            <div class="dropdown position-relative">
                <a href="#" data-bs-toggle="dropdown">
                    <i class="align-middle" data-feather="more-horizontal"></i>
                </a>
                <div class="dropdown-menu dropdown-menu-end">
                    <a class="dropdown-item" href="#">Esta Semana</a>
                    <a class="dropdown-item" href="#">Este Mês</a>
                    <a class="dropdown-item" href="#">Este Ano</a>
                </div>
            </div>
        </div>
        <h5 class="card-title mb-0">Vendas Mensais</h5>
    </div>
    <div class="card-body">
        <div class="chart">
            <canvas id="chart-sales"></canvas>
        </div>
    </div>
</div>
```

## Card com Tabela

Tabela dentro do card:

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Últimos Pedidos</h5>
    </div>
    <div class="card-body">
        <table class="table table-borderless mb-0">
            <thead>
                <tr>
                    <th>Cliente</th>
                    <th>Produto</th>
                    <th>Valor</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>João Silva</td>
                    <td>Produto A</td>
                    <td>R$ 150,00</td>
                    <td><span class="badge bg-success">Pago</span></td>
                </tr>
                <tr>
                    <td>Maria Santos</td>
                    <td>Produto B</td>
                    <td>R$ 230,00</td>
                    <td><span class="badge bg-warning">Pendente</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
```

## Card com Imagem de Fundo

Card com imagem de fundo e sobreposição:

```html
<div class="card text-white bg-cover"
     style="background-image: url('img/photos/unsplash-1.jpg');">
    <div class="card-img-overlay d-flex flex-column">
        <div class="card-body">
            <h3 class="card-title text-white mb-1">Título sobre Imagem</h3>
            <p class="card-text text-white-50">Descrição do card com imagem de fundo...</p>
        </div>
    </div>
</div>
```

## Card com Formulário

Formulário dentro do card:

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Formulário de Contato</h5>
    </div>
    <div class="card-body">
        <form>
            <div class="mb-3">
                <label class="form-label" for="nome">Nome</label>
                <input type="text" class="form-control" id="nome"
                       placeholder="Seu nome">
            </div>
            <div class="mb-3">
                <label class="form-label" for="email">Email</label>
                <input type="email" class="form-control" id="email"
                       placeholder="seu@email.com">
            </div>
            <div class="mb-3">
                <label class="form-label" for="mensagem">Mensagem</label>
                <textarea class="form-control" id="mensagem" rows="3"></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Enviar</button>
        </form>
    </div>
</div>
```

## Card com Avatar e Informações

Card de perfil de usuário:

```html
<div class="card">
    <div class="card-body text-center">
        <img src="img/avatars/avatar.jpg"
             class="avatar avatar-xl rounded-circle mb-3"
             alt="Avatar">
        <h5 class="card-title mb-0">Charles Hall</h5>
        <div class="text-muted mb-3">Designer</div>
        <p class="card-text mb-3">
            Especialista em UI/UX com foco em criar experiências incríveis.
        </p>
        <div class="mb-3">
            <a href="#" class="btn btn-primary me-1">Seguir</a>
            <a href="#" class="btn btn-light">Mensagem</a>
        </div>
        <div class="row text-center">
            <div class="col">
                <div class="fw-bold">1.2K</div>
                <div class="text-muted small">Seguidores</div>
            </div>
            <div class="col">
                <div class="fw-bold">256</div>
                <div class="text-muted small">Seguindo</div>
            </div>
            <div class="col">
                <div class="fw-bold">89</div>
                <div class="text-muted small">Projetos</div>
            </div>
        </div>
    </div>
</div>
```

## Cards Coloridos

Com diferentes cores de fundo:

```html
<!-- Primário -->
<div class="card bg-primary text-white">
    <div class="card-body">
        <h5 class="card-title text-white">Card Primário</h5>
        <p class="card-text text-white-50">Conteúdo do card...</p>
    </div>
</div>

<!-- Sucesso -->
<div class="card bg-success text-white">
    <div class="card-body">
        <h5 class="card-title text-white">Card de Sucesso</h5>
        <p class="card-text text-white-50">Conteúdo do card...</p>
    </div>
</div>

<!-- Aviso -->
<div class="card bg-warning text-dark">
    <div class="card-body">
        <h5 class="card-title">Card de Aviso</h5>
        <p class="card-text">Conteúdo do card...</p>
    </div>
</div>

<!-- Perigo -->
<div class="card bg-danger text-white">
    <div class="card-body">
        <h5 class="card-title text-white">Card de Perigo</h5>
        <p class="card-text text-white-50">Conteúdo do card...</p>
    </div>
</div>
```

## Card com Badge de Status

```html
<div class="card">
    <div class="card-body">
        <div class="d-flex align-items-center">
            <div class="flex-shrink-0">
                <div class="bg-primary rounded-3 p-3">
                    <i class="align-middle text-white" data-feather="package"></i>
                </div>
            </div>
            <div class="flex-grow-1 ms-3">
                <h5 class="card-title mb-1">Novo Pedido</h5>
                <div class="text-muted small">Pedido #12345</div>
            </div>
            <div class="flex-shrink-0">
                <span class="badge bg-success">Confirmado</span>
            </div>
        </div>
    </div>
</div>
```

## Grid de Cards

Vários cards em uma grade:

```html
<div class="row">
    <div class="col-sm-6 col-xl-3">
        <div class="card">
            <div class="card-body">
                <h5 class="card-title">Card 1</h5>
                <p class="card-text">Conteúdo do card 1...</p>
            </div>
        </div>
    </div>
    <div class="col-sm-6 col-xl-3">
        <div class="card">
            <div class="card-body">
                <h5 class="card-title">Card 2</h5>
                <p class="card-text">Conteúdo do card 2...</p>
            </div>
        </div>
    </div>
    <div class="col-sm-6 col-xl-3">
        <div class="card">
            <div class="card-body">
                <h5 class="card-title">Card 3</h5>
                <p class="card-text">Conteúdo do card 3...</p>
            </div>
        </div>
    </div>
    <div class="col-sm-6 col-xl-3">
        <div class="card">
            <div class="card-body">
                <h5 class="card-title">Card 4</h5>
                <p class="card-text">Conteúdo do card 4...</p>
            </div>
        </div>
    </div>
</div>
```

## Classes CSS

### Estrutura
| Classe | Descrição |
|--------|-----------|
| `.card` | Container principal do card |
| `.card-header` | Cabeçalho do card |
| `.card-body` | Conteúdo principal do card |
| `.card-footer` | Rodapé do card |
| `.card-title` | Título do card |
| `.card-text` | Texto do card |
| `.card-img-top` | Imagem no topo |
| `.card-img-bottom` | Imagem no rodapé |
| `.card-img-overlay` | Sobreposição de imagem |

### Modificadores
| Classe | Descrição |
|--------|-----------|
| `.card-actions` | Ações do card |
| `.float-end` | Alinha à direita |
| `.bg-cover` | Imagem de fundo cobre o card |
| `.text-white` | Texto branco |
| `.text-white-50` | Texto branco com 50% opacidade |

## Personalização

### Sombras

```html
<!-- Sem sombra -->
<div class="card shadow-none">

<!-- Sombra pequena -->
<div class="card shadow-sm">

<!-- Sombra regular -->
<div class="card shadow">

<!-- Sombra grande -->
<div class="card shadow-lg">
```

### Bordas

```html
<!-- Sem borda -->
<div class="card border-0">

<!-- Borda superior -->
<div class="card border-top border-primary">

<!-- Borda inferior -->
<div class="card border-bottom border-success">
```

### Hover Effect

```css
.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
}
```

## Acessibilidade

### ARIA Labels

```html
<div class="card" role="article">
    <div class="card-header">
        <h5 class="card-title" id="card-title-1">Título</h5>
    </div>
    <div class="card-body" aria-labelledby="card-title-1">
        <p class="card-text">Conteúdo...</p>
    </div>
</div>
```

## Exemplos Práticos

Veja exemplos práticos em:
- `ui-cards.html` - Demonstração completa de cards
- `index.html` - Dashboard com cards de estatísticas
- `dashboard-ecommerce.html` - Cards de e-commerce

## Recursos Adicionais

- [Bootstrap Cards](https://getbootstrap.com/docs/5.3/components/card/) - Documentação oficial
- [Chart.js](https://www.chartjs.org/) - Gráficos para cards
