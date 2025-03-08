# Sistema ERP Completo

Um sistema completo de Enterprise Resource Planning (ERP) para gerenciamento empresarial, desenvolvido com tecnologias modernas para oferecer uma solução abrangente para pequenas e médias empresas.

## 🚀 Tecnologias Utilizadas

- **Next.js 15** - Framework React com App Router para renderização híbrida
- **TypeScript** - Para tipagem estática e melhor desenvolvimento
- **Tailwind CSS** - Para estilização e design responsivo
- **Prisma ORM** - Para manipulação do banco de dados
- **PostgreSQL** - Como banco de dados relacional
- **NextAuth.js** - Para autenticação e gerenciamento de sessões
- **Zod** - Para validação de dados e formulários
- **React Hook Form** - Para gerenciamento de formulários
- **Lucide React** - Para ícones consistentes

## 📋 Principais Funcionalidades

### Módulo Financeiro
- Dashboard financeiro com gráficos e métricas
- Controle de fluxo de caixa e projeções
- Gestão de contas a pagar e receber
- Conciliação bancária

### Módulo de Estoque
- Cadastro e controle de produtos
- Gestão de compras e fornecedores
- Controle de transferências entre filiais
- Alertas de estoque mínimo

### Módulo de Vendas
- PDV (Ponto de Venda) responsivo
- Sistema de orçamentos e pedidos
- Gestão de comissões
- Histórico de vendas por cliente

### Módulo Fiscal
- Emissão de notas fiscais (NF-e, NFC-e, NFS-e)
- Controle de arquivos XML
- Emissão e controle de boletos

### Módulo de Cadastros
- Gerenciamento de clientes, fornecedores e funcionários
- Categorização e segmentação
- Histórico completo de interações

### Recursos Adicionais
- Sistema de chamados e atendimento
- Agenda e calendário compartilhado
- Gestão de contratos
- Relatórios customizáveis

## 🏗️ Arquitetura

O sistema foi desenvolvido seguindo os princípios de Clean Architecture, com separação clara entre camadas de:
- **Apresentação** - Interfaces de usuário e APIs
- **Aplicação** - Lógica de negócios
- **Domínio** - Entidades e regras de negócio
- **Infraestrutura** - Persistência de dados e integrações

## 🛠️ Instalação e Uso

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/sistema-erp.git
cd sistema-erp
```

2. Instale as dependências:
```bash
npm install
```

3. Configure as variáveis de ambiente:
```bash
cp .env.example .env.local
```
Edite o arquivo `.env.local` com suas configurações

4. Execute as migrações do banco de dados:
```bash
npx prisma migrate dev
```

5. Inicie o servidor de desenvolvimento:
```bash
npm run dev
```

6. Acesse http://localhost:3000 no navegador

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👥 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e enviar pull requests para melhorar este sistema.

# CRM Gestão

Sistema de gestão empresarial completo para gerenciamento de vendas, estoque, finanças, fiscal e muito mais.

## Tecnologias utilizadas

- Next.js 15
- Prisma
- TypeScript
- TailwindCSS
- Next Auth (Autenticação customizada com JWT)

## Configuração do ambiente

1. Clone o repositório
2. Instale as dependências
```bash
npm install --legacy-peer-deps
```

3. Configure o arquivo .env com as variáveis necessárias (use .env.example como base)
```
# Banco de Dados
DATABASE_URL="file:./dev.db"

# Next Auth
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="seu-segredo-aqui"

# JWT Secret para autenticação customizada
JWT_SECRET="sua-chave-jwt-super-secreta-deve-ser-longa"

# Configurações do sistema
NEXT_PUBLIC_APP_NAME="CRM Gestão"
NEXT_PUBLIC_LOGO_URL="/logo.png"
```

## Banco de Dados

### Migrações e Seeds

O projeto utiliza Prisma para gerenciar o banco de dados. Os seguintes scripts estão disponíveis:

- `npm run db:migrate` - Executa as migrações do banco de dados
- `npm run db:studio` - Abre o Prisma Studio para visualização do banco de dados
- `npm run db:seed` - Popula o banco de dados com dados iniciais (usuários de teste)
- `npm run db:reset` - Reseta o banco de dados (apaga todos os dados e executa as migrações)
- `npm run db:generate` - Gera o cliente Prisma baseado no schema

### Criando o banco de dados pela primeira vez

```bash
# Gere o cliente Prisma
npm run db:generate

# Execute as migrações
npm run db:migrate

# Popule o banco com dados iniciais
npm run db:seed
```

### Usuários criados pelo seed

O script de seed cria três usuários de teste:

1. **Administrador**
   - Email: admin@exemplo.com
   - Senha: senha123
   - Função: ADMIN

2. **Gerente**
   - Email: gerente@exemplo.com
   - Senha: senha123
   - Função: MANAGER

3. **Usuário Padrão**
   - Email: usuario@exemplo.com
   - Senha: senha123
   - Função: USER

## Executando o projeto

```bash
# Desenvolvimento
npm run dev

# Build para produção
npm run build

# Iniciar em modo produção
npm run start
```

## Gerenciamento de Usuários

O sistema possui uma interface para gerenciar usuários em `/gerenciar-usuario`. Nesta página você pode:

- Ver todos os usuários cadastrados
- Criar usuários de exemplo
- Adicionar novos usuários

## Estrutura do projeto

- `/src/app` - Páginas e rotas da aplicação
- `/src/components` - Componentes reutilizáveis
- `/src/lib` - Utilitários e configurações
- `/prisma` - Schema e configurações do banco de dados
