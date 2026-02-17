# Estrutura de Arquivos do AdminKit

Compreender a estrutura de arquivos do AdminKit é essencial para personalizar e manter seu projeto. Este guia detalha a organização completa do template.

## Estrutura Principal (Reorganizada - v2.0)

```
AdminKitPro/
├── index.html              # Página inicial (redirect para dashboard)
├── src/                    # Código fonte das páginas
│   ├── pages/             # Páginas do aplicativo
│   │   ├── dashboards/    # Dashboards (analytics, ecommerce, crypto)
│   │   ├── auth/          # Autenticação (sign-in, sign-up, reset-password)
│   │   ├── app/           # Páginas do app (settings, profile, projects, etc.)
│   │   ├── errors/        # Páginas de erro (404, 500)
│   │   └── misc/          # Páginas diversas (blank)
│   └── ui/                # Componentes e exemplos UI
│       ├── components/    # Componentes UI (cards, buttons, modals, etc.)
│       ├── forms/         # Formulários (inputs, validação, editores)
│       ├── tables/        # Tabelas (bootstrap, datatables)
│       ├── charts/        # Gráficos (apexcharts, chartjs)
│       ├── icons/         # Ícones (feather, font-awesome)
│       ├── maps/          # Mapas (google, vector)
│       ├── notifications/ # Notificações
│       └── app/           # Aplicações (calendar)
├── public/                # Assets públicos
│   ├── css/              # Estilos CSS
│   │   ├── light.css     # Tema claro (principal)
│   │   └── dark.css      # Tema escuro
│   ├── js/               # Scripts JavaScript
│   │   ├── app.js        # Aplicação principal
│   │   ├── settings.js   # Configurações
│   │   ├── datatables.js # DataTables
│   │   └── fullcalendar.js # FullCalendar
│   ├── fonts/            # Fontes Font Awesome
│   └── img/              # Imagens e ícones
│       ├── icons/        # Ícones SVG
│       ├── avatars/      # Avatares de exemplo
│       ├── photos/       # Fotos de exemplo
│       └── flags/        # Bandeiras
├── docs/                  # Documentação em pt-br
│   ├── guia-de-inicio/   # Guias de início
│   ├── componentes/      # Documentação de componentes
│   ├── exemplos/         # Exemplos de uso
│   └── personalizacao/   # Guias de personalização
├── README.md             # Documentação principal
├── LICENSE               # Licença MIT
├── CONTRIBUTING.md       # Guia de contribuição
└── CODE_OF_CONDUCT.md    # Código de conduta
```

## Arquivos CSS

### `public/css/light.css`
Arquivo CSS principal com o tema claro. Contém:
- Variáveis CSS para cores, fontes e espaçamentos
- Estilos de componentes Bootstrap customizados
- Estilos específicos do AdminKit
- Responsividade para diferentes dispositivos

### `public/css/dark.css`
Arquivo CSS com o tema escuro. Sobrescreve as variáveis de cores do tema claro para criar a aparência dark mode.

## Caminhos Relativos

Com a nova estrutura, os arquivos HTML em `src/` referenciam os assets usando caminhos relativos:

- CSS/JS: `../../public/css/` e `../../public/js/`
- Imagens: `../../public/img/`
- Fontes: carregadas automaticamente pelo navegador

## Arquivos JavaScript

### `public/js/app.js`
Script principal da aplicação. Contém:
- Inicialização de componentes
- Configuração de gráficos
- Lógica de interação da interface
- Manipulação de eventos

### `js/settings.js`
Gerencia as configurações do template:
- Troca de temas (light/dark/colored)
- Layout (fluid/boxed)
- Posição da sidebar (left/right)
- Layout da sidebar (default/compact)
- Persistência via localStorage

## Arquivos de Imagens

### `img/icons/`
Contém ícones SVG usados no template:
- Brand icons (logos de empresas)
- UI icons (ícones de interface)

### `img/avatars/`
Avatares de exemplo para:
- Perfil de usuário
- Comentários
- Menções em mensagens

### `img/photos/`
Fotos de exemplo usadas em:
- Cards de projetos
- Galerias
- Demonstração de layout

### `img/flags/`
Bandeiras de países para o seletor de idioma:
- us.png (Inglês)
- es.png (Espanhol)
- ru.png (Russo)
- de.png (Alemão)
- br.png (Português - pode ser adicionado)

## Páginas HTML Principais

### Páginas de Dashboard
- `index.html` - Dashboard Analytics (página principal)
- `dashboard-ecommerce.html` - Dashboard E-Commerce
- `dashboard-crypto.html` - Dashboard Crypto

### Páginas de Interface
- `ui-buttons.html` - Botões
- `ui-cards.html` - Cards
- `ui-modals.html` - Modais
- `ui-typography.html` - Tipografia
- `ui-alerts.html` - Alertas
- `ui-tabs.html` - Abas

### Páginas de Formulários
- `forms-basic-inputs.html` - Inputs básicos
- `forms-advanced-inputs.html` - Inputs avançados
- `forms-editors.html` - Editores de texto
- `forms-validation.html` - Validação de formulários

### Páginas de Tabelas
- `tables-bootstrap.html` - Tabelas Bootstrap
- `tables-datatables-responsive.html` - DataTables responsivas
- `tables-datatables-buttons.html` - DataTables com botões
- `tables-datatables-fixed-header.html` - DataTables com cabeçalho fixo

### Páginas de Gráficos
- `charts-chartjs.html` - Gráficos Chart.js
- `charts-apexcharts.html` - Gráficos ApexCharts

### Páginas de Autenticação
- `pages-sign-in.html` - Login
- `pages-sign-up.html` - Cadastro
- `pages-reset-password.html` - Recuperação de senha
- `pages-404.html` - Página não encontrada
- `pages-500.html` - Erro do servidor

### Outras Páginas
- `pages-profile.html` - Perfil de usuário
- `pages-settings.html` - Configurações
- `pages-blank.html` - Página em branco
- `calendar.html` - Calendário
- `icons-feather.html` - Ícones Feather

## Como Organizar Seu Projeto

### Para Projetos Pequenos
Mantenha a estrutura original do AdminKit. Edite os arquivos diretamente nas pastas existentes.

### Para Projetos Médios/Grandes
Considere separar seu código do template:

```
seu-projeto/
├── assets/
│   ├── css/           # Seus CSS customizados
│   ├── js/            # Seus JavaScript customizados
│   └── img/           # Suas imagens
├── adminkit/          # Template AdminKit (não editado)
├── templates/         # Seus templates HTML
└── index.html
```

### Para Integração com Backend
A estrutura depende da sua tecnologia:

#### PHP
```
public/
├── css/
├── js/
├── img/
├── templates/         # Arquivos .html ou .php
└── index.php
```

#### Node.js/Express
```
public/
├── css/
├── js/
├── img/
└── index.html
views/                  # Templates se usando engine de templates
└── layouts/
```

## Arquivos que Você Pode Editar com Segurança

### Editar Livremente
- `index.html` e outras páginas HTML
- `js/app.js` (para adicionar sua lógica)
- CSS customizado (crie seu próprio arquivo)
- Imagens em `img/`

### Editar com Cuidado
- `js/settings.js` (lógica de temas)
- CSS principal (pode afetar todo o sistema)

### Não Editar (a menos que necessário)
- `js/datatables.js` (plugin de terceiros)
- `js/fullcalendar.js` (plugin de terceiros)
- Arquivos de licença

## Boas Práticas

1. **Backup Sempre**: Faça backup antes de fazer alterações significativas
2. **Use CSS Customizado**: Crie um arquivo `custom.css` para suas modificações
3. **Mantenha a Estrutura**: Não mova arquivos de lugar sem atualizar os caminhos
4. **Documente Suas Mudanças**: Comente códigos complexos que você adicionar
5. **Versionamento**: Use Git para controlar versões do seu projeto

## Próximos Passos

- Configure os temas disponíveis em [Configuração](configuracao.md)
- Personalize cores e fontes em [Variáveis](variaveis.md)
- Explore os componentes em [Componentes](../componentes/)
