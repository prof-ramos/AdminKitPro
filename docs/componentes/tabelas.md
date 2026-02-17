# Tabelas

As tabelas do AdminKit Pro permitem exibir dados de forma organizada e legível, com suporte a recursos avançados como ordenação, busca e paginação.

## Visão Geral

O AdminKit Pro suporta:
- **Tabelas Bootstrap**: Tabelas padrão do Bootstrap 5
- **DataTables**: Tabelas avançadas com ordenação, busca e paginação
- **Tabelas Responsivas**: Adaptam-se a diferentes tamanhos de tela
- **Tabelas com Ações**: Botões e dropdowns em cada linha
- **Tabelas com Checkbox**: Seleção múltipla de linhas

## Tabela Básica

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Tabela Simples</h5>
    </div>
    <div class="card-body">
        <table class="table">
            <thead>
                <tr>
                    <th>Nome</th>
                    <th>Email</th>
                    <th>Cargo</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>João Silva</td>
                    <td>joao@email.com</td>
                    <td>Desenvolvedor</td>
                    <td><span class="badge bg-success">Ativo</span></td>
                </tr>
                <tr>
                    <td>Maria Santos</td>
                    <td>maria@email.com</td>
                    <td>Designer</td>
                    <td><span class="badge bg-warning">Pendente</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
```

## Tabela Sem Bordas

```html
<table class="table table-borderless">
    <thead>
        <tr>
            <th>Nome</th>
            <th>Email</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>João Silva</td>
            <td>joao@email.com</td>
        </tr>
    </tbody>
</table>
```

## Tabela com Hover

```html
<table class="table table-hover">
    <!-- Linhas destacadas ao passar o mouse -->
</table>
```

## Tabela Compacta

```html
<table class="table table-sm">
    <!-- Linhas com menos espaçamento -->
</table>
```

## Tabela com Striped

```html
<table class="table table-striped">
    <!-- Linhas alternadas com cores diferentes -->
</table>
```

## Tabela Responsiva

```html
<div class="table-responsive">
    <table class="table">
        <!-- Tabela com scroll horizontal em telas pequenas -->
    </table>
</div>
```

## Tabela com Borda Externa

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Tabela com Borda</h5>
    </div>
    <div class="card-body p-0">
        <table class="table table-striped mb-0">
            <thead>
                <tr>
                    <th>Nome</th>
                    <th>Email</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>João Silva</td>
                    <td>joao@email.com</td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
```

## Tabela com Ações

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Tabela com Ações</h5>
    </div>
    <div class="card-body">
        <table class="table">
            <thead>
                <tr>
                    <th>Nome</th>
                    <th>Email</th>
                    <th>Status</th>
                    <th class="text-end">Ações</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>João Silva</td>
                    <td>joao@email.com</td>
                    <td><span class="badge bg-success">Ativo</span></td>
                    <td class="text-end">
                        <button class="btn btn-light btn-sm">
                            <i class="align-middle" data-feather="edit-2"></i>
                        </button>
                        <button class="btn btn-light btn-sm">
                            <i class="align-middle" data-feather="trash"></i>
                        </button>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
```

## Tabela com Dropdown de Ações

```html
<table class="table">
    <thead>
        <tr>
            <th>Nome</th>
            <th>Ações</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>João Silva</td>
            <td>
                <div class="dropdown">
                    <button class="btn btn-light btn-sm dropdown-toggle"
                            type="button" data-bs-toggle="dropdown">
                        Ações
                    </button>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">Ver</a></li>
                        <li><a class="dropdown-item" href="#">Editar</a></li>
                        <li><hr class="dropdown-divider"></li>
                        <li><a class="dropdown-item text-danger" href="#">Excluir</a></li>
                    </ul>
                </div>
            </td>
        </tr>
    </tbody>
</table>
```

## Tabela com Checkbox

```html
<div class="card">
    <div class="card-header">
        <div class="row align-items-center">
            <div class="col">
                <h5 class="card-title mb-0">Tabela com Seleção</h5>
            </div>
            <div class="col-auto">
                <button class="btn btn-primary btn-sm">
                    <i class="align-middle" data-feather="trash"></i>
                    Excluir Selecionados
                </button>
            </div>
        </div>
    </div>
    <div class="card-body">
        <table class="table">
            <thead>
                <tr>
                    <th>
                        <div class="form-check">
                            <input class="form-check-input" type="checkbox"
                                   id="checkAll">
                        </div>
                    </th>
                    <th>Nome</th>
                    <th>Email</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>
                        <div class="form-check">
                            <input class="form-check-input" type="checkbox"
                                   id="check1">
                        </div>
                    </td>
                    <td>João Silva</td>
                    <td>joao@email.com</td>
                </tr>
            </tbody>
        </table>
    </div>
</div>
```

## Tabela com Avatar

```html
<table class="table">
    <thead>
        <tr>
            <th>Usuário</th>
            <th>Email</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <div class="d-flex align-items-center">
                    <div class="flex-shrink-0">
                        <img src="img/avatars/avatar.jpg"
                             class="avatar rounded-circle me-2"
                             alt="Avatar">
                    </div>
                    <div class="flex-grow-1">
                        João Silva
                    </div>
                </div>
            </td>
            <td>joao@email.com</td>
        </tr>
    </tbody>
</table>
```

## Tabela com Progresso

```html
<table class="table">
    <thead>
        <tr>
            <th>Projeto</th>
            <th>Progresso</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Website</td>
            <td>
                <div class="d-flex align-items-center">
                    <div class="flex-grow-1">
                        <div class="progress progress-sm">
                            <div class="progress-bar bg-success"
                                 role="progressbar"
                                 style="width: 75%;"></div>
                        </div>
                    </div>
                    <div class="flex-shrink-0 ms-3">
                        <span class="text-muted">75%</span>
                    </div>
                </div>
            </td>
        </tr>
    </tbody>
</table>
```

## Tabela com Status Colorido

```html
<table class="table">
    <thead>
        <tr>
            <th>Pedido</th>
            <th>Cliente</th>
            <th>Status</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>#12345</td>
            <td>João Silva</td>
            <td><span class="badge bg-success">Pago</span></td>
        </tr>
        <tr>
            <td>#12346</td>
            <td>Maria Santos</td>
            <td><span class="badge bg-warning">Pendente</span></td>
        </tr>
        <tr>
            <td>#12347</td>
            <td>Pedro Costa</td>
            <td><span class="badge bg-danger">Cancelado</span></td>
        </tr>
        <tr>
            <td>#12348</td>
            <td>Ana Lima</td>
            <td><span class="badge bg-info">Processando</span></td>
        </tr>
    </tbody>
</table>
```

## DataTables

O AdminKit Pro suporta DataTables para tabelas avançadas.

### DataTables Básico

```html
<table id="dataTable" class="table table-striped" style="width:100%">
    <thead>
        <tr>
            <th>Nome</th>
            <th>Cargo</th>
            <th>Escritório</th>
            <th>Idade</th>
            <th>Data de Início</th>
            <th>Salário</th>
        </tr>
    </thead>
    <tbody>
        <!-- Dados -->
    </tbody>
</table>

<script>
    $(document).ready(function() {
        $('#dataTable').DataTable();
    });
</script>
```

### DataTables com Botões

```html
<table id="dataTableButtons" class="table table-striped" style="width:100%">
    <!-- Dados -->
</table>

<script>
    $(document).ready(function() {
        $('#dataTableButtons').DataTable({
            dom: 'Bfrtip',
            buttons: [
                'copy', 'csv', 'excel', 'pdf', 'print'
            ],
            language: {
                url: '//cdn.datatables.net/plug-ins/1.13.4/i18n/pt_BR.json'
            }
        });
    });
</script>
```

### DataTables Responsivo

```html
<div class="table-responsive">
    <table id="dataTableResponsive" class="table table-striped" style="width:100%">
        <!-- Dados -->
    </table>
</div>

<script>
    $(document).ready(function() {
        $('#dataTableResponsive').DataTable({
            responsive: true
        });
    });
</script>
```

### DataTables com Busca por Coluna

```html
<table id="dataTableColumnSearch" class="table table-striped" style="width:100%">
    <thead>
        <tr>
            <th>Nome</th>
            <th>Cargo</th>
            <th>Escritório</th>
        </tr>
    </thead>
    <tbody>
        <!-- Dados -->
    </tbody>
</table>

<script>
    $(document).ready(function() {
        var table = $('#dataTableColumnSearch').DataTable();

        // Setup - add a text input to each footer cell
        $('#dataTableColumnSearch thead th').each(function() {
            var title = $(this).text();
            $(this).html('<input type="text" placeholder="Buscar ' + title + '" />');
        });

        // Apply the search
        table.columns().every(function() {
            var that = this;
            $('input', this.header()).on('keyup change clear', function() {
                if (that.search() !== this.value) {
                    that.search(this.value).draw();
                }
            });
        });
    });
</script>
```

### DataTables com Cabeçalho Fixo

```html
<div style="position: relative;">
    <table id="dataTableFixedHeader" class="table table-striped" style="width:100%">
        <!-- Dados -->
    </table>
</div>

<script>
    $(document).ready(function() {
        new DataTable('#dataTableFixedHeader', {
            fixedHeader: true
        });
    });
</script>
```

### DataTables com Seleção Múltipla

```html
<table id="dataTableMulti" class="table table-striped display" style="width:100%">
    <!-- Dados -->
</table>

<script>
    $(document).ready(function() {
        var table = $('#dataTableMulti').DataTable({
            columnDefs: [{
                orderable: false,
                className: 'select-checkbox',
                targets: 0
            }],
            select: {
                style: 'os',
                selector: 'td:first-child'
            },
            order: [[1, 'asc']]
        });
    });
</script>
```

### DataTables com AJAX

```html
<table id="dataTableAjax" class="table table-striped" style="width:100%">
    <thead>
        <tr>
            <th>Nome</th>
            <th>Cargo</th>
            <th>Escritório</th>
            <th>Idade</th>
        </tr>
    </thead>
</table>

<script>
    $(document).ready(function() {
        $('#dataTableAjax').DataTable({
            ajax: 'tables-datatables-ajax.json',
            columns: [
                {data: 'nome'},
                {data: 'cargo'},
                {data: 'escritorio'},
                {data: 'idade'}
            ]
        });
    });
</script>
```

## Tradução em Português

Para traduzir as DataTables para português:

```javascript
$('#minhaTabela').DataTable({
    language: {
        url: '//cdn.datatables.net/plug-ins/1.13.4/i18n/pt_BR.json'
    }
});
```

Ou manualmente:

```javascript
$('#minhaTabela').DataTable({
    language: {
        processing: "Processando...",
        search: "Buscar:",
        lengthMenu: "Mostrar _MENU_ registros",
        info: "Mostrando _START_ a _END_ de _TOTAL_ registros",
        infoEmpty: "Mostrando 0 a 0 de 0 registros",
        infoFiltered: "(filtrado de _MAX_ registros no total)",
        paginate: {
            first: "Primeiro",
            previous: "Anterior",
            next: "Próximo",
            last: "Último"
        }
    }
});
```

## Classes CSS

### Estrutura
| Classe | Descrição |
|--------|-----------|
| `.table` | Classe base da tabela |
| `.table-striped` | Linhas zebradas |
| `.table-bordered` | Tabela com bordas |
| `.table-borderless` | Sem bordas |
| `.table-hover` | Efeito hover nas linhas |
| `.table-sm` | Tabela compacta |
| `.table-responsive` | Tabela responsiva |

### Alinhamento
| Classe | Descrição |
|--------|-----------|
| `.text-start` | Alinhamento à esquerda |
| `.text-center` | Alinhamento ao centro |
| `.text-end` | Alinhamento à direita |

## Exemplos Práticos

- `tables-bootstrap.html` - Tabelas Bootstrap básicas
- `tables-datatables-responsive.html` - DataTables responsivos
- `tables-datatables-buttons.html` - DataTables com botões de exportação
- `tables-datatables-column-search.html` - Busca por coluna
- `tables-datatables-fixed-header.html` - Cabeçalho fixo
- `tables-datatables-multi.html` - Seleção múltipla
- `tables-datatables-ajax.html` - Dados via AJAX

## Recursos Adicionais

- [Bootstrap Tables](https://getbootstrap.com/docs/5.3/content/tables/) - Documentação oficial
- [DataTables](https://datatables.net/) - Plugin de tabelas avançadas
- [DataTables Brazilian Portuguese](https://datatables.net/plug-ins/i18n/pt-BR/) - Tradução PT-BR
