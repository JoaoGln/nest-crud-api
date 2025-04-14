# 🚀 NestJS CRUD API - Gestão de UFs, Cidades e Estudantes

API RESTful desenvolvida com NestJS para gerenciamento de unidades federativas (UFs), cidades e estudantes, com relacionamentos entre as entidades.

## 📋 Funcionalidades

- **CRUD Completo** para todas as entidades
- **Relacionamentos**:
  - 1 UF → N Cidades
  - 1 Cidade → N Estudantes
- **Validação de Dados** com class-validator
- **Banco de Dados SQLite** integrado
- **CLI Interativa** para testes

## 🛠️ Tecnologias

- [NestJS](https://nestjs.com/)
- [TypeORM](https://typeorm.io/)
- [SQLite](https://www.sqlite.org/)
- [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) (para testes de API)

## 📦 Estrutura do Projeto

nest-crud-api/

├── src/

│ ├── uf/ # Entidade Unidade Federativa

│ ├── cidade/ # Entidade Cidade

│ ├── estudante/ # Entidade Estudante

│ └── app.module.ts # Configuração principal

├── cli.ts # Interface CLI interativa

├── api.http # Coleção de requisições

├── database.sqlite # Banco de dados SQLite

└── NOTES.md # Anotações do projeto

## 🚀 Como Executar

### Pré-requisitos
- Node.js (v16+)
- npm ou yarn
- Git

### Instalação
git clone https://github.com/JoaoGln/nest-crud-api.git
cd nest-crud-api
npm install
Execução

# Inicie o servidor:
npm run start:dev

# Use a CLI interativa:
npx ts-node cli.ts
Teste as rotas via api.http (com extensão REST Client)

🌐 Endpoints
UFs
POST /uf - Cria uma UF

GET /uf - Lista todas UFs

GET /uf/:id - Busca UF por ID

PATCH /uf/:id - Atualiza UF

DELETE /uf/:id - Remove UF

Cidades
POST /cidade - Cria cidade (relacionada a UF)

GET /cidade - Lista cidades com UFs

Estudantes
POST /estudante - Cria estudante (relacionado a cidade)

GET /estudante - Lista estudantes com cidades e UFs

# 📝 Exemplo de Uso
Criando uma UF via CLI:

O que você deseja fazer? Criar UF

Nome da UF: São Paulo

Sigla (2 letras): SP

✅ UF criada: { "id": 1, "nome": "São Paulo", "sigla": "SP" }
