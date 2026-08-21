# 🍒 Doce Veneno — Demo: Sistema de Gestão de Estoque

Aplicação web de demonstração para o gerenciamento de estoque e registro de vendas da loja **Doce Veneno**. O sistema substitui planilhas manuais por uma interface moderna, intuitiva e segura, permitindo o controle total das peças — da compra à venda — com cálculo automático de lucro.

> ⚠️ **Projeto de demonstração.** Este repositório não inclui credenciais reais; o arquivo `.env` é ignorado e deve ser configurado localmente.

## ✨ Funcionalidades

- 🔐 **Autenticação segura:** login e cadastro de usuários (JWT + sessão).
- 📦 **Gestão de estoque:** adicionar, editar e remover peças (nome, quantidade, cor, tamanho, preço de compra/venda).
- 💰 **Registro de vendas:** marcar peças como vendidas e calcular o lucro automaticamente.
- 📊 **Histórico de vendas:** resumo financeiro com total vendido, custo e lucro.
- 🔍 **Pesquisa e filtros:** busca em tempo real no estoque.
- ✅ **Ações em lote:** vender ou excluir múltiplas peças de uma vez.
- 🎨 **Tema escuro:** interface responsiva e moderna.

## 🚀 Tecnologias

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla, ES6+)
- **Backend:** Node.js + Express.js
- **Banco de dados:** MongoDB e Supabase (PostgreSQL)
- **Autenticação:** JWT, bcrypt, express-session
- **Hospedagem:** Render / Vercel

## ▶️ Como rodar localmente

### Pré-requisitos

- [Node.js](https://nodejs.org/) 18+
- [npm](https://www.npmjs.com/)
- Conta no [MongoDB Atlas](https://www.mongodb.com/) e [Supabase](https://supabase.com/)

### Instalação

```bash
# 1. Instalar dependências
npm install

# 2. Configurar variáveis de ambiente
cp .env.example .env   # se existir, ou crie o .env manualmente

# 3. Rodar as migrações do banco (se aplicável)
node migration_script.js

# 4. Iniciar o servidor de desenvolvimento
npm run dev
```

Acesse em `http://localhost:3000`.

### Variáveis de ambiente (`/c/Users/lucas/Documents/Projetos programação/Sites/Demo Doce Veneno Planilha/.env`)

| Variável | Descrição |
| --- | --- |
| `MONGO_URI` | String de conexão do MongoDB |
| `PORT` | Porta do servidor (padrão `3000`) |
| `JWT_SECRET` | Segredo para os tokens JWT |
| `SUPABASE_URL` / `SUPABASE_SERVICE_KEY` | Credenciais do Supabase |
| `EMAIL_USER` / `EMAIL_PASS` | Credenciais de envio de e-mail (Gmail) |
| `ADMIN_USERNAME` / `ADMIN_PASSWORD` | Credenciais do painel administrativo |

> Windows: use caminhos e argumentos no formato MSYS (`/c/Users/<user>/...`).

## 📂 Estrutura

```
Demo Doce Veneno Planilha/
├── server.js            # Servidor Express
├── migration_script.js  # Script de migração
├── package.json
├── vercel.json
├── public/              # Frontend (HTML, CSS, JS, imagens)
│   ├── index.html
│   ├── estoque.html
│   ├── vendas.html
│   ├── style.css
│   ├── js/              # Scripts do frontend
│   └── imagens/
└── supabase/            # Configuração e migrações Supabase
```

---

© Lucas Oliveira