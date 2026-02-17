# Guia de Instalação do AdminKit

Bem-vindo ao AdminKit Pro! Este guia irá ajudá-lo a instalar e configurar o template em seu projeto.

## Requisitos do Sistema

Antes de começar, certifique-se de que você possui os seguintes requisitos:

- **Navegador Moderno**: Chrome, Firefox, Safari, Edge (versões mais recentes)
- **Servidor Web**: Qualquer servidor web local ou remoto (Apache, Nginx, etc.)
- **Editor de Código**: VS Code, Sublime Text, ou qualquer editor de sua preferência

## Opções de Instalação

### Opção 1: Download Direto

1. Baixe o arquivo ZIP do AdminKit Pro
2. Extraia o conteúdo para uma pasta em seu computador
3. Abra a pasta extraída em seu editor de código

### Opção 2: Via Git

Se você possui acesso ao repositório Git:

```bash
git clone [url-do-repositorio]
cd AdminKitPro
```

## Estrutura de Arquivos

Após a extração, você verá a seguinte estrutura:

```
AdminKitPro/
├── css/                 # Arquivos de estilo (light.css, dark.css)
├── js/                  # Arquivos JavaScript
├── img/                 # Imagens e ícones
├── fonts/               # Fontes utilizadas
├── docs/                # Documentação
└── *.html              # Páginas do template
```

## Servindo o Projeto

### Usando um Servidor Local

#### Opção A: Servidor Python (Instalado por padrão no macOS/Linux)

```bash
# Python 3
python3 -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Acesse: `http://localhost:8000`

#### Opção B: Servidor Node.js (http-server)

```bash
# Instale globalmente
npm install -g http-server

# Execute na pasta do projeto
http-server -p 8000
```

Acesse: `http://localhost:8000`

#### Opção C: Extensão Live Server (VS Code)

1. Instale a extensão "Live Server" no VS Code
2. Clique com o botão direito em `index.html`
3. Selecione "Open with Live Server"

### Usando um Servidor Web Tradicional

#### Apache

Coloque os arquivos na pasta pública do seu servidor web:

```bash
# Linux/macOS
/var/www/html/

# macOS (com Homebrew)
/usr/local/var/www/
```

#### Nginx

Configure o root do seu site para apontar para a pasta do AdminKit:

```nginx
server {
    listen 80;
    server_name seu-dominio.com;
    root /caminho/para/AdminKitPro;
    index index.html;
}
```

## Primeiro Acesso

1. Abra seu navegador e acesse o endereço do servidor local
2. Você verá a página inicial (Dashboard Analytics)
3. Para personalizar o tema, clique no ícone de configurações no canto superior direito

## Próximos Passos

- Configure o tema de acordo com suas preferências (veja [Configuração](configuracao.md))
- Explore a [Estrutura de Arquivos](estrutura.md)
- Personalize as [Variáveis de Customização](variaveis.md)
- Veja os [Componentes Disponíveis](../componentes/)

## Solução de Problemas

### O template não carrega corretamente

- Verifique se todos os arquivos estão na pasta correta
- Certifique-se de que os caminhos no HTML apontam para os locais corretos
- Verifique o console do navegador por mensagens de erro

### Os ícones não aparecem

- Verifique se a pasta `img/icons/` existe e contém os arquivos
- Certifique-se de que o arquivo `feather-icons.js` está sendo carregado

### O JavaScript não funciona

- Verifique se o arquivo `js/app.js` está sendo carregado
- Certifique-se de que o jQuery e o Bootstrap estão carregados antes do app.js

## Suporte

Se você encontrar algum problema não resolvido neste guia:

1. Consulte a [documentação oficial](https://adminkit.io/docs/)
2. Verifique o [fórum da comunidade](https://adminkit.io/community)
3. Entre em contato com o [suporte técnico](https://adminkit.io/support)
