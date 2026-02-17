# Plano de Reorganização - AdminKitPro

**Data:** 2026-02-17
**Status:** Draft
**Versão:** 1.0

---

## 📊 Resumo Executivo

Reorganizar o repositório AdminKitPro para seguir melhores práticas de estrutura de projetos web, movendo arquivos da raiz para diretórios organizados por funcionalidade.

---

## 🎯 Objetivo

Transformar a estrutura atual (com 45+ arquivos HTML na raiz) em uma organização profissional e escalável.

---

## 📁 Estrutura Proposta

### Antes (Atual)
```
AdminKitPro/
├── index.html
├── dashboard-ecommerce.html
├── dashboard-crypto.html
├── pages-settings.html
├── pages-profile.html
├── [... 40+ arquivos HTML na raiz]
├── css/
├── js/
├── img/
├── fonts/
└── docs/
```

### Depois (Proposta)
```
AdminKitPro/
├── index.html (redirect ou landing)
├── src/
│   ├── pages/
│   │   ├── dashboards/
│   │   │   ├── analytics.html (index.html)
│   │   │   ├── ecommerce.html
│   │   │   └── crypto.html
│   │   ├── auth/
│   │   │   ├── sign-in.html
│   │   │   ├── sign-up.html
│   │   │   └── reset-password.html
│   │   ├── app/
│   │   │   ├── settings.html
│   │   │   ├── profile.html
│   │   │   ├── projects.html
│   │   │   ├── clients.html
│   │   │   ├── orders.html
│   │   │   ├── tasks.html
│   │   │   ├── chat.html
│   │   │   ├── pricing.html
│   │   │   └── invoice.html
│   │   ├── errors/
│   │   │   ├── 404.html
│   │   │   └── 500.html
│   │   └── misc/
│   │       └── blank.html
│   └── ui/
│       ├── components/
│       │   ├── cards.html
│       │   ├── buttons.html
│       │   ├── modals.html
│       │   ├── tabs.html
│       │   ├── alerts.html
│       │   ├── typography.html
│       │   ├── grid.html
│       │   ├── offcanvas.html
│       │   ├── placeholders.html
│       │   └── general.html
│       ├── forms/
│       │   ├── basic-inputs.html
│       │   ├── advanced-inputs.html
│       │   ├── input-groups.html
│       │   ├── layouts.html
│       │   ├── validation.html
│       │   └── editors.html
│       ├── tables/
│       │   ├── bootstrap.html
│       │   ├── datatables-base.html
│       │   ├── datatables-ajax.html
│       │   ├── datatables-buttons.html
│       │   ├── datatables-fixed-header.html
│       │   ├── datatables-column-search.html
│       │   ├── datatables-multi.html
│       │   └── datatables-responsive.html
│       ├── charts/
│       │   ├── apexcharts.html
│       │   └── chartjs.html
│       ├── icons/
│       │   ├── feather.html
│       │   └── font-awesome.html
│       ├── maps/
│       │   ├── google.html
│       │   └── vector.html
│       └── notifications/
│           └── index.html
├── public/
│   ├── css/
│   │   ├── light.css
│   │   └── dark.css
│   ├── js/
│   │   ├── app.js
│   │   ├── settings.js
│   │   ├── datatables.js
│   │   └── fullcalendar.js
│   ├── fonts/
│   ├── img/
│   └── favicon.ico
├── docs/
│   ├── README.md
│   ├── guia-de-inicio/
│   ├── componentes/
│   ├── personalizacao/
│   └── exemplos/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
└── .github/
```

---

## 🔄 Plano de Migração

### Fase 1: Preparação
1. Criar estrutura de diretórios
2. Backup do estado atual (branch `backup-before-reorg`)

### Fase 2: Movimentação de Arquivos
3. Mover arquivos HTML para `src/pages/` e `src/ui/`
4. Mover CSS/JS/fonts/img para `public/`

### Fase 3: Atualização de Links
5. Atualizar links relativos em todos os arquivos HTML
6. Atualizar referências na documentação
7. Criar `index.html` na raiz (redirect ou página de boas-vindas)

### Fase 4: Validação
8. Testar todos os links internos
9. Verificar funcionamento da demo
10. Commit e push

---

## 📝 Tarefas Detalhadas

### 1. Criar Branch de Backup
```bash
git checkout -b backup-before-reorg
git push origin backup-before-reorg
git checkout main
```

### 2. Criar Estrutura de Diretórios
```bash
mkdir -p src/pages/{dashboards,auth,app,errors,misc}
mkdir -p src/ui/{components,forms,tables,charts,icons,maps,notifications}
mkdir -p public/{css,js,fonts,img}
```

### 3. Mover Arquivos - Dashboards
```bash
mv index.html src/pages/dashboards/analytics.html
mv dashboard-ecommerce.html src/pages/dashboards/ecommerce.html
mv dashboard-crypto.html src/pages/dashboards/crypto.html
```

### 4. Mover Arquivos - Autenticação
```bash
mv pages-sign-in.html src/pages/auth/sign-in.html
mv pages-sign-up.html src/pages/auth/sign-up.html
mv pages-reset-password.html src/pages/auth/reset-password.html
```

### 5. Mover Arquivos - App Pages
```bash
mv pages-settings.html src/pages/app/settings.html
mv pages-profile.html src/pages/app/profile.html
mv pages-projects.html src/pages/app/projects.html
mv pages-clients.html src/pages/app/clients.html
mv pages-orders.html src/pages/app/orders.html
mv pages-tasks.html src/pages/app/tasks.html
mv pages-chat.html src/pages/app/chat.html
mv pages-pricing.html src/pages/app/pricing.html
mv pages-invoice.html src/pages/app/invoice.html
```

### 6. Mover Arquivos - Errors
```bash
mv pages-404.html src/pages/errors/404.html
mv pages-500.html src/pages/errors/500.html
```

### 7. Mover Arquivos - UI Components
```bash
mv ui-cards.html src/ui/components/cards.html
mv ui-buttons.html src/ui/components/buttons.html
mv ui-modals.html src/ui/components/modals.html
mv ui-tabs.html src/ui/components/tabs.html
mv ui-alerts.html src/ui/components/alerts.html
mv ui-typography.html src/ui/components/typography.html
mv ui-grid.html src/ui/components/grid.html
mv ui-offcanvas.html src/ui/components/offcanvas.html
mv ui-placeholders.html src/ui/components/placeholders.html
mv ui-general.html src/ui/components/general.html
```

### 8. Mover Arquivos - Forms
```bash
mv forms-basic-inputs.html src/ui/forms/basic-inputs.html
mv forms-advanced-inputs.html src/ui/forms/advanced-inputs.html
mv forms-input-groups.html src/ui/forms/input-groups.html
mv forms-layouts.html src/ui/forms/layouts.html
mv forms-validation.html src/ui/forms/validation.html
mv forms-editors.html src/ui/forms/editors.html
```

### 9. Mover Arquivos - Tables
```bash
mv tables-bootstrap.html src/ui/tables/bootstrap.html
mv tables-datatables-ajax.html src/ui/tables/datatables-ajax.html
mv tables-datatables-buttons.html src/ui/tables/datatables-buttons.html
mv tables-datatables-fixed-header.html src/ui/tables/datatables-fixed-header.html
mv tables-datatables-column-search.html src/ui/tables/datatables-column-search.html
mv tables-datatables-multi.html src/ui/tables/datatables-multi.html
mv tables-datatables-responsive.html src/ui/tables/datatables-responsive.html
```

### 10. Mover Arquivos - Outros UI
```bash
mv charts-apexcharts.html src/ui/charts/apexcharts.html
mv charts-chartjs.html src/ui/charts/chartjs.html
mv icons-feather.html src/ui/icons/feather.html
mv icons-font-awesome.html src/ui/icons/font-awesome.html
mv maps-google.html src/ui/maps/google.html
mv maps-vector.html src/ui/maps/vector.html
mv notifications.html src/ui/notifications/index.html
mv calendar.html src/ui/app/calendar.html
```

### 11. Mover Assets para public/
```bash
mv css/* public/css/
mv js/* public/js/
mv fonts/* public/fonts/
mv img/* public/img/
mv index-ptbr.html src/pages/dashboards/index-ptbr.html
```

### 12. Atualizar Links em Todos os Arquivos HTML

**Padrões de substituição:**
- `href="index.html"` → `href="../pages/dashboards/analytics.html"`
- `href="pages-xxx.html"` → `href="../pages/app/xxx.html"`
- `href="ui-xxx.html"` → `href="../ui/components/xxx.html"`
- `href="forms-xxx.html"` → `href="../ui/forms/xxx.html"`
- `href="tables-xxx.html"` → `href="../ui/tables/xxx.html"`
- `href="css/xxx.css"` → `href="../public/css/xxx.css"`
- `href="js/xxx.js"` → `href="../public/js/xxx.js"`
- `src="img/xxx"` → `src="../public/img/xxx"`
- `src="fonts/xxx"` → `src="../public/fonts/xxx"`

### 13. Criar index.html na Raiz

Opção A - Redirect automático:
```html
<!DOCTYPE html>
<html>
<head>
    <meta http-equiv="refresh" content="0; url=src/pages/dashboards/analytics.html">
</head>
<body>
    <p>Redirecionando para <a href="src/pages/dashboards/analytics.html">Dashboard</a>...</p>
</body>
</html>
```

Opção B - Página de boas-vindas com links para todas as seções.

### 14. Atualizar Documentação

Atualizar referências em:
- `docs/guia-de-inicio/estrutura.md`
- `docs/componentes/*.md`
- `README.md`

---

## ⚠️ Considerações Importantes

1. **Links Relativos:** Todos os links precisarão ser ajustados para considerar a nova profundidade de diretórios
2. **Compatibilidade:** O template não usa build process, então caminhos devem funcionar diretamente no navegador
3. **Deploy:** Se hospedado diretamente (GitHub Pages, Netlify drop), verificar configuração de diretório base

---

## ✅ Critérios de Sucesso

- [ ] Todos os arquivos HTML movidos para estrutura organizada
- [ ] Links internos funcionando corretamente
- [ ] Assets acessíveis de todas as páginas
- [ ] Documentação atualizada
- [ ] Nenhum arquivo HTML permanece na raiz (exceto index.html)
- [ ] Commit com migração completo

---

## 📦 Deliverables

1. Repositório reorganizado
2. Branch de backup criado
3. Documentação atualizada
4. Guia de migração para usuários existentes

---

**Aprovado:** ___
**Data de Execução:** ___
