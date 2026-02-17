# Plano de Deploy - GitHub Pages para AdminKitPro

**Status:** RASCUNHO - Aguardando decisão sobre estratégia

**Data:** 2026-02-17

---

## Contexto

**Repositório:** https://github.com/prof-ramos/AdminKitPro

**Estrutura Atual:**
```
AdminKitPro/
├── css/              # Estilos (deve mover para public/)
├── js/               # Scripts (deve mover para public/)
├── fonts/            # Fontes (deve mover para public/)
├── img/              # Imagens (deve mover para public/)
├── public/           # Assets (css, js, fonts, img)
├── src/
│   ├── pages/        # Páginas HTML (51 arquivos)
│   │   ├── app/      # Profile, tasks, invoice, etc.
│   │   ├── auth/     # Login, register, etc.
│   │   ├── dashboards/  # Analytics, sales, etc.
│   │   ├── errors/   # 404, 500, etc.
│   │   └── misc/     # Blank page, etc.
│   └── ui/           # Componentes UI
│       ├── app/
│       ├── charts/
│       ├── components/
│       ├── forms/
│       ├── icons/
│       ├── maps/
│       ├── notifications/
│       └── tables/
├── docs/             # Documentação em Markdown (pt-BR)
│   ├── componentes/
│   ├── exemplos/
│   ├── guia-de-inicio/
│   └── personalizacao/
└── index.html        # Página principal (redirect)
```

**Padrão de Links Atual:**
- CSS/JS: `../../public/css/light.css`
- Imagens: `img/icons/icon-48x48.png`
- Navegação: `../app/profile.html`

---

## Decisão Pendente: Estratégia de Deploy

**AGUARDANDO ESCOLHA DO USUÁRIO:**

**Opção A: GitHub Actions Automático**
- Trigger: Push na branch main
- Deploy automático a cada commit
- Ideal para desenvolvimento ativo

**Opção B: Script Manual (gh-pages branch)**
- Deploy manual via script
- Controle total de quando publicar
- Requer execução manual

**Opção C: Hybrid (Recomendado)**
- GitHub Actions com trigger manual
- `workflow_dispatch` para controle
- CI/CD pronto + controle de publicação

---

## Análise Técnica (Preparação)

### 1. Estrutura para GitHub Pages

**Requisitos:**
- GitHub Pages serve arquivos estáticos de `/` (root) ou `/docs`
- HTMLs precisam estar acessíveis diretamente
- Links relativos devem funcionar
- Documentação markdown precisa ser convertida ou servida

**Abordagem Recomendada: Deploy em `/` (root)**

```
Estrutura no gh-pages ou após build:
├── index.html                    # Página principal
├── pages/                        # Páginas HTML
│   ├── app/
│   ├── auth/
│   ├── dashboards/
│   ├── errors/
│   └── misc/
├── ui/                           # Componentes UI
│   ├── app/
│   ├── charts/
│   ├── components/
│   ├── forms/
│   ├── icons/
│   ├── maps/
│   ├── notifications/
│   └── tables/
├── docs/                         # Documentação (convertida para HTML ou raw)
│   ├── componentes/
│   ├── exemplos/
│   ├── guia-de-inicio/
│   └── personalizacao/
├── css/                          # Estilos
├── js/                           # Scripts
├── fonts/                        # Fontes
├── img/                          # Imagens
└── assets/                       # Se necessário reorganizar
```

### 2. Problemas Identificados

**Links Relativos:**
- Atual: `../../public/css/light.css`
- Problema: Não existe `public/` na raiz do deploy
- Solução: Atualizar para `./css/light.css` ou `/css/light.css`

**Documentação Markdown:**
- GitHub Pages NÃO serve markdown nativamente
- Opções:
  1. Usar Jekyll/Hugo para converter MD → HTML
  2. Deixar MD raw (GitHub mostra visualmente)
  3. Converter para HTML estático

### 3. Assets Orphanados

**Diretórios na raiz que devem estar em public/ ou integrar:**
- `css/`, `js/`, `fonts/`, `img/` parecem duplicados com `public/`

---

## Próximos Passos (Após Decisão)

### Fase 1: Preparação
1. Auditoria de links relativos em todos HTMLs
2. Unificar estrutura de assets (css, js, fonts, img)
3. Decidir formato da documentação (MD vs HTML)

### Fase 2: Implementação (Depende da Opção Escolhida)

**Se Opção A (GitHub Actions Automático):**
- Criar `.github/workflows/deploy.yml`
- Configurar build/deploy automático
- Ativar GitHub Pages no repo

**Se Opção B (Script Manual):**
- Criar script `deploy.sh` ou `scripts/deploy.js`
- Configurar npm script se necessário
- Instruir uso manual

**Se Opção C (Hybrid):**
- Criar workflow com `workflow_dispatch`
- Permitir deploy manual via GitHub UI
- Melhor controle + automação

### Fase 3: Validação
1. Testar links relativos após deploy
2. Validar documentação acessível
3. Testar exemplos funcionando
4. Verificar responsividade

---

## Critérios de Sucesso

- [ ] Página principal (index.html) acessível em `https://prof-ramos.github.io/AdminKitPro/`
- [ ] Todos os exemplos em `src/` funcionando
- [ ] Documentação em `/docs` acessível e legível
- [ ] Links relativos preservados e funcionando
- [ ] Assets (CSS, JS, fonts, img) carregando corretamente
- [ ] Deploy automatizado (ou processo manual claro)

---

## Riscos e Mitigações

| Risco | Impacto | Mitigação |
|-------|---------|-----------|
| Links quebrados após reestruturação | Alto | Auditoria completa + testes |
| Documentação markdown não renderiza | Médio | Usar Jekyll ou converter para HTML |
| Assets não carregam | Alto | Mapear todos os caminhos |
| GitHub Pages limites | Baixo | Projeto estático, sem issues |

---

## Perguntas para o Usuário

1. **Qual estratégia de deploy?** (A, B, ou C)
2. **Documentação deve ser convertida para HTML ou pode ficar MD?**
3. **Manter estrutura atual `src/` ou achatá-la para root?**
4. **Precisa de ambiente de staging?**

---

**Status:** AGUARDANDO RESPOSTAS DO USUÁRIO PARA CONTINUAR

**Próxima Ação:** Responder às perguntas acima para detalhar implementação
