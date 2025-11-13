# 🎨 NS Studio Criações Digitais

[![Deploy Status](https://img.shields.io/badge/Deploy-Success-brightgreen)](https://github.com/nsstudio/criacoes-digitais)
[![Node.js Version](https://img.shields.io/badge/Node.js-18+-green)](https://nodejs.org/)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

## 📋 Sobre o Projeto

Sistema completo de vendas de produtos digitais com funcionalidades avançadas de gerenciamento, afiliados, cupons e integração com WhatsApp.

### ✨ Funcionalidades Principais

- 🔐 **Sistema de Permissões**: Owner, Admin e Membro
- 🛒 **E-commerce Completo**: Carrinho, checkout e entrega
- 💰 **Sistema de Afiliados**: Comissões e dashboard
- 🎫 **Cupons de Desconto**: Múltiplos tipos e validações
- 📱 **Integração WhatsApp**: Mensagens personalizadas
- 📊 **Analytics Avançado**: Relatórios e estatísticas
- 🎮 **Gamificação**: Pontos e conquistas
- 🤖 **IA Integrada**: Automações inteligentes
- 📁 **Entrega Segura**: Download protegido de arquivos
- 🎨 **Interface Moderna**: Design responsivo e animações

## 🚀 Deploy Rápido

### 1. GitHub + Vercel (Recomendado)

\`\`\`bash
# 1. Fork este repositório
# 2. Conecte ao Vercel
# 3. Configure as variáveis de ambiente
# 4. Deploy automático!
\`\`\`

### 2. Heroku

\`\`\`bash
# Clone o repositório
git clone https://github.com/SEU_USUARIO/ns-studio-criacoes-digitais.git
cd ns-studio-criacoes-digitais

# Crie app no Heroku
heroku create ns-studio-app

# Configure variáveis
heroku config:set NODE_ENV=production
heroku config:set SESSION_SECRET=sua_chave_secreta_forte
heroku config:set ADMIN_PASSWORD=sua_senha_admin
heroku config:set OWNER_PASSWORD=sua_senha_owner
heroku config:set WHATSAPP_NUMBER=5511999999999

# Deploy
git push heroku main
\`\`\`

### 3. Railway

\`\`\`bash
# 1. Conecte seu GitHub ao Railway
# 2. Selecione este repositório
# 3. Configure as variáveis de ambiente
# 4. Deploy automático!
\`\`\`

## ⚙️ Configuração

### Variáveis de Ambiente Obrigatórias

\`\`\`env
NODE_ENV=production
PORT=3000
SESSION_SECRET=sua_chave_secreta_super_forte_aqui
ADMIN_PASSWORD=sua_senha_admin_aqui
OWNER_PASSWORD=sua_senha_owner_aqui
WHATSAPP_NUMBER=5511999999999
SITE_NAME=NS Studio Criações Digitais
OWNER_NAME=Seu Nome
\`\`\`

### Instalação Local

\`\`\`bash
# Clone o repositório
git clone https://github.com/SEU_USUARIO/ns-studio-criacoes-digitais.git
cd ns-studio-criacoes-digitais

# Instale dependências
npm install

# Configure .env
cp .env.example .env
# Edite o arquivo .env com suas configurações

# Inicie o servidor
npm run dev
\`\`\`

## 📱 Uso

### Acesso Inicial

1. **Owner**: `/admin` com a senha configurada em `OWNER_PASSWORD`
2. **Admin**: Criado pelo Owner no painel
3. **Usuários**: Registro público em `/signup`

### Funcionalidades por Perfil

#### 👑 Owner
- Acesso total ao sistema
- Gerenciamento de admins
- Configurações globais
- Backup e manutenção
- Analytics completo

#### 🛡️ Admin
- Gerenciamento de produtos
- Usuários e pedidos
- Cupons e afiliados
- Relatórios básicos

#### 👤 Membro
- Compra de produtos
- Download de arquivos
- Perfil pessoal
- Histórico de compras

## 🛠️ Tecnologias

- **Backend**: Node.js + Express
- **Frontend**: EJS + Bootstrap 5
- **Banco**: JSON (File-based)
- **Upload**: Multer
- **Segurança**: Bcrypt + Sessions
- **Integração**: WhatsApp API
- **Deploy**: Vercel/Heroku/Railway

## 📊 Estrutura do Projeto

\`\`\`
ns-studio-criacoes-digitais/
├── 📁 config/          # Configurações
├── 📁 routes/          # Rotas da aplicação
├── 📁 views/           # Templates EJS
├── 📁 public/          # Arquivos estáticos
├── 📁 secret/          # Dados JSON
├── 📁 uploads/         # Arquivos de produtos
├── 📁 scripts/         # Scripts de manutenção
├── 📄 server.mjs       # Servidor principal
├── 📄 package.json     # Dependências
└── 📄 README.md        # Este arquivo
└── # A PARTE A BAIXO FOI CORTADA PRA N SER LONGO
\`\`\`

## 🔒 Segurança

- ✅ Senhas criptografadas (bcrypt)
- ✅ Sessões seguras
- ✅ Validação de entrada
- ✅ Rate limiting
- ✅ Headers de segurança
- ✅ Upload seguro de arquivos
- ✅ Controle de acesso granular

## 📈 Performance

- ⚡ Compressão Gzip
- ⚡ Cache de arquivos estáticos
- ⚡ Otimização de imagens
- ⚡ Lazy loading
- ⚡ Minificação CSS/JS

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

## 📞 Suporte

- 📧 Email: suporte@nsstudio.com
- 💬 WhatsApp: +55 22 97400 8281

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🎉 Agradecimentos

Obrigado por usar o NS Studio Criações Digitais! 

---

**Desenvolvido com ❤️ por NS Studio**
