# Formulários

Os formulários do AdminKit Pro são estilizados e funcionais, perfeitos para coletar dados dos usuários com uma experiência consistente.

## Visão Geral

O AdminKit Pro oferece:
- **Inputs básicos**: Campos de texto, email, senha, etc.
- **Layouts de formulário**: Vertical, horizontal, inline
- **Grupos de inputs**: Agrupamento de campos relacionados
- **Validação**: Feedback visual de validação
- **Inputs avançados**: Selects, textareas, checkboxes, radios
- **Plugins**: Datepicker, editor de texto, upload

## Input Básico

### Texto

```html
<div class="mb-3">
    <label class="form-label" for="nome">Nome Completo</label>
    <input type="text" class="form-control" id="nome"
           placeholder="Digite seu nome">
</div>
```

### Email

```html
<div class="mb-3">
    <label class="form-label" for="email">Email</label>
    <input type="email" class="form-control" id="email"
           placeholder="nome@exemplo.com">
</div>
```

### Senha

```html
<div class="mb-3">
    <label class="form-label" for="senha">Senha</label>
    <input type="password" class="form-control" id="senha"
           placeholder="Digite sua senha">
</div>
```

### Número

```html
<div class="mb-3">
    <label class="form-label" for="idade">Idade</label>
    <input type="number" class="form-control" id="idade"
           placeholder="Digite sua idade">
</div>
```

### Data

```html
<div class="mb-3">
    <label class="form-label" for="data">Data de Nascimento</label>
    <input type="date" class="form-control" id="data">
</div>
```

## Input com Descrição

```html
<div class="mb-3">
    <label class="form-label" for="senha">Senha</label>
    <input type="password" class="form-control" id="senha">
    <div class="form-text">Mínimo de 8 caracteres com letras e números.</div>
</div>
```

## Input Tamanho

```html
<!-- Input pequeno -->
<input type="text" class="form-control form-control-sm" placeholder="Pequeno">

<!-- Input normal -->
<input type="text" class="form-control" placeholder="Normal">

<!-- Input grande -->
<input type="text" class="form-control form-control-lg" placeholder="Grande">
```

## Select

### Select Simples

```html
<div class="mb-3">
    <label class="form-label" for="cargo">Cargo</label>
    <select class="form-select" id="cargo">
        <option selected>Selecione...</option>
        <option value="1">Desenvolvedor</option>
        <option value="2">Designer</option>
        <option value="3">Gerente</option>
    </select>
</div>
```

### Select com Tamanho

```html
<!-- Select pequeno -->
<select class="form-select form-select-sm">
    <!-- Opções -->
</select>

<!-- Select grande -->
<select class="form-select form-select-lg">
    <!-- Opções -->
</select>
```

## Textarea

```html
<div class="mb-3">
    <label class="form-label" for="mensagem">Mensagem</label>
    <textarea class="form-control" id="mensagem" rows="3"
              placeholder="Digite sua mensagem..."></textarea>
</div>
```

### Textarea com Tamanho

```html
<!-- Textarea pequena -->
<textarea class="form-control form-control-sm" rows="2"></textarea>

<!-- Textarea grande -->
<textarea class="form-control form-control-lg" rows="5"></textarea>
```

## Checkbox e Radio

### Checkbox

```html
<div class="form-check">
    <input class="form-check-input" type="checkbox" value="" id="check1">
    <label class="form-check-label" for="check1">
        Aceito os termos de uso
    </label>
</div>

<div class="form-check">
    <input class="form-check-input" type="checkbox" value="" id="check2" checked>
    <label class="form-check-label" for="check2">
        Receber novidades por email
    </label>
</div>
```

### Checkbox Inline

```html
<div class="form-check form-check-inline">
    <input class="form-check-input" type="checkbox" id="inline1">
    <label class="form-check-label" for="inline1">Opção 1</label>
</div>
<div class="form-check form-check-inline">
    <input class="form-check-input" type="checkbox" id="inline2">
    <label class="form-check-label" for="inline2">Opção 2</label>
</div>
```

### Radio

```html
<div class="form-check">
    <input class="form-check-input" type="radio" name="radioGroup" id="radio1">
    <label class="form-check-label" for="radio1">
        Masculino
    </label>
</div>
<div class="form-check">
    <input class="form-check-input" type="radio" name="radioGroup" id="radio2">
    <label class="form-check-label" for="radio2">
        Feminino
    </label>
</div>
<div class="form-check">
    <input class="form-check-input" type="radio" name="radioGroup" id="radio3" checked>
    <label class="form-check-label" for="radio3">
        Outro
    </label>
</div>
```

### Radio Inline

```html
<div class="form-check form-check-inline">
    <input class="form-check-input" type="radio" name="inlineRadio" id="inlineRadio1">
    <label class="form-check-label" for="inlineRadio1">Sim</label>
</div>
<div class="form-check form-check-inline">
    <input class="form-check-input" type="radio" name="inlineRadio" id="inlineRadio2">
    <label class="form-check-label" for="inlineRadio2">Não</label>
</div>
```

### Switch

```html
<div class="form-check form-switch">
    <input class="form-check-input" type="checkbox" id="switch1">
    <label class="form-check-label" for="switch1">
        Receber notificações
    </label>
</div>
```

## Input Group

### Input com Prefixo

```html
<div class="mb-3">
    <label class="form-label" for="username">Nome de Usuário</label>
    <div class="input-group">
        <span class="input-group-text">@</span>
        <input type="text" class="form-control" id="username"
               placeholder="usuario">
    </div>
</div>
```

### Input com Sufixo

```html
<div class="mb-3">
    <label class="form-label" for="website">Website</label>
    <div class="input-group">
        <input type="text" class="form-control" id="website"
               placeholder="meusite">
        <span class="input-group-text">.com</span>
    </div>
</div>
```

### Input com Prefixo e Sufixo

```html
<div class="mb-3">
    <label class="form-label" for="valor">Valor</label>
    <div class="input-group">
        <span class="input-group-text">R$</span>
        <input type="text" class="form-control" id="valor"
               placeholder="0,00">
        <span class="input-group-text">BRL</span>
    </div>
</div>
```

### Input com Botão

```html
<div class="input-group">
    <input type="text" class="form-control" placeholder="Buscar...">
    <button class="btn btn-primary" type="button">
        <i class="align-middle" data-feather="search"></i>
    </button>
</div>
```

### Input com Dropdown

```html
<div class="input-group">
    <button class="btn btn-outline-secondary dropdown-toggle"
            type="button" data-bs-toggle="dropdown">
        Ação
    </button>
    <ul class="dropdown-menu">
        <li><a class="dropdown-item" href="#">Opção 1</a></li>
        <li><a class="dropdown-item" href="#">Opção 2</a></li>
    </ul>
    <input type="text" class="form-control">
</div>
```

## Layouts de Formulário

### Formulário Vertical (Padrão)

```html
<form>
    <div class="mb-3">
        <label class="form-label" for="nome">Nome</label>
        <input type="text" class="form-control" id="nome">
    </div>
    <div class="mb-3">
        <label class="form-label" for="email">Email</label>
        <input type="email" class="form-control" id="email">
    </div>
    <button type="submit" class="btn btn-primary">Enviar</button>
</form>
```

### Formulário Horizontal

```html
<form>
    <div class="row mb-3">
        <label class="col-sm-2 col-form-label" for="nome">Nome</label>
        <div class="col-sm-10">
            <input type="text" class="form-control" id="nome">
        </div>
    </div>
    <div class="row mb-3">
        <label class="col-sm-2 col-form-label" for="email">Email</label>
        <div class="col-sm-10">
            <input type="email" class="form-control" id="email">
        </div>
    </div>
    <div class="row">
        <div class="col-sm-10 offset-sm-2">
            <button type="submit" class="btn btn-primary">Enviar</button>
        </div>
    </div>
</form>
```

### Formulário Inline

```html
<form class="row row-cols-lg-auto g-3 align-items-center">
    <div class="col-12">
        <label class="visually-hidden" for="inlineFormInputGroupUsername">Usuário</label>
        <div class="input-group">
            <div class="input-group-text">@</div>
            <input type="text" class="form-control" id="inlineFormInputGroupUsername"
                   placeholder="Usuário">
        </div>
    </div>
    <div class="col-12">
        <label class="visually-hidden" for="inlineFormSelectPref">Preferência</label>
        <select class="form-select" id="inlineFormSelectPref">
            <option selected>Escolha...</option>
            <option value="1">Um</option>
            <option value="2">Dois</option>
            <option value="3">Três</option>
        </select>
    </div>
    <div class="col-12">
        <div class="form-check">
            <input class="form-check-input" type="checkbox" id="inlineFormCheck">
            <label class="form-check-label" for="inlineFormCheck">
                Lembre de mim
            </label>
        </div>
    </div>
    <div class="col-12">
        <button type="submit" class="btn btn-primary">Enviar</button>
    </div>
</form>
```

## Formulário em Grid

```html
<form>
    <div class="row g-3">
        <div class="col">
            <input type="text" class="form-control" placeholder="Nome">
        </div>
        <div class="col">
            <input type="text" class="form-control" placeholder="Sobrenome">
        </div>
    </div>
    <div class="row g-3 mt-1">
        <div class="col-md-6">
            <label class="form-label" for="cidade">Cidade</label>
            <input type="text" class="form-control" id="cidade">
        </div>
        <div class="col-md-3">
            <label class="form-label" for="estado">Estado</label>
            <select class="form-select" id="estado">
                <option selected>Selecione...</option>
                <option>SP</option>
                <option>RJ</option>
                <option>MG</option>
            </select>
        </div>
        <div class="col-md-3">
            <label class="form-label" for="cep">CEP</label>
            <input type="text" class="form-control" id="cep">
        </div>
    </div>
</form>
```

## Validação

### Validação Visual

```html
<form class="needs-validation" novalidate>
    <div class="mb-3">
        <label class="form-label" for="nome">Nome</label>
        <input type="text" class="form-control" id="nome" required>
        <div class="invalid-feedback">
            Por favor, digite seu nome.
        </div>
    </div>
    <div class="mb-3">
        <label class="form-label" for="email">Email</label>
        <input type="email" class="form-control" id="email" required>
        <div class="invalid-feedback">
            Por favor, digite um email válido.
        </div>
    </div>
    <button class="btn btn-primary" type="submit">Enviar</button>
</form>

<script>
    // Validação do Bootstrap
    (function() {
        'use strict'
        var forms = document.querySelectorAll('.needs-validation')
        Array.prototype.slice.call(forms)
            .forEach(function(form) {
                form.addEventListener('submit', function(event) {
                    if (!form.checkValidity()) {
                        event.preventDefault()
                        event.stopPropagation()
                    }
                    form.classList.add('was-validated')
                }, false)
            })
    })()
</script>
```

### Estilos de Validação

```html
<!-- Válido -->
<div class="mb-3">
    <label class="form-label" for="valido">Input Válido</label>
    <input type="text" class="form-control is-valid" id="valido">
    <div class="valid-feedback">
        Tudo certo!
    </div>
</div>

<!-- Inválido -->
<div class="mb-3">
    <label class="form-label" for="invalido">Input Inválido</label>
    <input type="text" class="form-control is-invalid" id="invalido">
    <div class="invalid-feedback">
        Algo está errado.
    </div>
</div>
```

## Ranges (Sliders)

```html
<div class="mb-3">
    <label class="form-label" for="range">Range</label>
    <input type="range" class="form-range" id="range" min="0" max="100">
</div>

<!-- Range com passos -->
<div class="mb-3">
    <label class="form-label" for="range2">Range com Passos</label>
    <input type="range" class="form-range" min="0" max="5" step="0.5" id="range2">
</div>

<!-- Range desabilitado -->
<div class="mb-3">
    <label class="form-label" for="range3">Range Desabilitado</label>
    <input type="range" class="form-range" id="range3" disabled>
</div>
```

## Upload de Arquivo

```html
<div class="mb-3">
    <label class="form-label" for="arquivo">Upload de Arquivo</label>
    <input class="form-control" type="file" id="arquivo">
</div>

<!-- Múltiplos arquivos -->
<div class="mb-3">
    <label class="form-label" for="arquivos">Múltiplos Arquivos</label>
    <input class="form-control" type="file" id="arquivos" multiple>
</div>
```

## Cores

```html
<div class="mb-3">
    <label class="form-label" for="cor">Selecione uma Cor</label>
    <input type="color" class="form-control form-control-color" id="cor"
           value="#563d7c" title="Escolha sua cor">
</div>
```

## Inputs Readonly e Disabled

```html
<!-- Readonly -->
<div class="mb-3">
    <label class="form-label" for="readonly">Readonly</label>
    <input type="text" class="form-control" id="readonly"
           value="Não pode ser editado" readonly>
</div>

<!-- Disabled -->
<div class="mb-3">
    <label class="form-label" for="disabled">Disabled</label>
    <input type="text" class="form-control" id="disabled"
           value="Desabilitado" disabled>
</div>
```

## Formulário Completo

```html
<div class="card">
    <div class="card-header">
        <h5 class="card-title mb-0">Formulário de Cadastro</h5>
    </div>
    <div class="card-body">
        <form>
            <!-- Dados Pessoais -->
            <h6 class="mb-3">Dados Pessoais</h6>
            <div class="row g-3 mb-4">
                <div class="col-md-6">
                    <label class="form-label" for="nome">Nome Completo</label>
                    <input type="text" class="form-control" id="nome" required>
                </div>
                <div class="col-md-6">
                    <label class="form-label" for="email">Email</label>
                    <input type="email" class="form-control" id="email" required>
                </div>
                <div class="col-md-6">
                    <label class="form-label" for="telefone">Telefone</label>
                    <input type="tel" class="form-control" id="telefone">
                </div>
                <div class="col-md-6">
                    <label class="form-label" for="nascimento">Data de Nascimento</label>
                    <input type="date" class="form-control" id="nascimento">
                </div>
            </div>

            <!-- Endereço -->
            <h6 class="mb-3">Endereço</h6>
            <div class="row g-3 mb-4">
                <div class="col-12">
                    <label class="form-label" for="endereco">Endereço</label>
                    <input type="text" class="form-control" id="endereco">
                </div>
                <div class="col-md-6">
                    <label class="form-label" for="cidade">Cidade</label>
                    <input type="text" class="form-control" id="cidade">
                </div>
                <div class="col-md-3">
                    <label class="form-label" for="estado">Estado</label>
                    <select class="form-select" id="estado">
                        <option selected>Selecione...</option>
                        <option>SP</option>
                        <option>RJ</option>
                        <option>MG</option>
                    </select>
                </div>
                <div class="col-md-3">
                    <label class="form-label" for="cep">CEP</label>
                    <input type="text" class="form-control" id="cep">
                </div>
            </div>

            <!-- Preferências -->
            <h6 class="mb-3">Preferências</h6>
            <div class="mb-3">
                <div class="form-check">
                    <input class="form-check-input" type="checkbox" id="newsletter">
                    <label class="form-check-label" for="newsletter">
                        Receber newsletter
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="checkbox" id="termos" required>
                    <label class="form-check-label" for="termos">
                        Aceito os termos de uso
                    </label>
                </div>
            </div>

            <!-- Botões -->
            <div class="d-flex justify-content-end gap-2">
                <button type="reset" class="btn btn-light">Limpar</button>
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>
        </form>
    </div>
</div>
```

## Classes CSS

### Estrutura
| Classe | Descrição |
|--------|-----------|
| `.form-control` | Input básico |
| `.form-select` | Select dropdown |
| `.form-label` | Label do campo |
| `.form-text` | Texto de ajuda |
| `.form-check` | Checkbox/radio |
| `.form-check-input` | Input de checkbox/radio |
| `.form-check-label` | Label de checkbox/radio |

### Tamanhos
| Classe | Descrição |
|--------|-----------|
| `.form-control-sm` | Input pequeno |
| `.form-control-lg` | Input grande |

### Validação
| Classe | Descrição |
|--------|-----------|
| `.is-valid` | Estado válido |
| `.is-invalid` | Estado inválido |
| `.valid-feedback` | Feedback de sucesso |
| `.invalid-feedback` | Feedback de erro |

## Exemplos Práticos

- `forms-basic-inputs.html` - Inputs básicos
- `forms-layouts.html` - Layouts de formulário
- `forms-input-groups.html` - Grupos de inputs
- `forms-advanced-inputs.html` - Inputs avançados
- `forms-validation.html` - Validação de formulários

## Recursos Adicionais

- [Bootstrap Forms](https://getbootstrap.com/docs/5.3/forms/overview/) - Documentação oficial
- [Flatpickr](https://flatpickr.js.org/) - Datepicker
- [Quill](https://quilljs.com/) - Editor de texto rico
