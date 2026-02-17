# Tradução e Internacionalização (i18n)

Guia completo para traduzir o AdminKit Pro para outros idiomas e implementar internacionalização.

## 🌍 Visão Geral

O AdminKit Pro já inclui suporte básico para múltiplos idiomas com seleção de idioma na navbar. Este guia mostra como:

1. Traduzir textos estáticos
2. Implementar mudança dinâmica de idioma
3. Traduzir datas e números
4. Suportar RTL (Right-to-Left)

## 📝 Traduzir Textos Estáticos

### Método 1: Busca e Substituição

Para projetos simples, use busca e substituição:

```bash
# Encontre textos para traduzir
grep -r "Welcome" *.html
grep -r "Dashboard" *.html
grep -r "Settings" *.html
```

### Método 2: Arquivos de Tradução

Crie arquivos JSON para cada idioma:

#### js/i18n/pt-BR.json

```json
{
  "common": {
    "welcome": "Bem-vindo",
    "dashboard": "Painel de Controle",
    "settings": "Configurações",
    "logout": "Sair",
    "save": "Salvar",
    "cancel": "Cancelar",
    "delete": "Excluir",
    "edit": "Editar",
    "add": "Adicionar",
    "search": "Buscar",
    "loading": "Carregando...",
    "noData": "Nenhum dado disponível"
  },
  "dashboard": {
    "title": "Painel de Controle",
    "sales": "Vendas",
    "visitors": "Visitantes",
    "earnings": "Ganhos",
    "orders": "Pedidos",
    "recentMovement": "Movimento Recente",
    "browserUsage": "Uso de Navegador",
    "realTime": "Tempo Real",
    "calendar": "Calendário",
    "monthlySales": "Vendas Mensais",
    "latestProjects": "Projetos Recentes"
  },
  "sidebar": {
    "dashboards": "Painéis",
    "pages": "Páginas",
    "uiElements": "Elementos UI",
    "forms": "Formulários",
    "tables": "Tabelas",
    "charts": "Gráficos",
    "maps": "Mapas",
    "auth": "Autenticação"
  }
}
```

#### js/i18n/en.json

```json
{
  "common": {
    "welcome": "Welcome",
    "dashboard": "Dashboard",
    "settings": "Settings",
    "logout": "Logout",
    "save": "Save",
    "cancel": "Cancel",
    "delete": "Delete",
    "edit": "Edit",
    "add": "Add",
    "search": "Search",
    "loading": "Loading...",
    "noData": "No data available"
  }
}
```

### Método 3: Atributos data-i18n

```html
<!-- Adicionar atributos de tradução -->
<h1 data-i18n="dashboard.title">Analytics Dashboard</h1>
<span data-i18n="common.welcome">Welcome</span>

<!-- Com parâmetros -->
<span data-i18n="welcomeUser" data-i18n-args='{"name": "João"}'>
  Welcome, João
</span>
```

## 🔧 Implementar Sistema de Tradução

### JavaScript Básico

```javascript
// js/i18n.js
const translations = {
  'pt-BR': {
    'dashboard.title': 'Painel de Controle',
    'common.welcome': 'Bem-vindo'
  },
  'en': {
    'dashboard.title': 'Dashboard',
    'common.welcome': 'Welcome'
  }
};

let currentLanguage = 'pt-BR';

function t(key) {
  return translations[currentLanguage][key] || key;
}

function setLanguage(lang) {
  currentLanguage = lang;
  document.querySelectorAll('[data-i18n]').forEach(el => {
    const key = el.getAttribute('data-i18n');
    el.textContent = t(key);
  });
}

// Salvar preferência
function saveLanguagePreference(lang) {
  localStorage.setItem('language', lang);
}

// Carregar preferência
function loadLanguagePreference() {
  return localStorage.getItem('language') || 'pt-BR';
}
```

### HTML com Seletor de Idioma

```html
<!-- Seletor de idioma na navbar -->
<li class="nav-item dropdown">
  <a class="nav-flag dropdown-toggle" href="#" id="languageDropdown" data-bs-toggle="dropdown">
    <img src="img/flags/br.png" alt="Português" />
  </a>
  <div class="dropdown-menu dropdown-menu-end">
    <a class="dropdown-item" href="#" data-lang="pt-BR">
      <img src="img/flags/br.png" width="20" class="align-middle me-1" />
      <span class="align-middle">Português</span>
    </a>
    <a class="dropdown-item" href="#" data-lang="en">
      <img src="img/flags/us.png" width="20" class="align-middle me-1" />
      <span class="align-middle">English</span>
    </a>
    <a class="dropdown-item" href="#" data-lang="es">
      <img src="img/flags/es.png" width="20" class="align-middle me-1" />
      <span class="align-middle">Español</span>
    </a>
  </div>
</li>
```

### JavaScript para Mudança de Idioma

```javascript
// Event listeners para mudança de idioma
document.querySelectorAll('[data-lang]').forEach(element => {
  element.addEventListener('click', (e) => {
    e.preventDefault();
    const lang = element.getAttribute('data-lang');
    setLanguage(lang);
    saveLanguagePreference(lang);
    location.reload(); // Recarregar para aplicar mudanças
  });
});

// Carregar idioma ao iniciar
document.addEventListener('DOMContentLoaded', () => {
  const savedLang = loadLanguagePreference();
  setLanguage(savedLang);
});
```

## 📅 Traduzir Datas e Números

### Formatação de Datas

```javascript
// Formatar data de acordo com o idioma
function formatDate(date, locale = 'pt-BR') {
  return new Intl.DateTimeFormat(locale, {
    year: 'numeric',
    month: 'long',
    day: 'numeric'
  }).format(date);
}

// Exemplos
formatDate(new Date(), 'pt-BR'); // "17 de fevereiro de 2026"
formatDate(new Date(), 'en-US'); // "February 17, 2026"
formatDate(new Date(), 'es-ES'); // "17 de febrero de 2026"
```

### Formatação de Números

```javascript
// Formatar números
function formatNumber(number, locale = 'pt-BR') {
  return new Intl.NumberFormat(locale).format(number);
}

// Formatar moeda
function formatCurrency(amount, locale = 'pt-BR', currency = 'BRL') {
  return new Intl.NumberFormat(locale, {
    style: 'currency',
    currency: currency
  }).format(amount);
}

// Exemplos
formatNumber(1234567.89, 'pt-BR'); // "1.234.567,89"
formatNumber(1234567.89, 'en-US'); // "1,234,567.89"

formatCurrency(1234.56, 'pt-BR', 'BRL'); // "R$ 1.234,56"
formatCurrency(1234.56, 'en-US', 'USD'); // "$1,234.56"
```

### Formatação de Percentagem

```javascript
function formatPercent(value, locale = 'pt-BR') {
  return new Intl.NumberFormat(locale, {
    style: 'percent',
    minimumFractionDigits: 1
  }).format(value);
}

// Exemplos
formatPercent(0.653, 'pt-BR'); // "65,3%"
formatPercent(0.653, 'en-US'); // "65.3%"
```

## 🔄 RTL (Right-to-Left)

### Suporte para Árabe, Hebraico, etc.

```html
<!-- Adicionar atributo dir -->
<html lang="ar" dir="rtl">
```

### CSS para RTL

```css
/* Sobrescrever direções para RTL */
[dir="rtl"] .sidebar {
  right: 0;
  left: auto;
}

[dir="rtl"] .main {
  margin-right: 250px;
  margin-left: 0;
}

/* Ajustar ícones e setas */
[dir="rtl"] .dropdown-toggle::after {
  transform: rotate(180deg);
}
```

## 🌐 Idiomas Suportados

### Adicionar Novo Idioma

1. **Adicionar bandeira**

```bash
# Salvar bandeira em img/flags/
img/flags/fr.png  # Francês
img/flags/de.png  # Alemão
img/flags/it.png  # Italiano
```

2. **Criar arquivo de tradução**

```javascript
// js/i18n/fr.json
{
  "common": {
    "welcome": "Bienvenue",
    "dashboard": "Tableau de bord"
  }
}
```

3. **Adicionar opção no seletor**

```html
<a class="dropdown-item" href="#" data-lang="fr">
  <img src="img/flags/fr.png" width="20" class="align-middle me-1" />
  <span class="align-middle">Français</span>
</a>
```

### Lista de Idiomas Comuns

| Código | Idioma | Bandeira | RTL |
|--------|--------|----------|-----|
| pt-BR | Português (Brasil) | br.png | Não |
| en | English | us.png | Não |
| es | Español | es.png | Não |
| fr | Français | fr.png | Não |
| de | Deutsch | de.png | Não |
| it | Italiano | it.png | Não |
| ar | العربية | sa.png | Sim |
| he | עברית | il.png | Sim |
| ja | 日本語 | jp.png | Não |
| zh | 中文 | cn.png | Não |

## 🎯 Melhores Práticas

### 1. Separar Textos do Código

```javascript
// ❌ Não recomendado
alert('Bem-vindo ao sistema!');

// ✅ Recomendado
alert(t('common.welcome'));
```

### 2. Usar Chaves Descritivas

```javascript
// ❌ Não recomendado
'text1': 'Bem-vindo'
'text2': 'Configurações'

// ✅ Recomendado
'common.welcome': 'Bem-vindo'
'settings.title': 'Configurações'
```

### 3. Manter Contexto

```json
{
  "button.save": "Salvar",
  "action.save": "Salvar",
  "message.saved": "Salvo com sucesso"
}
```

### 4. Pluralização

```javascript
function pluralize(key, count) {
  const keyPlural = count === 1 ? key : key + '_plural';
  return t(keyPlural).replace('{count}', count);
}

// No JSON
{
  "item": "{count} item",
  "item_plural": "{count} itens"
}
```

## 📚 Bibliotecas de i18n

### i18next (Recomendado)

```javascript
// Instalar
// npm install i18next

// Configurar
import i18next from 'i18next';

i18next.init({
  lng: 'pt-BR',
  resources: {
    'pt-BR': {
      translation: require('./i18n/pt-BR.json')
    },
    'en': {
      translation: require('./i18n/en.json')
    }
  }
});

// Usar
i18next.t('common.welcome');
```

### Polyglot (Alternativa)

```javascript
// Instalar
// npm install node-polyglot

// Configurar
import Polyglot from 'node-polyglot';

const polyglot = new Polyglot({
  phrases: {
    'welcome': 'Bem-vindo',
    'dashboard': 'Painel de Controle'
  }
});

// Usar
polyglot.t('welcome');
```

## ✅ Checklist de Internacionalização

- [ ] Textos estáticos traduzidos
- [ ] Sistema de tradução implementado
- [ ] Datas formatadas corretamente
- [ ] Números e moedas formatados
- [ ] Seletor de idioma funcionando
- [ ] Preferências salvas em localStorage
- [ ] Bandeiras adicionadas
- [ ] RTL suportado (se necessário)
- [ ] Testado em múltiplos idiomas

## 🔗 Recursos

- [MDN - Intl API](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Intl)
- [i18next Documentation](https://www.i18next.com/)
- [Unicode CLDR](http://cldr.unicode.org/)

---

**Versão:** 1.0.0
**Última atualização:** 2026-02-17
