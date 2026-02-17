# Contribuindo com o AdminKit Pro

Obrigado por considerar contribuir com o AdminKit Pro! Este documento fornece diretrizes e instruções sobre como contribuir com o projeto.

## Índice

- [Código de Conduta](#código-de-conduta)
- [Como Posso Contribuir?](#como-posso-contribuir)
- [Processo de Contribuição](#processo-de-contribuição)
- [Padrões de Código](#padrões-de-código)
- [Convenções de Commit](#convenções-de-commit)
- [Documentação](#documentação)
- [Reportando Bugs](#reportando-bugs)
- [Sugerindo Funcionalidades](#sugerindo-funcionalidades)

---

## Código de Conduta

Ao participar deste projeto, você concorda em manter um ambiente inclusivo e respeitoso. Por favor, leia nosso [Código de Conduta](CODE_OF_CONDUCT.md) antes de contribuir.

---

## Como Posso Contribuir?

### Reportando Bugs

Se você encontrar um bug, por favor:

1. Verifique se o bug já foi reportado nas [issues existentes](../../issues)
2. Se não encontrado, crie uma nova issue usando o template de bug report
3. Forneça o máximo de informações possível para reproduzir o bug

### Sugerindo Funcionalidades

Tem uma ideia para melhorar o AdminKit Pro?

1. Verifique as [issues existentes](../../issues) para evitar duplicatas
2. Use o template de feature request
3. Explique claramente o uso case e os benefícios

### Enviando Pull Requests

Contribuições via pull requests são bem-vindas! Antes de enviar:

1. Leia e siga este guia
2. Escolha uma issue para trabalhar (ou crie uma se necessário)
3. Faça um fork do repositório
4. Crie uma branch para sua alteração
5. Faça suas mudanças seguindo os padrões do projeto
6. Teste suas mudanças
7. Envie o pull request

---

## Processo de Contribuição

### 1. Preparação

#### Fork e Clone

```bash
# Faça um fork do repositório
# Clone seu fork
git clone https://github.com/SEU-USUARIO/adminkit-pro.git
cd adminkit-pro

# Adicione o repositório upstream
git remote add upstream https://github.com/usuario-original/adminkit-pro.git
```

#### Sincronize com Upstream

Antes de começar a trabalhar, certifique-se de que seu fork está atualizado:

```bash
git fetch upstream
git checkout main
git merge upstream/main
```

### 2. Crie uma Branch

Crie uma branch para sua contribuição:

```bash
git checkout -b feature/minha-nova-funcionalidade
# ou
git checkout -b fix/correcao-do-bug
# ou
git checkout -b docs/atualizacao-documentacao
```

Use prefixos descritivos:
- `feature/` - novas funcionalidades
- `fix/` - correções de bugs
- `docs/` - alterações na documentação
- `style/` - formatação, ponto e vírgula, etc.
- `refactor/` - refatoração de código
- `test/` - adição ou atualização de testes
- `chore/` - tarefas de manutenção

### 3. Faça Suas Mudanças

#### Padrões de Código

**HTML:**
- Use indentação de 2 espaços
- Mantenha o HTML semântico
- Use comentários para seções complexas
- Valide seu HTML

```html
<!-- Bom -->
<div class="card">
  <div class="card-body">
    <h5 class="card-title">Título</h5>
  </div>
</div>

<!-- Evite -->
<div class='card'><div class='card-body'><h5 class='card-title'>Título</h5></div></div>
```

**CSS:**
- Use classes BEM quando apropriado
- Mantenha seletores específicos, mas não excessivos
- Use variáveis CSS para valores repetidos
- Comente regras complexas

```css
/* Bom */
.card {
  --card-padding: 1.5rem;
  padding: var(--card-padding);
}

.card__title {
  font-size: 1.25rem;
}

/* Evite */
div div .card h5 {
  font-size: 20px;
}
```

**JavaScript:**
- Use `const` e `let`, evite `var`
- Use arrow functions para callbacks
- Mantenha funções pequenas e focadas
- Adicione JSDoc para funções complexas

```javascript
// Bom
const calculateTotal = (items) => {
  return items.reduce((sum, item) => sum + item.price, 0);
};

// Evite
function calculateTotal(items) {
  var sum = 0;
  for (var i = 0; i < items.length; i++) {
    sum = sum + items[i].price;
  }
  return sum;
}
```

### 4. Teste Suas Mudanças

Antes de enviar um PR:

1. **Teste em múltiplos navegadores**
   - Chrome (última versão)
   - Firefox (última versão)
   - Safari (última versão)
   - Edge (última versão)

2. **Teste responsividade**
   - Desktop (1920x1080)
   - Tablet (768x1024)
   - Mobile (375x667)

3. **Teste temas**
   - Tema claro
   - Tema escuro
   - Tema colorido

4. **Valide código**
   ```bash
   # Valide HTML
   npx html-validate *.html

   # Verifique CSS
   npx stylelint "css/**/*.css"

   # Verifique JavaScript
   npx eslint js/**/*.js
   ```

### 5. Commit Suas Mudanças

Use mensagens de commit claras e descritivas (veja [Convenções de Commit](#convenções-de-commit)):

```bash
git add .
git commit -m "feat: adiciona novo componente de carousel"
```

### 6. Push e Pull Request

```bash
# Push para sua branch
git push origin feature/minha-nova-funcionalidade
```

Então, crie um Pull Request no GitHub:

1. Vá para a página do repositório
2. Clique em "Pull Requests"
3. Clique em "New Pull Request"
4. Selecione sua branch
5. Preencha o template de PR
6. Clique em "Create Pull Request"

---

## Convenções de Commit

Usamos o padrão [Conventional Commits](https://www.conventionalcommits.org/):

```
<tipo>(<escopo>): <descrição>

[corpo opcional]

[rodapé opcional]
```

### Tipos de Commit

- `feat`: Nova funcionalidade
- `fix`: Correção de bug
- `docs`: Alterações na documentação
- `style`: Formatação, missing semi colons, etc.
- `refactor`: Refatoração de código
- `test`: Adição ou atualização de testes
- `chore`: Atualização de tarefas, configs, etc.
- `perf`: Melhoria de performance
- `ci`: Alterações em CI/CD

### Exemplos

```bash
feat(componentes): adiciona componente de modal customizado
fix(formularios): corrige validação de email
docs(instalacao): atualiza instruções de setup
style(css): padroniza espaçamento em variaveis
refactor(graficos): otimiza renderizacao do ApexCharts
test(botoes): adiciona testes de clique
chore(deps): atualiza Bootstrap para v5.3.2
perf(tabelas): melhora performance do DataTables
ci(github): configura actions para deploy
```

---

## Documentação

### Atualizando a Documentação

Se sua alteração afeta a funcionalidade do projeto:

1. Atualize os arquivos de documentação relevantes em `docs/`
2. Use português brasileiro claro e conciso
3. Inclua exemplos de código quando aplicável
4. Mantenha a estrutura consistente

### Estrutura de Documentação

```
docs/
├── componentes/        # Documentação de componentes
├── exemplos/           # Exemplos de uso
├── guia-de-inicio/     # Guias de introdução
└── personalizacao/     # Guias de personalização
```

### Formatação

Use Markdown padrão do GitHub:

```markdown
# Título Principal

## Seção Secundária

### Subseção

- Item 1
- Item 2

```javascript
// Código com syntax highlighting
const exemplo = "valor";
```

> Notas importantes

[Links](docs/README.md)
```

---

## Reportando Bugs

### Antes de Reportar

1. **Pesquise issues existentes** - Verifique se o bug já foi reportado
2. **Verifique a versão** - Certifique-se de estar usando a versão mais recente
3. **Teste em ambientes diferentes** - Browser, dispositivo, etc.

### Template de Bug Report

Use este template ao criar uma issue de bug:

```markdown
## Descrição do Bug
Descrição breve e clara do problema

## Passos para Reproduzir
1. Vá para '...'
2. Clique em '....'
3. Role até '....'
4. Veja o erro

## Comportamento Esperado
Descrição do que você esperava acontecer

## Capturas de Tela
Se aplicável, adicione capturas de tela

## Ambiente
- Sistema Operacional: [ex. Windows 11, macOS Ventura]
- Browser: [ex. Chrome 120, Firefox 121]
- Versão do AdminKit: [ex. 1.0.0]
- Resolução: [ex. 1920x1080]

## Contexto Adicional
Informações adicionais, logs, etc.
```

---

## Sugerindo Funcionalidades

### Antes de Sugerir

1. **Verifique issues existentes** - Evite duplicatas
2. **Pense no uso case** - Qual problema isso resolve?
3. **Considere o escopo** - É uma mudança pequena ou grande?

### Template de Feature Request

Use este template ao sugerir uma funcionalidade:

```markdown
## Descrição da Funcionalidade
Descrição clara e concisa da funcionalidade proposta

## Problema ou Uso Case
Qual problema essa funcionalidade resolveria?
Qual o uso case específico?

## Solução Proposta
Descreva sua solução em detalhes

## Alternativas Consideradas
Descreva soluções alternativas que você considerou

## Contexto Adicional
Informações adicionais, exemplos, mockups, etc.
```

---

## Review de Pull Request

### O que esperar

- Seu PR será revisado por mantenedores do projeto
- Feedback será fornecido de forma construtiva
- Mudanças podem ser solicitadas

### Como responder ao feedback

1. **Responda a cada comentário** - Confirme que você entendeu
2. **Faça as mudanças solicitadas** - Push commits adicionais
3. **Seja respeitoso** - Mesmo em discordância

### Aprovação e Merge

Após aprovação:

- O mantenedor fará o merge na branch principal
- O PR será fechado automaticamente
- Você será notificado

---

## Obtendo Ajuda

Se você precisar de ajuda:

1. **Leia a documentação** - [docs/README.md](docs/README.md)
2. **Pesquise issues** - Verifique se alguém teve o mesmo problema
3. **Abra uma issue** - Use o template apropriado
4. **GitHub Discussions** - Para conversas mais gerais

---

## Reconhecimento

Contribuidores serão listados no arquivo [CONTRIBUTORS.md](CONTRIBUTORS.md) (se existir) ou mencionados nos release notes.

Obrigado por contribuir com o AdminKit Pro! 🎉

---

## Licença

Ao contribuir, você concorda que suas contribuições serão licenciadas sob a [Licença MIT](LICENSE).
