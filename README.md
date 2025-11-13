# NS Studio Criações Digitais

Plataforma completa para venda de produtos digitais com sistema de afiliados, gamificação e automação. Este repositório inclui servidor Express com EJS, páginas estilizadas em Bootstrap, e infraestrutura Docker com Nginx como reverse proxy.

## Recursos Principais
- Autenticação de usuários e cadastro
- Dashboard do usuário com métricas
- Loja com filtros, ordenação e página de produto
- Painel Administrativo (usuários, produtos, configurações, logs, backup)
- Sistema de Tickets (cliente cria, admin responde)
- Wishlist (lista de desejos) por usuário
- Modo Manutenção com bloqueio para visitantes

## Requisitos
- Node.js 18+
- Docker 28+ (opcional, recomendado)

## Ambiente (variáveis)
- `PORT` (padrão: 3000)
- `NODE_ENV` (padrão: production)
- `SESSION_SECRET`
- `SITE_NAME`, `OWNER_NAME`, `WHATSAPP_NUMBER` (opcionais)

## Executando com Docker
1. Build e subir serviços:
```
docker compose up -d
```
2. Acessar:
- App: `http://localhost/` (via Nginx)
- App direto: `http://localhost:3000/`
3. Logs:
```
docker compose logs --no-color --tail 200
```

## Desenvolvimento local (sem Docker)
```
npm install
npm run dev
```
Acesse `http://localhost:3000/`.

## Estrutura
- `server.mjs`: servidor Express e middleware de manutenção
- `views/`: páginas EJS (login, loja, produto, dashboard, admin, etc.)
- `routes/`: rotas modulares (admin, wishlist, tickets, etc.)
- `secret/`: arquivos JSON persistentes (users, produtos, sales, tickets, logs, ...)
- `public/`: estáticos

## Rotas Importantes
- Público: `/`, `/login`, `/signup`, `/loja`, `/loja/produto/:id`
- Usuário: `/dashboard`, `/dashboard/produtos`
- Admin: `/admin` e APIs sob `/admin/*`
- Wishlist API: `/api/wishlist/*`
- Tickets: `/tickets/*`

## Modo Manutenção
- Ative em Configurações (Admin) ou ajustando `secret/settings.json` (`maintenanceMode: true`).
- Visitantes são direcionados para `views/maintenance.ejs`; admins continuam com acesso.

## Troubleshooting
- Se ver “Internal Server Error” em `/loja/produto/:id`, garanta que o produto existe em `secret/produtos.json` e que a página `views/produto.ejs` está atualizada.
- Admin “Erro ao carregar/deletar produtos”: atualizado para retornar `{products}` e implementado `DELETE /admin/products/:productId`.
- Wishlist: montada em `/api/wishlist`; exige login.
- Tickets: montados em `/tickets`; admins podem alterar status e responder.

## Segurança
- Não use `MemoryStore` em produção. Configure um store de sessão (Redis, etc.).
- Não faça commit de segredos.

## Licença
MIT
