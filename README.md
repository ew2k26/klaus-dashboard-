<div align="center">

# 🌐 Klaus Dashboard

### Dashboard web para configuracao do Klaus Bot

[![Flask](https://img.shields.io/badge/Flask-3.0-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Vercel](https://img.shields.io/badge/Vercel-Deployed-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://klaus-dashboard-delta.vercel.app)

**Demo:** [klaus-dashboard-delta.vercel.app](https://klaus-dashboard-delta.vercel.app)

</div>

---

## 📋 Sobre

O **Klaus Dashboard** e um painel web completo para configuracao e gerenciamento do Klaus Bot. Com ele, administradores de servidores podem personalizar todas as funcionalidades do bot de forma visual e intuitiva.

---

## ⭐ Funcionalidades

### 🔐 Autenticacao
- Login via Discord OAuth2
- Sessoes seguras com cookies HTTP-only
- Verificacao de permissoes de administrador

### ⚙️ Configuracao do Servidor
- **Boas-vindas**: Mensagens personalizadas com embed, imagem e cores
- **Adeus**: Mensagens de despedida configuraveis
- **Auto-Cargo**: Atribuicao automatica de cargo ao entrar
- **Logging**: Logs de mensagens, membros, moderacao e voz
- **Auto-Resposta**: Respostas automaticas ao bot

### 💰 Sistema Economico
- Configuracao de koins iniciais
- Cooldowns de daily, work, rob
- Configuracoes de crime e heist
- Sistema de loteria e cofre

### 📊 Sistema de XP
- Configuracao de XP minimo/maximo
- Cooldown entre mensagens
- Recompensas por cargo
- Canal de anuncios de level-up

### 🛡️ Auto-Moderacao
- Anti-spam configuravel
- Anti-links
- Lista de palavras proibidas
- Deteccao de raid

### 🎨 Personalizacao
- Cores do embed primario, sucesso, erro e aviso
- Configuracoes de fun commands
- Configuracoes premium

### 👤 Perfil do Usuario
- Visualizacao do perfil com imagem gerada
- Personalizacao de background e borda
- Loja de cosmetics

### 🏆 Leaderboard
- Ranking publico de koins
- Ranking de XP por servidor
- Estatisticas detalhadas

### 📋 Status
- Status em tempo real do bot
- Estatisticas de uso
- Informacoes de uptime

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|------------|-----|
| **Flask** | Framework web backend |
| **Jinja2** | Motor de templates |
| **MongoDB** | Banco de dados |
| **PyMongo** | Driver MongoDB |
| **HTML/CSS/JS** | Frontend |
| **Vercel** | Hospedagem |

---

## 🚀 Instalacao

### Requisitos
- Python 3.11+
- MongoDB (local ou Atlas)
- Discord App credentials

### 1. Clone o repositorio

```bash
git clone https://github.com/ew2k26/klaus-dashboard-.git
cd klaus-dashboard-
```

### 2. Crie ambiente virtual

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/Mac
source venv/bin/activate
```

### 3. Instale dependencias

```bash
pip install -r requirements.txt
```

### 4. Configure variaveis de ambiente

Crie um arquivo `.env`:

```env
CLIENT_ID=seu_discord_client_id
CLIENT_SECRET=seu_discord_client_secret
BOT_TOKEN=seu_bot_token
MONGODB_URL=sua_url_mongodb
REDIRECT_URI=https://klaus-dashboard-delta.vercel.app/callback
MOD_PASSWORD=sua_senha_moderador
```

### 5. Execute localmente

```bash
python app.py
```

O dashboard estara disponivel em `http://localhost:5000`

---

## 🌐 Deploy

### Vercel (Recomendado)

1. Conecte o repositorio ao Vercel
2. Configure as variaveis de ambiente no painel do Vercel
3. O deploy sera feito automaticamente

### Heroku

1. Crie um app no Heroku
2. Configure as variaveis de ambiente
3. Faca push do codigo

---

## 📁 Estrutura

```
klaus-dashboard-/
├── app.py              # Backend Flask (monolitico)
├── requirements.txt    # Dependencias Python
├── Procfile            # Configuracao Heroku
├── runtime.txt         # Versao Python
├── vercel.json         # Configuracao Vercel
├── static/
│   ├── style.css       # Estilos CSS (46KB)
│   └── script.js       # JavaScript (19KB)
└── templates/
    ├── index.html      # Pagina principal
    ├── dashboard.html  # Painel de servers
    ├── server.html     # Config do server
    ├── moderacao.html  # Painel de moderacao
    ├── profile.html    # Perfil do usuario
    ├── leaderboard.html # Ranking publico
    ├── status.html     # Status do bot
    ├── privacy.html    # Politica de privacidade
    └── terms.html      # Termos de servico
```

---

## 🔒 Seguranca

- Tokens armazenados em cookies HTTP-only secure
- OAuth2 com scopes minimos (identify + guilds)
- Verificacao de permissoes de administrador
- Whitelist de campos permitidos para escrita no banco
- Certificados TLS para conexao MongoDB

---

## 📄 Licenca

Licenciado sob a MIT License.

---

<div align="center">

**Feito com 💜 para a comunidade Klaus Bot**

</div>
