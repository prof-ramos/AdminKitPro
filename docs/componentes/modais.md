# Modais

Os modais do AdminKit Pro são diálogos sobrepostos focados em conteúdo específico, perfeitos para formulários, confirmações e exibições detalhadas.

## Visão Geral

Os modais do AdminKit Pro incluem:
- **Backdrop**: Fundo escurecido para focar atenção
- **Teclado ESC**: Fechar com a tecla ESC
- **Click outside**: Fechar clicando fora do modal
- **Scrolling**: Conteúdo com scroll quando necessário
- **Responsividade**: Adaptam-se a diferentes tamanhos de tela
- **Animações**: Transições suaves de entrada/saída

## Modal Básico

```html
<!-- Botão de acionamento -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal"
        data-bs-target="#modalExemplo">
    Abrir Modal
</button>

<!-- Modal -->
<div class="modal fade" id="modalExemplo" tabindex="-1" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Título do Modal</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal" aria-label="Fechar"></button>
            </div>
            <div class="modal-body">
                <p>Este é um modal básico com título, corpo e botões de ação.</p>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-light"
                        data-bs-dismiss="modal">Fechar</button>
                <button type="button" class="btn btn-primary">Salvar</button>
            </div>
        </div>
    </div>
</div>
```

## Estrutura do Modal

| Parte | Classe | Descrição |
|-------|--------|-----------|
| Container | `.modal` | Container principal |
| Overlay | `.modal-dialog` | Janela do modal |
| Conteúdo | `.modal-content` | Conteúdo do modal |
| Cabeçalho | `.modal-header` | Header com título e fechar |
| Corpo | `.modal-body` | Conteúdo principal |
| Rodapé | `.modal-footer` | Botões de ação |

## Modal com Scroll

Quando o conteúdo é maior que a viewport:

```html
<div class="modal fade" id="modalScroll" tabindex="-1">
    <div class="modal-dialog modal-dialog-scrollable">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Modal com Scroll</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <p>Conteúdo longo...</p>
                <p>Mais conteúdo...</p>
                <!-- Conteúdo com scroll -->
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-primary"
                        data-bs-dismiss="modal">Fechar</button>
            </div>
        </div>
    </div>
</div>
```

## Modal Centralizado Verticalmente

```html
<div class="modal fade" id="modalCentro" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

## Tamanhos de Modal

### Pequeno

```html
<div class="modal fade" id="modalPequeno" tabindex="-1">
    <div class="modal-dialog modal-sm">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

### Médio (Padrão)

```html
<div class="modal fade" id="modalMedio" tabindex="-1">
    <div class="modal-dialog">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

### Grande

```html
<div class="modal fade" id="modalGrande" tabindex="-1">
    <div class="modal-dialog modal-lg">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

### Extra Grande

```html
<div class="modal fade" id="modalXG" tabindex="-1">
    <div class="modal-dialog modal-xl">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

### Fullscreen

```html
<!-- Fullscreen em todas as telas -->
<div class="modal fade" id="modalFull" tabindex="-1">
    <div class="modal-dialog modal-fullscreen">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>

<!-- Fullscreen apenas em telas pequenas -->
<div class="modal fade" id="modalFullSm" tabindex="-1">
    <div class="modal-dialog modal-fullscreen-sm-down">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

## Modal com Formulário

```html
<div class="modal fade" id="modalForm" tabindex="-1">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Novo Usuário</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <form>
                    <div class="mb-3">
                        <label class="form-label" for="nome">Nome</label>
                        <input type="text" class="form-control" id="nome">
                    </div>
                    <div class="mb-3">
                        <label class="form-label" for="email">Email</label>
                        <input type="email" class="form-control" id="email">
                    </div>
                    <div class="mb-3">
                        <label class="form-label" for="cargo">Cargo</label>
                        <select class="form-select" id="cargo">
                            <option>Selecione...</option>
                            <option>Desenvolvedor</option>
                            <option>Designer</option>
                            <option>Gerente</option>
                        </select>
                    </div>
                </form>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-light"
                        data-bs-dismiss="modal">Cancelar</button>
                <button type="button" class="btn btn-primary">Salvar</button>
            </div>
        </div>
    </div>
</div>
```

## Modal de Confirmação

```html
<div class="modal fade" id="modalConfirmacao" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Confirmar Exclusão</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <p>Tem certeza que deseja excluir este item?</p>
                <p class="text-muted small">Esta ação não pode ser desfeita.</p>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-light"
                        data-bs-dismiss="modal">Cancelar</button>
                <button type="button" class="btn btn-danger">Excluir</button>
            </div>
        </div>
    </div>
</div>
```

## Modal com Imagem

```html
<div class="modal fade" id="modalImagem" tabindex="-1">
    <div class="modal-dialog modal-lg modal-dialog-centered">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Visualizar Imagem</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body p-0">
                <img src="img/photos/large.jpg"
                     class="img-fluid w-100"
                     alt="Imagem">
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-primary"
                        data-bs-dismiss="modal">Fechar</button>
            </div>
        </div>
    </div>
</div>
```

## Modal com Alerta

```html
<div class="modal fade" id="modalAlerta" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <div class="modal-header bg-danger text-white">
                <h5 class="modal-title text-white">Atenção!</h5>
                <button type="button" class="btn-close btn-close-white"
                        data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <div class="alert alert-danger">
                    <i class="align-middle" data-feather="alert-circle"></i>
                    Esta é uma mensagem importante que requer sua atenção.
                </div>
                <p>Detalhes adicionais sobre o alerta...</p>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-light"
                        data-bs-dismiss="modal">Entendi</button>
                <button type="button" class="btn btn-danger">Continuar</button>
            </div>
        </div>
    </div>
</div>
```

## Modal com Tabs

```html
<div class="modal fade" id="modalTabs" tabindex="-1">
    <div class="modal-dialog modal-lg">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Modal com Tabs</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <ul class="nav nav-tabs mb-3" role="tablist">
                    <li class="nav-item">
                        <a class="nav-link active" data-bs-toggle="tab"
                           href="#tabInfo">Informações</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" data-bs-toggle="tab"
                           href="#tabHistorico">Histórico</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" data-bs-toggle="tab"
                           href="#tabConfig">Configurações</a>
                    </li>
                </ul>
                <div class="tab-content">
                    <div class="tab-pane fade show active" id="tabInfo">
                        <p>Conteúdo das informações...</p>
                    </div>
                    <div class="tab-pane fade" id="tabHistorico">
                        <p>Conteúdo do histórico...</p>
                    </div>
                    <div class="tab-pane fade" id="tabConfig">
                        <p>Conteúdo das configurações...</p>
                    </div>
                </div>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-light"
                        data-bs-dismiss="modal">Fechar</button>
                <button type="button" class="btn btn-primary">Salvar</button>
            </div>
        </div>
    </div>
</div>
```

## Modal com Progresso

```html
<div class="modal fade" id="modalProgresso" tabindex="-1">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Processando...</h5>
            </div>
            <div class="modal-body text-center">
                <div class="mb-3">
                    <div class="spinner-border text-primary" role="status">
                        <span class="visually-hidden">Carregando...</span>
                    </div>
                </div>
                <p>Aguarde enquanto processamos sua solicitação.</p>
                <div class="progress">
                    <div class="progress-bar progress-bar-striped progress-bar-animated"
                         role="progressbar" style="width: 75%"></div>
                </div>
            </div>
        </div>
    </div>
</div>
```

## Modal com Tabela

```html
<div class="modal fade" id="modalTabela" tabindex="-1">
    <div class="modal-dialog modal-xl">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Detalhes dos Pedidos</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <div class="table-responsive">
                    <table class="table table-hover">
                        <thead>
                            <tr>
                                <th>Pedido</th>
                                <th>Cliente</th>
                                <th>Data</th>
                                <th>Valor</th>
                                <th>Status</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>#12345</td>
                                <td>João Silva</td>
                                <td>17/02/2026</td>
                                <td>R$ 150,00</td>
                                <td><span class="badge bg-success">Pago</span></td>
                            </tr>
                            <!-- Mais linhas -->
                        </tbody>
                    </table>
                </div>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-light"
                        data-bs-dismiss="modal">Fechar</button>
                <button type="button" class="btn btn-primary">Exportar</button>
            </div>
        </div>
    </div>
</div>
```

## Controlando via JavaScript

### Abrir Modal

```javascript
var modal = new bootstrap.Modal(document.getElementById('modalExemplo'));
modal.show();
```

### Fechar Modal

```javascript
var modal = new bootstrap.Modal(document.getElementById('modalExemplo'));
modal.hide();
```

### Toggle Modal

```javascript
var modal = new bootstrap.Modal(document.getElementById('modalExemplo'));
modal.toggle();
```

### Eventos do Modal

```javascript
var modalElement = document.getElementById('modalExemplo');

modalElement.addEventListener('show.bs.modal', function() {
    console.log('Modal está sendo aberto');
});

modalElement.addEventListener('shown.bs.modal', function() {
    console.log('Modal foi aberto completamente');
});

modalElement.addEventListener('hide.bs.modal', function() {
    console.log('Modal está sendo fechado');
});

modalElement.addEventListener('hidden.bs.modal', function() {
    console.log('Modal foi fechado completamente');
});
```

## Sem Backdrop

```html
<div class="modal fade" id="modalSemBackdrop" tabindex="-1"
     data-bs-backdrop="false">
    <div class="modal-dialog">
        <div class="modal-content">
            <!-- Conteúdo -->
        </div>
    </div>
</div>
```

## Backdrop Estático

Não fecha ao clicar fora:

```html
<div class="modal fade" id="modalBackdropStatic" tabindex="-1"
     data-bs-backdrop="static" data-bs-keyboard="false">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Atenção</h5>
            </div>
            <div class="modal-body">
                <p>Você deve confirmar esta ação antes de continuar.</p>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-primary"
                        data-bs-dismiss="modal">Confirmar</button>
            </div>
        </div>
    </div>
</div>
```

## Classes CSS

### Estrutura
| Classe | Descrição |
|--------|-----------|
| `.modal` | Container principal |
| `.modal-dialog` | Janela do modal |
| `.modal-content` | Conteúdo do modal |
| `.modal-header` | Cabeçalho |
| `.modal-body` | Corpo |
| `.modal-footer` | Rodapé |

### Modificadores
| Classe | Descrição |
|--------|-----------|
| `.fade` | Adiciona animação de fade |
| `.modal-dialog-centered` | Centraliza verticalmente |
| `.modal-dialog-scrollable` | Permite scroll no corpo |
| `.modal-sm` | Modal pequeno |
| `.modal-lg` | Modal grande |
| `.modal-xl` | Modal extra grande |
| `.modal-fullscreen` | Modal tela cheia |

## Acessibilidade

### ARIA Attributes

```html
<div class="modal fade" id="modalAcessivel" tabindex="-1"
     role="dialog" aria-labelledby="modalTitulo" aria-hidden="true">
    <div class="modal-dialog" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="modalTitulo">Título</h5>
                <button type="button" class="btn-close"
                        data-bs-dismiss="modal"
                        aria-label="Fechar"></button>
            </div>
            <div class="modal-body">
                <!-- Conteúdo -->
            </div>
        </div>
    </div>
</div>
```

## Exemplos Práticos

- `ui-modals.html` - Demonstração completa de modais

## Recursos Adicionais

- [Bootstrap Modals](https://getbootstrap.com/docs/5.3/components/modal/) - Documentação oficial
